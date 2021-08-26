---
description: Wird verwendet, um einzelne Teile einer Anwendung in einer gesperrten Umgebung zu schützen. Sie kann bei der Installation von Dateien, Registrierungsschlüsseln und erstellten Ordnern verwendet werden.
ms.assetid: 7c20e211-7704-49c2-a0c5-aaa695a09764
title: LockPermissions-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6724f9559f8bf4b5c0aac4581dab6ad7496e2c0e8e023636e621214760c26c99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043140"
---
# <a name="lockpermissions-table"></a>LockPermissions-Tabelle

Die LockPermissions-Tabelle wird verwendet, um einzelne Teile einer Anwendung in einer gesperrten Umgebung zu schützen. Sie kann bei der Installation von Dateien, Registrierungsschlüsseln und erstellten Ordnern verwendet werden.

Ein Paket, das für die Installation in Windows Server 2008 R2 oder Windows 7 vorgesehen ist, sollte die [MsiLockPermissionsEx-Tabelle](msilockpermissionsex-table.md) anstelle der LockPermissions-Tabelle verwenden. Windows Installerversionen vor Windows Installer 5.0 ignorieren die MsiLockPermissionsEx-Tabelle. Windows Installer 5.0 kann ein Paket installieren, das die LockPermissions-Tabelle enthält. Ab Windows Installer 5.0 schlägt die Installation eines Pakets fehl, das sowohl die MsiLockPermissionsEx-Tabelle als auch die LockPermissions-Tabelle enthält, und gibt die Fehlermeldung 1941 Windows Installer zurück.

Die LockPermissions-Tabelle enthält die folgenden Spalten.



