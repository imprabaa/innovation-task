public class BMACalculator {

  
    public static double calculateBMA(Map<String, Double> modelPredictions, Map<String, Double> modelWeights) {
        double weightedSum = 0.0;
        double totalWeight = 0.0;

        for (String model : modelPredictions.keySet()) {
            double prediction = modelPredictions.get(model);
            double weight = modelWeights.getOrDefault(model, 0.0);
            weightedSum += prediction * weight;
            totalWeight += weight;
        }

      
        if (totalWeight == 0) {
            throw new IllegalArgumentException("Total weight cannot be zero.");
        }

        return weightedSum / totalWeight;
    }

    public static void main(String[] args) {
      
        Map<String, Double> modelPredictions = new HashMap<>();
        modelPredictions.put("Model1", 10.0);
        modelPredictions.put("Model2", 20.0);
        modelPredictions.put("Model3", 30.0);

    
        Map<String, Double> modelWeights = new HashMap<>();
        modelWeights.put("Model1", 0.2);
        modelWeights.put("Model2", 0.5);
        modelWeights.put("Model3", 0.3);

        
        double bmaResult = calculateBMA(modelPredictions, modelWeights);
        System.out.println("Bayesian Model Averaging Result: " + bmaResult);
    }
}
