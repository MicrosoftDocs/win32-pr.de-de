---
title: DirectML-Schnittstellen
description: Die folgenden Schnittstellen werden in DirectML.h deklariert.
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: deb388962043926afd3868785364df6297b05d78f3997359fc88ea97ab679f33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728950"
---
# <a name="directml-interfaces"></a>DirectML-Schnittstellen

Die folgenden Schnittstellen werden in DirectML.h deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) | Erstellt ein DirectML-Gerät für ein bestimmtes Direct3D 12-Gerät. |
| [**IDMLCommandRecorder**](/windows/desktop/api/directml/nn-directml-idmlcommandrecorder) | Zeichnet Verteilungen von DirectML-Arbeiten in eine Direct3D 12-Befehlsliste auf. |
| [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) | Stellt eine kompilierte, effiziente Form eines Operators dar, der für die Ausführung auf der GPU geeignet ist. |
| [**IDMLDebugDevice**](/windows/desktop/api/directml/nn-directml-idmldebugdevice) | Steuert die DirectML-Debugebene. |
| [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice) | Stellt ein DirectML-Gerät dar, das zum Erstellen von Operatoren, Bindungstabellen, Befehlsaufzeichnungen und anderen Objekten verwendet wird. |
| [**IDMLDevice1**](/windows/desktop/api/directml/nn-directml-idmldevice1) | Stellt ein DirectML-Gerät dar, das zum Erstellen von Operatoren, Bindungstabellen, Befehlsaufzeichnungen und anderen Objekten verwendet wird. |
| [**IDMLDeviceChild**](/windows/win32/api/directml/nn-directml-idmldevicechild) | Eine Schnittstelle, die von allen -Objekten implementiert wird, die vom DirectML-Gerät erstellt wurden. |
| [**IDMLDispatchable**](/windows/desktop/api/directml/nn-directml-idmldispatchable) | Wird von -Objekten implementiert, die mithilfe von [IDMLCommandRecorder::RecordDispatch](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)in einer Befehlsliste für die Verteilung auf der GPU aufgezeichnet werden können. |
| [**IDMLObject**](/windows/desktop/api/directml/nn-directml-idmlobject) | Eine Schnittstelle, von der [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice) und [IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild) direkt erben (und alle anderen Schnittstellen indirekt). Folglich stellt sie Methoden bereit, die allen DirectML-Schnittstellen gemeinsam sind, insbesondere Methoden zum Zuordnen privater Daten und zum Kommentieren von Objektnamen. |
| [**IDMLOperator**](/windows/desktop/api/directml/nn-directml-idmloperator) | Stellt einen DirectML-Operator dar. |
| [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) | Stellt ein spezialisiertes -Objekt dar, dessen Zweck darin besteht, kompilierte Operatoren zu initialisieren. |
| [**IDMLPageable**](/windows/desktop/api/directml/nn-directml-idmlpageable) | Wird von -Objekten implementiert, die aus dem GPU-Speicher entfernt werden können und daher für [IDMLDevice::Evict](/windows/desktop/api/directml/nf-directml-idmldevice-evict) und [IDMLDevice::MakeResident](/windows/desktop/api/directml/nf-directml-idmldevice-makeresident)bereitgestellt werden können. |

## <a name="related-topics"></a>Zugehörige Themen

* [DirectML-Referenz](direct3d-directml-reference.md)
* [Core-Referenz](direct3d-12-core-reference.md)
* [Referenz für Direct3D 12](direct3d-12-reference.md)
