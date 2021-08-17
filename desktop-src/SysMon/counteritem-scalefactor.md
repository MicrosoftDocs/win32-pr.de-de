---
title: CounterItem.ScaleFactor-Eigenschaft
description: Ruft den Skalierungsfaktor ab, der zum Graphen des Indikatorwerts verwendet wird, oder legt diesen fest.
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- ScaleFactor-Eigenschaft SysMon
- ScaleFactor-Eigenschaft SysMon , CounterItem-Klasse
- CounterItem-Klasse SysMon , ScaleFactor-Eigenschaft
topic_type:
- apiref
api_name:
- CounterItem.ScaleFactor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794cd84dd62518cc3089b8644f41b5545aeaf547b275c703a4cb87f5fec2b4a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883664"
---
# <a name="counteritemscalefactor-property"></a>CounterItem.ScaleFactor-Eigenschaft

Ruft den Skalierungsfaktor ab, der zum Graphen des Indikatorwerts verwendet wird, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a>Eigenschaftswert

Skalierungsfaktor, der zum Anzeigen der diagrammierten Indikatorwerte verwendet wird. Gültige Werte liegen zwischen -9 und 9 (die Werte entsprechen 0,000000001 bis 1000000000,0).

**Vor Windows Vista:** Gültige Werte liegen zwischen -7 und 7 (die Werte entsprechen 0,0000001 bis 1000000,0).

## <a name="remarks"></a>Hinweise

Legen Sie diese Eigenschaft nur fest, wenn Sie den Standardskalfaktor des Zählers ändern möchten (jeder Leistungsindikator definiert einen eigenen Skalierungsfaktor). Der Wert dieser Eigenschaft wird auf Integer.MaxValue festgelegt, wenn der Zähler seinen Standardskalierenfaktor verwendet, um die Werte zu graphieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**SystemMonitor.ScaleToFit**](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





