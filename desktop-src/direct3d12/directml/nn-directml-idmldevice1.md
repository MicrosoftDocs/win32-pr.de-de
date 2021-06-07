---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: Stellt ein DirectML-Gerät dar, das zum Erstellen von Operatoren, Bindungstabellen, Befehlsaufzeichnungen und anderen Objekten verwendet wird.
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
ms.openlocfilehash: 7a10cf2c9fe683775d163c7b5cb0e30fe07de08f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417178"
---
# <a name="idmldevice1-interface-directmlh"></a>IDMLDevice1-Schnittstelle (directml.h)

Stellt ein DirectML-Gerät dar, das zum Erstellen von Operatoren, Bindungstabellen, Befehlsaufzeichnungen und anderen Objekten verwendet wird. Die **IDMLDevice1-Schnittstelle** erbt von [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).

Ein DirectML-Gerät ist immer genau einem zugrunde liegenden Direct3D 12-Gerät zugeordnet. Alle vom DirectML-Gerät erstellten Objekte behalten einen starken Verweis auf ihr übergeordnetes Gerät bei. Im Gegensatz zum Direct3D 12-Gerät ist das DML-Gerät kein Singleton. Daher ist es möglich, mehrere DirectML-Geräte über dasselbe Direct3D 12-Gerät zu erstellen. Dies wird jedoch nicht empfohlen, da das DirectML-Gerät über keinen veränderlichen Zustand verfügt, sodass es wenig Vorteile bietet, mehrere DML-Geräte über dasselbe Direct3D 12-Gerät zu erstellen.

Dieses Objekt ist threadsicher.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="availability"></a>Verfügbarkeit
Diese API wurde in der DirectML-Version `1.1.0` eingeführt.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
**Zielplattform:** Windows


## <a name="inheritance"></a>Vererbung


Die IDMLDevice1-Schnittstelle erbt von der IDMLDevice-Schnittstelle.



## <a name="methods"></a>Methoden

<p>Die <b>IDMLDevice1-Schnittstelle</b> verfügt über diese Methoden.</p>

| Methode | BESCHREIBUNG |
| ---- |:---- |
| [IDMLDevice1::CompileGraph](../directml/nf-directml-idmldevice1-compilegraph.md) | Kompiliert ein Diagramm von DirectML-Operatoren in ein Objekt, das an die GPU gesendet werden kann. |


## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | directml.h |

## <a name="see-also"></a>Siehe auch

[IDMLDevice-Schnittstelle](/windows/win32/api/directml/nn-directml-idmldevice)