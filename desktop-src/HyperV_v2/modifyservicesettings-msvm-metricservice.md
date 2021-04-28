---
description: 'ModifyServiceSettings-Methode der Msvm_MetricService Klasse: Ändert die Einstellungsdaten für den Dienst.'
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: ModifyServiceSettings-Methode der Msvm_MetricService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 088aec001dd63de7344256fd9e114b6ff73e4425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112178"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a>ModifyServiceSettings-Methode der Msvm \_ MetricService-Klasse

Ändert die Einstellungsdaten für den Dienst.

## <a name="syntax"></a>Syntax


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SettingData* \[ In\]
</dt> <dd>

Enthält eine eingebettete Instanz der [**Msvm \_ MetricServiceSettingData-Klasse,**](msvm-metricservicesettingdata.md) die die geänderten Einstellungsdaten für den Dienst enthält.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.



| Rückgabecode/-wert                                                                                                                                                                | BESCHREIBUNG                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>                    | Erfolg.<br/>                                |
| <dl> <dt>**Überprüfte Methodenparameter – Auftrag gestartet**</dt> <dt>4096</dt> </dl> | Methodenparameter überprüft, Auftrag gestartet.<br/> |
| <dl> <dt>**Fehler**</dt> <dt>32768</dt> </dl>                                 | Fehler.<br/>                                 |
| <dl> <dt>**Zugriff verweigert**</dt> <dt>32769</dt> </dl>                          | Der Zugriff wurde verweigert.<br/>                          |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>32770</dt> </dl>                          | Wird nicht unterstützt.<br/>                          |
| <dl> <dt>**Der Status ist unbekannt**</dt> <dt>32771.</dt> </dl>                      | Der Status ist unbekannt.<br/>                      |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                | Time out.<br/>                               |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>32773</dt> </dl>                      | Ungültiger Parameter.<br/>                      |
| <dl> <dt>**System wird verwendet**</dt> <dt>32774</dt> </dl>                       | Das System wird verwendet.<br/>                       |
| <dl> <dt>**Ungültiger Zustand für diesen Vorgang**</dt> <dt>32775</dt> </dl>       | Ungültiger Zustand für diesen Vorgang.<br/>       |
| <dl> <dt>**Falscher Datentyp**</dt> <dt>32776</dt> </dl>                    | Falscher Datentyp.<br/>                    |
| <dl> <dt>**System ist nicht verfügbar**</dt> <dt>32777</dt> </dl>                | Das System ist nicht verfügbar.<br/>                |
| <dl> <dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt> </dl>                          | Nicht genügend Arbeitsspeicher.<br/>                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 8 \[ Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2012-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

