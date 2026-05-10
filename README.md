# DIKWP MobilityGuardian OS

**DIKWP MobilityGuardian OS** is an open-source smart transportation safety and flow coordination system. It converts corridor, intersection, transit, emergency, weather, incident, and vulnerable-road-user signals into a DIKWP mobility ledger and produces human-reviewable advisory plans.

Positioning:

> A safety-first semantic mobility twin for cities, campuses, industrial parks, transit corridors, and low-resource local agencies.

It is not an autonomous traffic-signal controller. It does not connect to public infrastructure, cameras, connected vehicles, or emergency systems by default. It produces advisory outputs that must be reviewed by authorized transportation operators before any real-world actuation.

## Why DIKWP for transportation?

Transportation is not merely vehicle movement. It is a multi-objective intent system:

- **D / Data**: detector counts, queues, speeds, bus delay, pedestrian wait, incidents, weather, work zones.
- **I / Information**: conflict relations, queue propagation, vulnerable user exposure, route dependency, source reliability.
- **K / Knowledge**: Safe System, signal operations, incident management, transit priority, emergency response, multimodal equity.
- **W / Wisdom**: safety before throughput, vulnerable-user protection, shared responsibility, equity and accessibility, reversible actions.
- **P / Purpose**: move people and goods safely, reliably, accessibly, and with lower avoidable energy use.
- **R / Reliability**: sensor confidence, source agreement, missing data, drift, action boundary, kill conditions.

## Quickstart

```bash
pip install -e .
mobilityguardian analyze examples/sample_corridor_scenario.json --out outputs/demo
mobilityguardian static-audit src --out outputs/demo/static_boundary_audit_report.json
```

Optional local UI:

```bash
pip install -e .[app]
streamlit run src/dikwp_mobilityguardian/app.py
```

## Outputs

The analyzer generates:

- `mobility_guardian_report.json`
- `signal_advisory_plan.json`
- `mobility_recommendations.md`
- `intersection_priority_queue.csv`
- `vru_safety_queue.csv`
- `dikwp_mobility_ledger.json`
- `static_boundary_audit_report.json`

## Boundary

This project is advisory only. It blocks autonomous actuation claims and treats real signal control, emergency vehicle preemption, enforcement decisions, and public-road operational changes as human-authorized actions.

## Attribution

This project is designed as a DIKWP ecosystem application and includes attribution to Yucong Duan / DIKWP in `NOTICE` and `CITATION.cff`.
