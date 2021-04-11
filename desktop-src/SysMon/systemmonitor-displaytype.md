---
title: Systemmonitor. Display Type (Eigenschaft)
description: Ruft den Diagrammtyp ab, der zum Diagramm der Leistungs Indikatorendaten verwendet wird, oder legt ihn fest.
ms.assetid: a04545b1-920e-4fb3-909b-dc47e1374629
keywords:
- DisplayType-Eigenschaft (Sysmon)
- DisplayType-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse sysmon, Display Type (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.DisplayType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c0e96ff0da57ef9e5f580063dc4f693d672e15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103833"
---
# <a name="systemmonitordisplaytype-property"></a>Systemmonitor. Display Type (Eigenschaft)

Ruft den Diagrammtyp ab, der zum Diagramm der Leistungs Indikatorendaten verwendet wird, oder legt ihn fest.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property DisplayType As DisplayTypeConstants
```



## <a name="property-value"></a>Eigenschaftswert

Der Diagrammtyp, der verwendet wird, um die Leistungsdaten anzuzeigen. Mögliche Werte finden Sie unter [**displaytypekonstanten**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).

## <a name="exceptions"></a>Ausnahmen



| Ausnahmetyp               | Bedingung                                         |
|------------------------------|---------------------------------------------------|
| **System.ArgumentException** | Der angegebene Diagramm-oder Berichts Wert ist ungültig. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> </dl>

 

 





