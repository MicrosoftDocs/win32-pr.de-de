---
title: TaskService. Connect-Methode
description: Bei der Skripterstellung wird eine Verbindung mit einem Remote Computer hergestellt, und alle nachfolgenden Aufrufe dieser Schnittstelle werden einer Remote Sitzung zugeordnet.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Connect-Methode Taskplaner
- Connect-Methode Taskplaner, Task Service-Objekt
- Task Service-Objekt Taskplaner, Connect-Methode
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
ms.openlocfilehash: 1db5f13e20da825cbdaf45ae399279687f6ff4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949641"
---
# <a name="taskserviceconnect-method"></a>TaskService. Connect-Methode

Bei der Skripterstellung wird eine Verbindung mit einem Remote Computer hergestellt, und alle nachfolgenden Aufrufe dieser Schnittstelle werden einer Remote Sitzung zugeordnet. Wenn der Servername-Parameter leer ist, wird diese Methode auf dem lokalen Computer ausgeführt. Wenn die UserID nicht angegeben ist, wird das aktuelle Token verwendet.

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

*Servername* \[ in, optional\]
</dt> <dd>

Der Name des Computers, mit dem Sie eine Verbindung herstellen möchten. Wenn der Servername-Parameter leer ist, wird diese Methode auf dem lokalen Computer ausgeführt.

</dd> <dt>

*Benutzer* \[ in, optional\]
</dt> <dd>

Der Benutzername, der während der Verbindung mit dem Computer verwendet wird. Wenn der Benutzer nicht angegeben ist, wird das aktuelle Token verwendet.

</dd> <dt>

*Domäne* \[ in, optional\]
</dt> <dd>

Die Domäne des Benutzers, der im *Benutzer* Parameter angegeben ist.

</dd> <dt>

*Kennwort* \[ in, optional\]
</dt> <dd>

Das Kennwort, das zum Herstellen einer Verbindung mit dem Computer verwendet wird. Wenn der Benutzername und das Kennwort nicht angegeben sind, wird das aktuelle Token verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **TaskService. Connect** -Methode sollte aufgerufen werden, bevor eine der anderen [**Task Service**](taskservice.md) -Methoden aufgerufen wird.

Wenn die Verbindungsmethode fehlschlägt, können Sie den Fehler Bezeichner erfassen, um die Bedeutung des Fehlers zu ermitteln. In der folgenden Tabelle werden die Fehler Bezeichner und deren Beschreibungen aufgelistet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fehler Bezeichner</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x80070005</td>
<td>Der Zugriff auf die Verbindung mit dem Taskplaner-Dienst wird verweigert.</td>
</tr>
<tr class="even">
<td>0x80041315</td>
<td>Der Taskplaner-Dienst wird nicht ausgeführt.</td>
</tr>
<tr class="odd">
<td>0x8007000e</td>
<td>Die Anwendung verfügt nicht über genügend Arbeitsspeicher, um den Vorgang abzuschließen, oder der <em>Benutzer</em>, das <em>Kennwort</em>oder die <em>Domäne</em> hat mindestens einen NULL-Wert und einen nicht-NULL-Wert.</td>
</tr>
<tr class="even">
<td>53</td>
<td>Dieser Fehler wird in den folgenden Situationen zurückgegeben:
<ul>
<li>Der im <em>Server</em> Name-Parameter angegebene Computername ist nicht vorhanden.</li>
<li>Wenn Sie versuchen, eine Verbindung mit einem Windows Server 2003-oder Windows XP-Computer herzustellen, und auf dem Remote Computer die Firewallausnahme für Datei-und Druckerfreigabe nicht aktiviert ist oder der Remote Registrierungsdienst nicht ausgeführt wird.</li>
<li>Wenn Sie versuchen, eine Verbindung mit einem Windows Vista-Computer herzustellen, und auf dem Remote Computer nicht die Firewallausnahme für die Remote Verwaltung geplanter Tasks aktiviert ist und die Firewallausnahme für die Datei-und Druckerfreigabe aktiviert ist oder der Remote Registrierungsdienst nicht ausgeführt wird.</li>
</ul></td>
</tr>
<tr class="odd">
<td>50</td>
<td>Die Parameter " <em>User</em>", " <em>Password</em>" und " <em>Domain</em> " können nicht angegeben werden, wenn eine Verbindung mit einem Windows XP-oder Windows Server 2003-Remote Computer von einem Computer mit Windows Vista</td>
</tr>
</tbody>
</table>



 

Wenn Sie von Windows Vista aus eine Verbindung mit einem Windows Vista-Remote Computer herstellen möchten, müssen Sie die Firewallausnahme für die Remote Verwaltung geplanter Tasks auf dem Remote Computer zulassen. Um diese Ausnahme zuzulassen, klicken Sie auf Start, Systemsteuerung, Sicherheit, Programm durch die Windows-Firewall zulassen, und aktivieren Sie dann das Kontrollkästchen Remote Verwaltung geplanter Aufgaben. Klicken Sie dann im Dialogfeld Windows-Firewall-Einstellungen auf die Schaltfläche OK.

Wenn Sie von einem Windows Vista-Computer aus eine Verbindung mit einem Remote Computer mit Windows XP oder Windows Server 2003 herstellen, müssen Sie die Firewallausnahme für die Datei-und Druckerfreigabe auf dem Remote Computer zulassen. Klicken Sie zum zulassen dieser Ausnahme auf Start und auf Systemsteuerung, doppelklicken Sie auf Windows-Firewall, wählen Sie die Registerkarte Ausnahmen, und wählen Sie dann die Datei-und Druckerfreigabe Firewall-Ausnahme aus. Klicken Sie dann im Dialogfeld Windows-Firewall auf die Schaltfläche OK. Der Remote Registrierungsdienst muss auch auf dem Remote Computer ausgeführt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





