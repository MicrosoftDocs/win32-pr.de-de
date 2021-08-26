---
title: TaskService. Verbinden-Methode
description: Für die Skripterstellung stellt eine Verbindung mit einem Remotecomputer her und ordnet alle nachfolgenden Aufrufe dieser Schnittstelle einer Remotesitzung zu.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Verbinden-Methode Taskplaner
- Verbinden-Methode Taskplaner , TaskService-Objekt
- TaskService-Objekt Taskplaner , Verbinden-Methode
topic_type:
- apiref
api_name:
- TaskService.Connect
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e8d9491fb66d8e79b18efed363d4eb4f21bc6c5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472346"
---
# <a name="taskserviceconnect-method"></a>TaskService. Verbinden-Methode

Für die Skripterstellung stellt eine Verbindung mit einem Remotecomputer her und ordnet alle nachfolgenden Aufrufe dieser Schnittstelle einer Remotesitzung zu. Wenn der serverName-Parameter leer ist, wird diese Methode auf dem lokalen Computer ausgeführt. Wenn die userId nicht angegeben ist, wird das aktuelle Token verwendet.

## <a name="syntax"></a>Syntax


```VB
TaskService.Connect( _
  [ ByVal serverName ], _
  [ ByVal user ], _
  [ ByVal domain ], _
  [ ByVal password ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*serverName* \[ in, optional\]
</dt> <dd>

Der Name des Computers, mit dem Sie eine Verbindung herstellen möchten. Wenn der serverName-Parameter leer ist, wird diese Methode auf dem lokalen Computer ausgeführt.

</dd> <dt>

*Benutzer* \[ in, optional\]
</dt> <dd>

Der Benutzername, der während der Verbindung mit dem Computer verwendet wird. Wenn der Benutzer nicht angegeben ist, wird das aktuelle Token verwendet.

</dd> <dt>

*Domäne* \[ in, optional\]
</dt> <dd>

Die Domäne des Im Benutzerparameters angegebenen *Benutzers.*

</dd> <dt>

*Kennwort* \[ in, optional\]
</dt> <dd>

Das Kennwort, das zum Herstellen einer Verbindung mit dem Computer verwendet wird. Wenn Benutzername und Kennwort nicht angegeben sind, wird das aktuelle Token verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **TaskService.Verbinden-Methode** sollte aufgerufen werden, bevor eine der anderen [**TaskService-Methoden**](taskservice.md) aufgerufen wird.

Wenn die Verbinden-Methode fehlschlägt, können Sie den Fehlerbezeichner erfassen, um die Bedeutung des Fehlers zu ermitteln. In der folgenden Tabelle sind die Fehlerbezeichner und ihre Beschreibungen aufgeführt.




| Fehlerbezeichner | BESCHREIBUNG | 
|------------------|-------------|
| 0x80070005 | Der Zugriff zum Herstellen einer Verbindung mit dem Taskplaner Dienst wird verweigert. | 
| 0x80041315 | Der Taskplaner Dienst wird nicht ausgeführt. | 
| 0x8007000e | Die Anwendung verfügt nicht über genügend Arbeitsspeicher, um den Vorgang abzuschließen, oder der <em>Benutzer,</em> <em>das Kennwort</em>oder die <em>Domäne</em> weist mindestens einen NULL- und einen Wert ungleich NULL auf. | 
| 53 | Dieser Fehler wird in den folgenden Situationen zurückgegeben:<ul><li>Der im <em>serverName-Parameter</em> angegebene Computername ist nicht vorhanden.</li><li>Wenn Sie versuchen, eine Verbindung mit einem Windows Server 2003- oder Windows XP-Computer herzustellen und auf dem Remotecomputer die Firewallausnahme datei- und druckerfreigabe nicht aktiviert ist oder der Remoteregistrierungsdienst nicht ausgeführt wird.</li><li>Wenn Sie versuchen, eine Verbindung mit einem Windows Vista-Computer herzustellen, und auf dem Remotecomputer ist die Firewallausnahme für die Verwaltung geplanter Remoteaufgaben nicht aktiviert und die Firewallausnahme datei- und druckerfreigabe aktiviert, oder der Remoteregistrierungsdienst wird nicht ausgeführt.</li></ul> | 
| 50 | Die <em>Benutzer-,</em> <em>Kennwort-</em>oder <em>Domänenparameter</em> können nicht angegeben werden, wenn eine Verbindung mit einem Remotecomputer Windows XP oder Windows Server 2003 von einem computer Windows Vista hergestellt wird. | 




 

Wenn Sie von einem Windows Vista aus eine Verbindung mit einem Remotecomputer Windows Vista herstellen möchten, müssen Sie die Remote-Firewallausnahme für die Verwaltung geplanter Tasks auf dem Remotecomputer zulassen. Um diese Ausnahme zuzulassen, klicken Sie auf Start, Systemsteuerung, Sicherheit, Programm über Windows Firewall zulassen, und aktivieren Sie dann das Kontrollkästchen Verwaltung geplanter Remoteaufgaben. Klicken Sie dann im Dialogfeld Windows Firewall Einstellungen auf ok.

Wenn Sie von einem computer Windows Vista eine Verbindung mit einem Remotecomputer Windows XP oder Windows Server 2003 herstellen, müssen Sie die Firewallausnahme datei- und druckerfreigabe auf dem Remotecomputer zulassen. Um diese Ausnahme zuzulassen, klicken Sie auf Start, Systemsteuerung, doppelklicken Sie auf Windows Firewall, wählen Sie die Registerkarte Ausnahmen aus, und wählen Sie dann die Firewallausnahme Datei- und Druckerfreigabe aus. Klicken Sie dann im Dialogfeld Firewall Windows auf die Schaltfläche OK. Der Remoteregistrierungsdienst muss auch auf dem Remotecomputer ausgeführt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





