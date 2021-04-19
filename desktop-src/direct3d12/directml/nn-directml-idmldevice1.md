---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: Stellt ein directml-Gerät dar, das zum Erstellen von Operatoren, Bindungs Tabellen, Befehls Recorder und anderen Objekten verwendet wird.
helpviewer_keywords:
- IDMLDevice1
- IDMLDevice1 interface
- IDMLDevice1 interface
- described
- direct3d12.idmldevice1
- directml/IDMLDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1
- directml/IDMLDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.h
api_name:
- IDMLDevice1
ms.openlocfilehash: a23d6ec4299a2aa3ca7e9f6873167412d094af8d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106361746"
---
# <a name="idmldevice1-interface-directmlh"></a>IDMLDevice1-Schnittstelle (directml. h)

Stellt ein directml-Gerät dar, das zum Erstellen von Operatoren, Bindungs Tabellen, Befehls Recorder und anderen Objekten verwendet wird. Die **IDMLDevice1** -Schnittstelle erbt von [idmldevice](/windows/win32/api/directml/nn-directml-idmldevice).

Ein directml-Gerät ist immer genau einem zugrunde liegenden Direct3D 12-Gerät zugeordnet. Alle Objekte, die vom directml-Gerät erstellt wurden, behalten einen starken Verweis auf das übergeordnete Gerät bei. Im Gegensatz zum Direct3D 12-Gerät ist das DML-Gerät kein Singleton. Daher ist es möglich, mehrere directml-Geräte über das gleiche Direct3D 12-Gerät zu erstellen. Dies wird jedoch nicht empfohlen, da das directml-Gerät keinen änderbaren Zustand aufweist. es gibt also wenig Vorteil beim Erstellen mehrerer DML-Geräte über dasselbe Direct3D 12-Gerät.

Dieses Objekt ist Thread sicher.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="availability"></a>Verfügbarkeit
Diese API wurde in der directml-Version eingeführt `1.1.0` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
**Zielplattform**: Windows


## <a name="inheritance"></a>Vererbung


Die IDMLDevice1-Schnittstelle erbt von der idmldevice-Schnittstelle.



## <a name="methods"></a>Methoden

<p>Die <b>IDMLDevice1</b> -Schnittstelle verfügt über diese Methoden.</p>

| Methode | BESCHREIBUNG |
| ---- |:---- |
| [IDMLDevice1:: compilegraph](../directml/nf-directml-idmldevice1-compilegraph.md) | Kompiliert ein Diagramm von directml-Operatoren in ein Objekt, das an die GPU gesendet werden kann. |


## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | directml. h |

## <a name="see-also"></a>Siehe auch

[Idmldevice-Schnittstelle](/windows/win32/api/directml/nn-directml-idmldevice)