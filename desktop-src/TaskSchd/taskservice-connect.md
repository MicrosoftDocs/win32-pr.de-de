---
title: TaskService. Verbinden-Methode
description: Für die Skripterstellung stellt eine Verbindung mit einem Remotecomputer her und ordnet alle nachfolgenden Aufrufe dieser Schnittstelle einer Remotesitzung zu.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Verbinden-Methode Taskplaner
- Verbinden Methode Taskplaner , TaskService-Objekt
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
ms.openlocfilehash: d4da8fb2aed018eab9880ab6c8a6bed310e6d89bb293d52efc5d6ac6d8baf190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059738"
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

Wenn die Verbinden-Methode fehlschlägt, können Sie den Fehlerbezeichner erfassen, um die Bedeutung des Fehlers zu ermitteln. In der folgenden Tabelle sind die Fehlerbezeichner und deren Beschreibungen aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fehlerbezeichner</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x80070005</td>
<td>Der Zugriff zum Herstellen einer Verbindung mit dem Taskplaner Dienst wird verweigert.</td>
</tr>
<tr class="even">
<td>0x80041315</td>
<td>Der Taskplaner Dienst wird nicht ausgeführt.</td>
</tr>
<tr class="odd">
<td>0x8007000e</td>
<td>Die Anwendung verfügt nicht über genügend Arbeitsspeicher, um den Vorgang abzuschließen, oder der <em>Benutzer,</em> <em>das Kennwort</em>oder die <em>Domäne</em> weist mindestens einen NULL- und einen Wert ungleich NULL auf.</td>
</tr>
<tr class="even">
<td>53</td>
<td>Dieser Fehler wird in den folgenden Situationen zurückgegeben:
<ul>
<li>Der im <em>serverName-Parameter</em> angegebene Computername ist nicht vorhanden.</li>
<li>Wenn Sie versuchen, eine Verbindung mit einem Windows Server 2003- oder Windows XP-Computer herzustellen, und auf dem Remotecomputer ist die Firewallausnahme Datei- und Druckerfreigabe nicht aktiviert, oder der Remoteregistrierungsdienst wird nicht ausgeführt.</li>
<li>Wenn Sie versuchen, eine Verbindung mit einem Windows Vista-Computer herzustellen, und auf dem Remotecomputer ist die Firewallausnahme für die Verwaltung geplanter Remoteaufgaben nicht aktiviert und die Firewallausnahme datei- und druckerfreigabe aktiviert, oder der Remoteregistrierungsdienst wird nicht ausgeführt.</li>
</ul></td>
</tr>
<tr class="odd">
<td>50</td>
<td>Die <em>Benutzer-,</em> <em>Kennwort-</em>oder <em>Domänenparameter</em> können nicht angegeben werden, wenn eine Verbindung mit einem Remotecomputer Windows XP oder Windows Server 2003 von einem computer Windows Vista hergestellt wird.</td>
</tr>
</tbody>
</table>



 

Wenn Sie von einem Windows Vista aus eine Verbindung mit einem Remotecomputer Windows Vista herstellen möchten, müssen Sie die Remote-Firewallausnahme für die Verwaltung geplanter Tasks auf dem Remotecomputer zulassen. Um diese Ausnahme zuzulassen, klicken Sie auf Start, Systemsteuerung, Sicherheit, Programm über Windows Firewall zulassen, und aktivieren Sie dann das Kontrollkästchen Verwaltung geplanter Remoteaufgaben. Klicken Sie dann im Dialogfeld Windows Firewall Einstellungen auf die Schaltfläche OK.

Wenn Sie von einem computer Windows Vista eine Verbindung mit einem Remotecomputer Windows XP oder Windows Server 2003 herstellen, müssen Sie die Firewallausnahme datei- und druckerfreigabe auf dem Remotecomputer zulassen. Um diese Ausnahme zuzulassen, klicken Sie auf Start, Systemsteuerung doppelklicken Sie auf Windows Firewall, wählen Sie die Registerkarte Ausnahmen aus, und wählen Sie dann die Firewallausnahme Datei- und Druckerfreigabe aus. Klicken Sie dann im Dialogfeld Windows Firewall auf die Schaltfläche OK. Der Remoteregistrierungsdienst muss auch auf dem Remotecomputer ausgeführt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





