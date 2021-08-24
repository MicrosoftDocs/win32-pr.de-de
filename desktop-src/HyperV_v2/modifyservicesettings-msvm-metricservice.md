---
description: 'ModifyServiceSettings-Methode der Msvm_MetricService-Klasse: Ändert die Einstellungsdaten für den Dienst.'
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: ModifyServiceSettings-Methode der Msvm_MetricService-Klasse
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
ms.openlocfilehash: 51af98d230433687d9a16cb3ab858fd746b7ff1ca4e17eaf0b36cce16e92c875
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693910"
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

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.



| Rückgabecode/-wert                                                                                                                                                                | Beschreibung                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>                    | Erfolg.<br/>                                |
| <dl> <dt>**Methodenparameter überprüft**</dt> – Auftrag gestartet <dt>4096</dt> </dl> | Methodenparameter überprüft, Auftrag gestartet.<br/> |
| <dl> <dt>**Fehler**</dt> <dt>32768</dt> </dl>                                 | Fehler.<br/>                                 |
| <dl> <dt>**Zugriff verweigert**</dt> <dt>32769</dt> </dl>                          | Zugriff verweigert:<br/>                          |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>32770</dt> </dl>                          | Wird nicht unterstützt.<br/>                          |
| <dl> <dt>**Status ist unbekannt**</dt> <dt>32771</dt> </dl>                      | Der Status ist unbekannt.<br/>                      |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                | Time-Out.<br/>                               |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>32773</dt> </dl>                      | Ungültiger Parameter.<br/>                      |
| <dl> <dt>**System wird verwendet**</dt> <dt>32774</dt> </dl>                       | Das System wird verwendet.<br/>                       |
| <dl> <dt>**Ungültiger Zustand für diesen Vorgang**</dt> <dt>32775</dt> </dl>       | Ungültiger Zustand für diesen Vorgang.<br/>       |
| <dl> <dt>**Falscher Datentyp**</dt> <dt>32776</dt> </dl>                    | Falscher Datentyp.<br/>                    |
| <dl> <dt>**System ist nicht verfügbar**</dt> <dt>32777</dt> </dl>                | Das System ist nicht verfügbar.<br/>                |
| <dl> <dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt> </dl>                          | Nicht genügend Arbeitsspeicher.<br/>                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

