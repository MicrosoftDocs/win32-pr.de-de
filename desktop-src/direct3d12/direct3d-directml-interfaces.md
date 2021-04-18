---
title: DirectML-Schnittstellen
description: Die folgenden Schnittstellen werden in "directml. h" deklariert.
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 9752b52f1d9a311a1ada6b609a86691a336b77e7
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "106341567"
---
# <a name="directml-interfaces"></a>DirectML-Schnittstellen

Die folgenden Schnittstellen werden in "directml. h" deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) | Erstellt ein directml-Gerät für ein bestimmtes Direct3D 12-Gerät. |
| [**IDMLCommandRecorder**](/windows/desktop/api/directml/nn-directml-idmlcommandrecorder) | Datensätze: die Verteilung von directml funktioniert in eine Direct3D 12-Befehlsliste. |
| [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) | Stellt eine kompilierte, effiziente Form eines Operators dar, der für die Ausführung auf der GPU geeignet ist. |
| [**IDMLDebugDevice**](/windows/desktop/api/directml/nn-directml-idmldebugdevice) | Steuert die directml-debugschicht. |
| [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice) | Stellt ein directml-Gerät dar, das zum Erstellen von Operatoren, Bindungs Tabellen, Befehls Recorder und anderen Objekten verwendet wird. |
| [**IDMLDevice1**](/windows/desktop/direct3d12/directml/nn-directml-idmldevice1) | Stellt ein directml-Gerät dar, das zum Erstellen von Operatoren, Bindungs Tabellen, Befehls Recorder und anderen Objekten verwendet wird. |
| [**IDMLDeviceChild**](/windows/win32/api/directml/nn-directml-idmldevicechild) | Eine Schnittstelle, die von allen-Objekten implementiert wird, die auf dem directml-Gerät |
| [**IDMLDispatchable**](/windows/desktop/api/directml/nn-directml-idmldispatchable) | Wird von Objekten implementiert, die mithilfe von [idmlcommandrecorder:: recorddispatch](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)in einer Befehlsliste für die Verteilung auf der GPU aufgezeichnet werden können. |
| [**IDMLObject**](/windows/desktop/api/directml/nn-directml-idmlobject) | Eine Schnittstelle, von der [idmldevice](/windows/win32/api/directml/nn-directml-idmldevice) und [idmldevicechild](/windows/desktop/api/directml/nn-directml-idmldevicechild) direkt geerbt werden (und alle anderen Schnittstellen, indirekt). Folglich werden Methoden bereitstellt, die allen directml-Schnittstellen gemeinsam sind, insbesondere Methoden, um private Daten zuzuordnen und Objektnamen zu kommentieren. |
| [**IDMLOperator**](/windows/desktop/api/directml/nn-directml-idmloperator) | Stellt einen directml-Operator dar. |
| [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) | Stellt ein spezialisiertes Objekt dar, dessen Zweck die Initialisierung von kompilierten Operatoren ist. |
| [**IDMLPageable**](/windows/desktop/api/directml/nn-directml-idmlpageable) | Wird von Objekten implementiert, die aus GPU-Speicher entfernt werden können, und kann daher für [idmldevice:: evict](/windows/desktop/api/directml/nf-directml-idmldevice-evict) und [idmldevice:: makeresident](/windows/desktop/api/directml/nf-directml-idmldevice-makeresident)bereitgestellt werden. |

## <a name="related-topics"></a>Zugehörige Themen

* [DirectML-Referenz](direct3d-directml-reference.md)
* [Core-Referenz](direct3d-12-core-reference.md)
* [Referenz für Direct3D 12](direct3d-12-reference.md)
