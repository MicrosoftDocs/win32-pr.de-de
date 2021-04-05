---
description: Ändert die Einstellungsdaten für den Dienst.
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Modifyservicesettings-Methode der Msvm_MetricService-Klasse
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
ms.openlocfilehash: b680f5f46d99d46f99094e05db653083fd7ae952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752224"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a>Modifyservicesettings-Methode der MSVM \_ metricservice-Klasse

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

*SettingData* \[ in\]
</dt> <dd>

Enthält eine eingebettete Instanz der [**MSVM \_ metricservicesettingdata**](msvm-metricservicesettingdata.md) -Klasse, die die geänderten Einstellungsdaten für den Dienst enthält.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.



| Rückgabecode/-wert                                                                                                                                                                | BESCHREIBUNG                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>                    | Erfolg.<br/>                                |
| <dl> <dt>**Methoden Parameter aktiviert-Auftrag gestartet**</dt> <dt>4096</dt> </dl> | Methoden Parameter aktiviert, Auftrag wurde gestartet.<br/> |
| <dl> <dt></dt> Fehler <dt>32768</dt> </dl>                                 | Fehler.<br/>                                 |
| <dl> <dt>**Zugriff verweigert**</dt> <dt>32769</dt> </dl>                          | Zugriff verweigert.<br/>                          |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>32770</dt> </dl>                          | Wird nicht unterstützt.<br/>                          |
| <dl> <dt>**Status ist unbekannt**</dt> <dt>32771</dt> </dl>                      | Der Status ist unbekannt.<br/>                      |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                | Timeout.<br/>                               |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>32773</dt> </dl>                      | Ungültiger Parameter.<br/>                      |
| <dl> <dt>**System wird verwendet**</dt> <dt>32774</dt> </dl>                       | Das System wird verwendet.<br/>                       |
| <dl> <dt>**Ungültiger Status für diesen Vorgang**</dt> <dt>32775</dt> </dl>       | Ungültiger Status für diesen Vorgang.<br/>       |
| <dl> <dt>**Falscher Datentyp**</dt> <dt>32776</dt> </dl>                    | Falscher Datentyp.<br/>                    |
| <dl> <dt>**System ist nicht verfügbar**</dt> <dt>32777</dt> </dl>                | Das System ist nicht verfügbar.<br/>                |
| <dl> <dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt> </dl>                          | Nicht genügend Arbeitsspeicher.<br/>                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ metricservice**](msvm-metricservice.md)
</dt> </dl>

 

