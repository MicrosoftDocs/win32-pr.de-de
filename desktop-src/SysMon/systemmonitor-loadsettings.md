---
title: SystemMonitor.LoadSettings-Methode
description: Fügt dem Systemmonitor die Leistungsindikatoren in der HTML-Vorlagendatei hinzu.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- LoadSettings-Methode SysMon
- LoadSettings-Methode SysMon , SystemMonitor-Objekt
- SystemMonitor-Objekt SysMon , LoadSettings-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.LoadSettings
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 387bf2e42475d27f5440afb3fa0b945c910b3ac3bad610495936cd3a4a900bbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882325"
---
# <a name="systemmonitorloadsettings-method"></a>SystemMonitor.LoadSettings-Methode

Fügt dem Systemmonitor die Leistungsindikatoren in der HTML-Vorlagendatei hinzu.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SettingsFileName* \[ In\]
</dt> <dd>

HTML-Zeichenfolge, die die Leistungsindikatoren angibt, die dem Systemmonitor hinzugefügt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um die aktuellen Leistungsindikatoren im Systemmonitor in einer HTML-Datei zu speichern, rufen Sie die [**SystemMonitor.SaveAs-Methode**](systemmonitor-saveas.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