| Spalte     | Typ                               | Key | Nullwerte zulässig |
|------------|------------------------------------|-----|----------|
| LockObject | [Identifier](identifier.md)       | J   | N        |
| Tabelle      | [Text](text.md)                   | J   | N        |
| Domain     | [Formatiert](formatted.md)         | J   | J        |
| Benutzer       | [Formatiert](formatted.md)         | J   | N        |
| Berechtigung | [DoubleInteger](doubleinteger.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

Diese Spalte und die Spalte Tabelle geben zusammen die Datei, das Verzeichnis oder den Registrierungsschlüssel an, die gesichert werden soll. Die LockObject-Spalte ist ein Fremdschlüssel, der auf den Primärschlüssel der tabelle verweist, die von der Table -Spalte angegeben wird.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabelle
</dt> <dd>

Diese Spalte und die LockObject-Spalte geben die Datei, das Verzeichnis oder den Registrierungsschlüssel an, die gesichert werden soll. Geben Sie in der Spalte Tabelle den Namen File, Registry oder CreateFolder ein, um ein LockObject anzugeben, das in der Dateitabelle, Registrierungstabelle oder [CreateFolder-Tabelle aufgeführt ist.](createfolder-table.md) [](file-table.md) [](registry-table.md)

</dd> <dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Domäne
</dt> <dd>

Die Spalte, die die Domäne des Benutzers identifiziert, für die Berechtigungen festgelegt werden sollen. Dies ist der Name eines eigenständigen Computers oder eines Domänennamens. Der Spaltendatentyp ist [Formatiert,](formatted.md)und Sie können die Zeichenfolge %USERDOMAIN in diesem Feld verwenden, um den Wert der USERDOMAIN-Umgebungsvariablen für die \[ \] aktuelle Domäne zu erhalten. Um eine andere Domäne zu erhalten, muss benutzerdefinierte [Aktionen verwendet werden.](custom-actions.md) Weitere Informationen finden Sie in der Tabelle für benutzerdefinierte Aktionen.

</dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>Benutzer
</dt> <dd>

Die Spalte, die den lokalisierten Namen des Benutzers identifiziert, für den Berechtigungen festgelegt werden sollen. Dieser Name muss sich auf dem Computer oder der Domäne befinden. Die Installation schlägt fehl, wenn der Computer oder Domänencontroller die Kombination aus Domäne und Benutzer nicht erkennt oder wenn die Sicherheits-ID (SID) des Benutzers nicht abgerufen werden kann. Für ein einzelnes LockObject können mehrere Benutzer angegeben werden.

Die allgemeinen Benutzernamen "Everyone" und "Administrators" können auf Englisch eingegeben werden und werden bekannten SIDs zugeordnet. LocalSystem erhält vollständige Kontrolle über alle Sicherheitsbeschreibungen, die über die LockPermissions-Tabelle erstellt werden. Sie können die [**ComputerName-Eigenschaft,**](computername.md) [**logonUser-Eigenschaft**](logonuser.md) oder [**USERNAME-Eigenschaft**](username.md) in diesem Feld verwenden, um den aktuellen Benutzer zu erhalten. Eine benutzerdefinierte Aktion ist erforderlich, um den lokalisierten Namen eines anderen Benutzers oder einer Gruppe ein eingaben zu können.

Sie können mehrere Datensätze mit identischen LockObject- und Table-Einträgen (aber unterschiedlichen Benutzereinträgen) verwenden, um Zugriffssteuerungslisten für mehrere Benutzer anzugeben.

</dd> <dt>

<span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Berechtigung
</dt> <dd>

Die Spalte, die die ganzzahlige Beschreibung von Systemberechtigungen identifiziert. Im Folgenden finden Sie die am häufigsten verwendeten Werte (eine vollständige Liste ist in Winnt.h vorhanden).



| Berechtigung                                                              | BESCHREIBUNG                     |
|------------------------------------------------------------------------|---------------------------------|
| GENERIC \_ ALL<br/> 0X10000000<br/> 268435456<br/>     | Lese-, Schreib- und Ausführungszugriff |
| GENERIC \_ EXECUTE<br/> 0X20000000<br/> 536870912<br/> | Ausführen des Zugriffs                  |
| GENERISCHER \_ SCHREIBZUGRIFF<br/> 0X40000000<br/> 1073741824<br/>  | Schreibzugriff                    |



 

Generic READ kann nicht \_ in der Spalte Berechtigung angegeben werden. Bei diesem Versuch ist ein Fehler zu sehen. Stattdessen müssen Sie einen Wert wie KEY READ oder \_ FILE \_ GENERIC READ \_ angeben.

Der in dieser Spalte eingegebene NULL-Wert ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [Aktionen InstallFiles,](installfiles-action.md) [WriteRegistryValues](writeregistryvalues-action.md)und [CreateFolders](createfolders-action.md) [*in*](s-gly.md) Sequenztabellen verarbeiten die Informationen in dieser Tabelle. Informationen zur Verwendung von *Sequenztabellen finden* Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

Die Berechtigung kann nur in der LockPermissions-Tabelle für Benutzer festgelegt werden, die bereits auf dem Computer oder in der Domäne vorhanden sind. Der Versuch, Berechtigungen für einen unbekannten Benutzer zu erstellen, führt zu einem Fehler bei der Installation, auch wenn dieses Benutzerkonto während der Installation durch eine verzögerte benutzerdefinierte Aktion erstellt wird.

Es wird empfohlen, die lokale Gruppe des Systemadministrators in allen Zugriffssteuerungslisten (Access Control Lists, ACL) zu enthalten. Dadurch wird sichergestellt, dass der Systemadministrator auf Objekte zugreifen und diese verwalten kann.

Jede Datei, jeder Registrierungsschlüssel oder jedes Verzeichnis, die in der LockPermissions-Tabelle aufgeführt sind, erhält eine explizite Sicherheitsbeschreibung, unabhängig davon, ob sie ein vorhandenes Objekt ersetzt oder nicht. Der Windows Installer versucht, die Sicherheit für Objekte zu gewährleisten, die bereits im System vorhanden sind. Wenn ein Objekt nicht in der LockPermissions-Tabelle aufgeführt ist und ein vorhandenes Objekt ersetzt, ruft die Ersetzung die Sicherheitseinstellungen des Objekts ab, das ersetzt wird.

Wenn ein Objekt nicht in der LockPermissions-Tabelle aufgeführt ist und kein vorhandenes Objekt ersetzt, erhält es keinen expliziten Sicherheitsdeskriptor. Der Zugriff auf das neue Objekt basiert auf den Attributen des übergeordneten Objekts oder Containerobjekts. Wenn ein Objekt nicht in der Tabelle aufgeführt ist und ein Objekt ohne expliziten Sicherheitsdeskriptor ersetzt, basiert der Zugriff auf das neue Objekt auf den Attributen des übergeordneten Objekts oder Containerobjekts.

Der Windows Installer legt die [**UserSID-Eigenschaft**](usersid.md) auf die Sicherheits-ID (SID) oder den Benutzer fest, der die Installation ausgeführt.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE55](ice55.md)  
</dl>

 

 




