# PAssign08
modify mileage calculator
working with adding an additional method that will convert the values in the textfield
private void convertValues() {
		double distance = 0.0, capacity = 0.0;
		if (tfCapacity.getText() != null && !tfCapacity.getText().isEmpty() && tfDistance.getText() != null
				&& !tfDistance.getText().isEmpty()) {
			distance = Double.parseDouble(tfDistance.getText());
			capacity = Double.parseDouble(tfCapacity.getText());

		}
		if (comboBox.getValue().equals(altResult)) {
			distance *= 1.609;
			capacity *= 3.785;

			tfDistance.setText(String.format("%.2f", distance));
			tfCapacity.setText(String.format("%.2f", capacity));
			calcMileage();
		} else {
			distance *= 0.621;
			capacity *= 0.264;

			tfDistance.setText(String.format("%.2f", distance));
			tfCapacity.setText(String.format("%.2f", capacity));
			calcMileage();
		}

	}
