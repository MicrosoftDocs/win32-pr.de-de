---
title: System Monitor. scaledefit-Methode
description: Skalierungs Wert Werte, die in das Diagramm passen.
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- Scaledefit-Methode (Sysmon)
- Scaledefit-Methode (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", scaledefit-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.ScaleToFit
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1e481dd44c441ea9e2dd44f2e63a06539da74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741112"
---
# <a name="systemmonitorscaletofit-method"></a>System Monitor. scaledefit-Methode

Skalierungs Wert Werte, die in das Diagramm passen.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*selectedcountersonly* \[ in\]
</dt> <dd>

True, wenn nur die ausgewählten Indikatoren skaliert werden sollen. andernfalls false, um alle Indikatoren zu skalieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode wird die Diagramm Ansicht gelöscht. Sysmon verwendet dann den für jeden Zählers angegebenen Skalierungsfaktor, um das Diagramm neu zu zeichnen, wenn es sich bei der Datenquelle um eine Protokolldatei handelt, oder um neue Werte zu erstellen, wenn die Datenquelle eine echt Zeit Aktivität ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> <dt>

[**"Count. scalefactor"**](counteritem-scalefactor.md)
</dt> <dt>

[**"Zählelement. ausgewählt"**](counteritem-selected.md)
</dt> </dl>

 

 





