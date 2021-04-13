---
title: Systemmonitor. LoadSettings-Methode
description: Fügt dem System Monitor die Indikatoren in der HTML-Vorlagen Datei hinzu.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- LoadSettings-Methode (Sysmon)
- LoadSettings-Methode (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", LoadSettings-Methode
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
ms.openlocfilehash: 6e412ebfe97035c4847391a7cc9166cf512897bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391937"
---
# <a name="systemmonitorloadsettings-method"></a>Systemmonitor. LoadSettings-Methode

Fügt dem System Monitor die Indikatoren in der HTML-Vorlagen Datei hinzu.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Settingsfilename* \[ in\]
</dt> <dd>

HTML-Zeichenfolge, die die Zähler angibt, die dem System Monitor hinzugefügt werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um die aktuellen Leistungsindikatoren im System Monitor in einer HTML-Datei zu speichern, wenden Sie die Methode [**Systemmonitor. SaveAs**](systemmonitor-saveas.md) an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> </dl>

 

 





