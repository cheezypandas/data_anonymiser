# data_anonymiser
Takes any dataset and anonymises it for commercial analysis.


Data Miser is a desktop application developed using Tkinter and Pandas, tailored for large organisations like financial institutions or government agencies to anonymise datasets securely. It offers a flexible foundation for responsible data handling, bridging practical use with privacy assurance. The tool directly anonymises CSV, Excel and Zip files while providing optional privacy guarantees such as k-anonymity. Its design emphasises functionality, modularity, and practicality in data governance.

At the core of the app is a clear anonymisation pipeline that allows the user to load a CSV file, select specific columns considered personally identifiable, and replace their values with standardised tokens like "REDACTED". This approach offers straightforward pseudonymisation useful for pre-processing tasks, demonstrations, or less complex use cases where full formal guarantees are not required.

For cases requiring more robust protections, the application offers optional support for k-anonymity. When this feature is enabled, the user may define a k value (e.g. k=3), and the application ensures that all quasi-identifier groups meet the threshold. Where the threshold is not met, suppression is applied using "SUPPRESSED" to prevent individual records from being distinguished. This balance between simplicity and rigour makes the tool suitable both for everyday privacy-conscious work and for more regulated environments, without forcing unnecessary overhead when it’s not needed.

The decision to make advanced privacy controls optional was intentional — real-world anonymisation often requires trade-offs between utility and risk, and this approach allows the user to decide based on their context. Moreover, every core component of the anonymisation logic is separated from interface elements, ensuring the tool can be extended in future with minimal friction.

Workflow:

1. Open the app and load a CSV dataset.

2. Select the columns that should be anonymised.

2.1 (Optional) Enable the k-anonymity feature and input your desired k value.

3. Run the anonymisation process.

4. Save the anonymised output as a new CSV file.
