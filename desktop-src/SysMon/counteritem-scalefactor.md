---
title: Count. scalefactor (Eigenschaft)
description: Ruft den Skalierungsfaktor ab, mit dem der indikatorenwert dargestellt wird, oder legt ihn fest
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- Scalefactor-Eigenschaft (Sysmon)
- Scalefactor-Eigenschaft "sysmon", "ratteritem"-Klasse
- Namteritem Class sysmon, scalefactor-Eigenschaft
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
ms.openlocfilehash: ed9a04df634fe54c82230ade679afb3259519173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340797"
---
# <a name="counteritemscalefactor-property"></a>Count. scalefactor (Eigenschaft)

Ruft den Skalierungsfaktor ab, mit dem der indikatorenwert dargestellt wird, oder legt ihn fest

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a>Eigenschaftswert

Der Skalierungsfaktor, der beim Anzeigen der dargestellten Werte für Werte verwendet wird. Gültige Werte liegen im Bereich von-9 bis 9 (die Werte entsprechen 0,000000001-100000000,0).

**Vor Windows Vista:** Gültige Werte reichen von-7 bis 7 (die Werte entsprechen 0,0000001-1000000,0).

## <a name="remarks"></a>Bemerkungen

Legen Sie diese Eigenschaft nur fest, wenn Sie den standardmäßigen Skalierungsfaktor des Zählers ändern möchten (jeder Counter definiert seinen eigenen Skalierungsfaktor). Der Wert dieser Eigenschaft wird auf "Integer. MaxValue" festgelegt, wenn der Leistungs Besatz den Standard Skalierungsfaktor verwendet, um die Werte zu Graphen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ratteritem**](counteritem.md)
</dt> <dt>

[**Systemmonitor. scaledefit**](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





