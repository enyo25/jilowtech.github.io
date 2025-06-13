import React from "react";
import { Card, CardContent } from "@/components/ui/card";

const caseStudies = [
  {
    title: "Smart City Infrastructure & Sustainability Dashboard",
    slug: "smart-city",
    summary:
      "Optimize urban resource usage and public service delivery using real-time sensor, utility, complaint, and budget data.",
    kpis: [
      "Air quality, noise, and traffic KPIs",
      "Utility consumption trends",
      "Complaint sentiment trends",
      "Budget vs. actual spend"
    ],
    visuals: [
      "Map visuals by sensor type",
      "Sankey chart: Budget flow",
      "Utility usage heatmap"
    ],
    modeling: [
      "Geo-clustering",
      "Budget variance modeling",
      "Sentiment + sensor prediction"]
  },
  {
    title: "AI-Powered Retail & Customer Journey Analytics",
    slug: "retail-journey",
    summary:
      "Understand customer behavior across transactions, reviews, and web clickstream to boost retention and engagement.",
    kpis: [
      "AOV and frequency",
      "Click-through to conversion",
      "Product sentiment",
      "CLV modeling"
    ],
    visuals: [
      "Funnel: click → cart → purchase",
      "SKU sentiment heatmap",
      "Cohort chart"
    ],
    modeling: [
      "RFM segmentation",
      "Review sentiment scoring",
      "Clickstream clustering"]
  },
  {
    title: "Healthcare Provider Optimization & Patient Outcome Analysis",
    slug: "healthcare-outcomes",
    summary:
      "Improve delivery by linking patient treatment, outcomes, staff scheduling, and claims.",
    kpis: [
      "Avg. treatment time",
      "Recovery rate",
      "Staff utilization",
      "Claim approval %"
    ],
    visuals: [
      "Gantt chart of treatments",
      "Outcome distribution",
      "Claims over time"
    ],
    modeling: [
      "Time-based relationships",
      "Predictive indicators",
      "Drill-through claims analysis"]
  },
  {
    title: "Financial Crime Detection & Compliance Monitoring",
    slug: "fincrime-monitoring",
    summary:
      "Detect suspicious activity via transaction patterns, alerts, and watchlist hits.",
    kpis: [
      "% of flagged transactions",
      "Alert resolution time",
      "High-risk customer distribution"
    ],
    visuals: [
      "Customer → AML → Transactions network",
      "Risk heatmap",
      "Alert status chart"
    ],
    modeling: [
      "Dynamic risk thresholds",
      "Rolling anomaly detection",
      "Drill-through AML workflows"]
  },
  {
    title: "Streaming Platform & Viewer Behavior Analytics",
    slug: "streaming-analytics",
    summary:
      "Drive engagement by analyzing viewing patterns, ratings, and subscription trends.",
    kpis: [
      "Avg. watch time",
      "Rating trends",
      "Binge session frequency"
    ],
    visuals: [
      "Watch duration by genre",
      "Rating vs. production cost",
      "Engagement by region"
    ],
    modeling: [
      "Binge detection logic",
      "Viewer segmentation",
      "Sentiment-driven NPS"]
  }
];

export default function PortfolioPage() {
  return (
    <div className="grid gap-6 p-6 md:grid-cols-2">
      {caseStudies.map((item) => (
        <Card key={item.slug} className="rounded-2xl shadow-lg">
          <CardContent className="p-4">
            <h2 className="text-xl font-bold text-blue-800 mb-2">{item.title}</h2>
            <p className="text-sm mb-2 text-gray-700">{item.summary}</p>
            <div className="text-sm">
              <p className="font-semibold text-gray-600">Key KPIs:</p>
              <ul className="list-disc ml-5 text-gray-800">
                {item.kpis.map((kpi, idx) => (
                  <li key={idx}>{kpi}</li>
                ))}
              </ul>
              <p className="font-semibold text-gray-600 mt-2">Visuals:</p>
              <ul className="list-disc ml-5 text-gray-800">
                {item.visuals.map((vis, idx) => (
                  <li key={idx}>{vis}</li>
                ))}
              </ul>
              <p className="font-semibold text-gray-600 mt-2">Advanced Modeling:</p>
              <ul className="list-disc ml-5 text-gray-800">
                {item.modeling.map((mod, idx) => (
                  <li key={idx}>{mod}</li>
                ))}
              </ul>
            </div>
          </CardContent>
        </Card>
      ))}
    </div>
  );
}
# jilowtech.github.io
