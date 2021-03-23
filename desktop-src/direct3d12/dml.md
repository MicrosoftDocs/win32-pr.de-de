---
title: Direct Machine Learning (DirectML)
description: Direct Machine Learning (directml) ist eine API auf niedriger Ebene für Machine Learning. Sie hat eine vertraute (natives C++, Nano-COM) Schnittstelle und einen Workflow im Stil von DirectX 12.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 25bbd169a1ad0467ed56135c31c8c2a0b70b57a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103568"
---
# <a name="direct-machine-learning-directml"></a>Direct Machine Learning (DirectML)

Direct Machine Learning (directml) ist eine API auf niedriger Ebene für Machine Learning. Sie hat eine vertraute (natives C++, Nano-COM) Schnittstelle und einen Workflow im Stil von DirectX 12. Sie können Machine Learning-Rückschlussworkloads in Ihr Spiel, Ihre Engine, Ihre Middleware, Ihr Back-End oder in eine andere Anwendung integrieren. DirectML wird von jeder DirectX 12-kompatiblen Hardware unterstützt.

Directml wird in Windows 10, Version 1903, und in der entsprechenden Version des Windows SDK eingeführt.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [Introduction to DirectML](dml-intro.md) (Einführung in DirectML) | Direct Machine Learning (directml) ist eine API auf niedriger Ebene für Machine Learning (ml). |
| [Bindung in DirectML](dml-binding.md) | In directml bezieht sich *Bindung* auf die Anlage von Ressourcen an die Pipeline, die die GPU während der Initialisierung und Ausführung ihrer Machine Learning-Operatoren verwenden soll. Bei diesen Ressourcen kann es sich um Eingabe-und Ausgabe Tensoren handeln, z. b. um temporäre oder permanente Ressourcen, die der Operator benötigt. |
| [UAV-Barrieren und Ressourcen Zustands Barrieren in directml](dml-barriers.md) | Beschreibt die Richtigkeit der Vorteile von Barrieren und wie Sie in directml mit Ihnen arbeiten können. |
| [Verwenden von Schritten zum Ausdrücken von Auffüll-und Speicher Layout](dml-strides.md) | Directml-Tensoren werden von Eigenschaften beschrieben, die als *Größen* und *Fortschritte* des Mandanten bezeichnet werden. |
| [Ressourcenlebensdauer und -synchronisierung](dml-resource-lifetime.md) | Um ein nicht definiertes Verhalten zu vermeiden, muss Ihre directml-Anwendung die Objekt Lebensdauer und Synchronisierung zwischen der CPU und der GPU ordnungsgemäß verwalten. |
| [Verwenden der directml-debugschicht](dml-debug-layer.md) | Die directml-debugschicht ist eine optionale Entwicklungszeit Komponente, die Sie beim Debuggen Ihres directml-Codes unterstützt. |
| [Behandeln von Fehlern und Entfernen von Geräten](dml-errors.md) | In diesem Thema wird erläutert, wie Sie das Entfernen von Geräte-und anderen Fehlerzuständen in directml Debuggen. |
| [Directml-Hilfsfunktionen](dml-helper-functions.md) | Code Auflistungen wichtiger directml-Hilfsfunktionen. |
| [DirectML Sample Applications](dml-min-app.md) (DirectML-Beispielanwendungen) | Links zu directml-Beispielanwendungen, einschließlich einer Stichprobe einer minimalen directml-Anwendung. |

## <a name="related-topics"></a>Verwandte Themen

* [Direct3D 12-Programmieranleitung](directx-12-programming-guide.md)
