---
title: SystemMonitor.ScaleToFit-Methode
description: Skalieren Sie Indikatorwerte so, dass sie in das Diagramm passen.
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- ScaleToFit-Methode SysMon
- ScaleToFit-Methode SysMon , SystemMonitor-Objekt
- SystemMonitor-Objekt SysMon , ScaleToFit-Methode
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
ms.openlocfilehash: 1cddb539f8c8d2c6c78f70d96d82da171e11a62afbeaa31d1a011c74c2cb096d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118881514"
---
# <a name="systemmonitorscaletofit-method"></a>SystemMonitor.ScaleToFit-Methode

Skalieren Sie Indikatorwerte so, dass sie in das Diagramm passen.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*selectedCountersOnly* \[ In\]
</dt> <dd>

True, um nur die ausgewählten Leistungsindikatoren zu skalieren; andernfalls FALSE, um alle Leistungsindikatoren zu skalieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode löscht die Diagrammansicht. SYSMON verwendet dann den für jeden Indikator angegebenen Skalierungsfaktor, um das Diagramm neu zu zeichnen, wenn es sich bei der Datenquelle um eine Protokolldatei handelt, oder beginnt mit dem Graphen neuer Indikatorwerte, wenn es sich bei der Datenquelle um eine Echtzeitaktivität handelt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**CounterItem.ScaleFactor**](counteritem-scalefactor.md)
</dt> <dt>

[**CounterItem.Selected**](counteritem-selected.md)
</dt> </dl>

 

 





