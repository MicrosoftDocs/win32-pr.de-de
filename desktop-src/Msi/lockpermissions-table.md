---
description: Wird verwendet, um einzelne Teile einer Anwendung in einer gesperrten Umgebung zu sichern. Sie kann mit der Installation von Dateien, Registrierungs Schlüsseln und erstellten Ordnern verwendet werden.
ms.assetid: 7c20e211-7704-49c2-a0c5-aaa695a09764
title: Lockberechtigungs Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c07402b80caec7beff68083567f2ff2fb9bf5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350208"
---
# <a name="lockpermissions-table"></a>Lockberechtigungs Tabelle

Die lockberechtigungs-Tabelle wird verwendet, um einzelne Teile einer Anwendung in einer gesperrten Umgebung zu sichern. Sie kann mit der Installation von Dateien, Registrierungs Schlüsseln und erstellten Ordnern verwendet werden.

Ein Paket, das für die Installation in Windows Server 2008 R2 oder Windows 7 vorgesehen ist, sollte die Tabelle " [msilockpermissionsex](msilockpermissionsex-table.md) " anstelle der Tabelle "lockberechtigungs Tabelle" verwenden. In Windows Installer Versionen vor Windows Installer 5,0 wird die Tabelle "msilockpermissionsex" ignoriert. Windows Installer 5,0 kann ein-Paket installieren, das die lockberechtigungs-Tabelle enthält. Ab Windows Installer 5,0 tritt bei der Installation eines Pakets, das sowohl die msilockpermissionsex-Tabelle als auch die lockberechtigungs Tabelle enthält, ein Fehler auf, und die Fehlermeldung 1941 wird Windows Installer zurückgegeben.

Die lockberechtigungs-Tabelle weist die folgenden Spalten auf.



| Spalte     | Typ                               | Schlüssel | Nullwerte zulässig |
|------------|------------------------------------|-----|----------|
| LockObject | [Bezeichner](identifier.md)       | J   | N        |
| Tabelle      | [Text](text.md)                   | J   | N        |
| Domain     | [Großformatige](formatted.md)         | J   | J        |
| Benutzer       | [Großformatige](formatted.md)         | J   | N        |
| Berechtigung | [Doubleiteger](doubleinteger.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

In dieser Spalte und der Tabellenspalte werden die Datei, das Verzeichnis oder der Registrierungsschlüssel angegeben, die gesichert werden sollen. Die LockObject-Spalte ist ein Fremdschlüssel, der auf den Primärschlüssel der Tabelle verweist, die in der Tabellenspalte angegeben ist.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub
</dt> <dd>

In dieser Spalte und der Spalte lockobject wird die Datei, das Verzeichnis oder der Registrierungsschlüssel angegeben, die gesichert werden sollen. Geben Sie in der Spalte Tabelle den Eintrag File, Registry oder Up Folder ein, um ein lockobject anzugeben, das in der [Dateitabelle](file-table.md), der [Registrierungs Tabelle](registry-table.md)oder der [Tabelle](createfolder-table.md)"Tabelle" aufgeführt ist.

</dd> <dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>-
</dt> <dd>

Die Spalte, die die Domäne des Benutzers identifiziert, für den Berechtigungen festgelegt werden sollen. Dies ist der Name eines eigenständigen Computers oder eines Domänen Namens. Der Spaltendatentyp ist [formatiert](formatted.md), und Sie können die Zeichenfolge \[ % UserDomain \] in diesem Feld verwenden, um den Wert der User Domain-Umgebungsvariablen für die aktuelle Domäne zu erhalten. Zum erhalten einer anderen Domäne müssen [benutzerdefinierte Aktionen](custom-actions.md)verwendet werden. Weitere Informationen finden Sie in der benutzerdefinierten Aktionstabelle.

</dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>Bedienungs
</dt> <dd>

Die Spalte, die den lokalisierten Namen des Benutzers identifiziert, für den Berechtigungen festgelegt werden sollen. Dieser Name muss sich auf dem Computer oder in der Domäne befinden. Die Installation schlägt fehl, wenn der Computer oder der Domänen Controller die Kombination aus Domäne und Benutzer nicht erkennt oder wenn die Sicherheits-ID (SID) des Benutzers nicht abgerufen werden kann. Es können mehrere Benutzer für ein einzelnes lockobject angegeben werden.

Die allgemeinen Benutzernamen "jeder" und "Administratoren" können in englischer Sprache eingegeben werden und werden bekannten SIDs zugeordnet. "LocalSystem" erhält Vollzugriff in allen Sicherheits Deskriptoren, die über die lockberechtigungtabelle erstellt wurden. Sie können den aktuellen Benutzer mit der Eigenschaft " [**Computername**](computername.md)", der Eigenschaft " [**LogonUser**](logonuser.md) " oder der [**username**](username.md) -Eigenschaft in diesem Feld erhalten. Eine benutzerdefinierte Aktion ist erforderlich, um den lokalisierten Namen eines beliebigen Benutzers oder einer Gruppe einzugeben.

Sie können mehrere Datensätze mit identischen lockobject-und Table-Einträgen (aber unterschiedlichen Benutzer Einträgen) verwenden, um Zugriffs Steuerungs Listen für mehrere Benutzer anzugeben.

</dd> <dt>

<span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Berechtigung
</dt> <dd>

Die Spalte, die die ganzzahlige Beschreibung der System Privilegien identifiziert. Im folgenden finden Sie die am häufigsten verwendeten Werte (eine komplette Liste ist in "Winnt. h" vorhanden).



| Berechtigung                                                              | BESCHREIBUNG                     |
|------------------------------------------------------------------------|---------------------------------|
| generisch \_ alle<br/> 0X10000000<br/> 268435456<br/>     | Lese-, Schreib-und Ausführungs Zugriff |
| generisch \_ Ausführen<br/> 0X20000000<br/> 536870912<br/> | Zugriff ausführen                  |
| generischer \_ Schreibvorgang<br/> 0X40000000<br/> 1073741824<br/>  | Schreibzugriff                    |



 

Sie können \_ in der Berechtigungs Spalte keinen generischen Lesevorgang angeben. Der Versuch, dies zu tun, schlägt fehl. Stattdessen müssen Sie einen Wert angeben, z. b \_ . den Schlüssel Lesevorgang oder den \_ allgemeinen Datei Lesevorgang \_ .

In diese Spalte eingegebene NULL ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Informationen in dieser Tabelle werden in den Aktionen [InstallFiles](installfiles-action.md), [schreiteregistryvalues](writeregistryvalues-action.md)und [kreatefolders](createfolders-action.md) in [*Sequenz Tabellen*](s-gly.md) verarbeitet. Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

Die Berechtigung kann nur für Benutzer festgelegt werden, die bereits auf dem Computer oder in der Domäne vorhanden sind. Der Versuch, Berechtigungen für einen unbekannten Benutzer festzulegen, bewirkt, dass die Installation fehlschlägt, auch wenn dieses Benutzerkonto während der Installation durch eine verzögerte benutzerdefinierte Aktion erstellt wird.

Es wird empfohlen, dass die lokale Gruppe des Systemadministrators in allen Zugriffs Steuerungs Listen (Access Control Lists, ACL) enthalten ist. Dadurch wird sichergestellt, dass der Systemadministrator auf Objekte zugreifen und Sie verwalten kann.

Alle Dateien, Registrierungsschlüssel oder Verzeichnisse, die in der Tabelle lockberechtigungs Tabelle aufgeführt sind, erhalten eine explizite Sicherheits Beschreibung, unabhängig davon, ob ein vorhandenes Objekt ersetzt wird oder nicht. Der Windows Installer versucht, die Sicherheit von Objekten beizubehalten, die bereits im System vorhanden sind. Wenn ein Objekt nicht in der Tabelle lockberechtigungs Tabelle aufgeführt ist und ein vorhandenes Objekt ersetzt, ruft der Austausch die Sicherheitseinstellungen des Objekts ab, das es ersetzt.

Wenn ein Objekt nicht in der Tabelle lockberechtigungs Tabelle aufgeführt ist und kein vorhandenes Objekt ersetzt, empfängt es keine explizite Sicherheits Beschreibung. Der Zugriff auf das neue Objekt basiert auf den Attributen des übergeordneten Objekts bzw. des Container Objekts. Wenn ein Objekt nicht in der Tabelle aufgeführt ist und ein Objekt ohne explizite Sicherheits Beschreibung ersetzt, basiert der Zugriff auf das neue Objekt auf den Attributen des übergeordneten Objekts bzw. des Container Objekts.

Der Windows Installer legt die [**UserSID**](usersid.md) -Eigenschaft auf die Sicherheits-ID (SID) oder den Benutzer fest, der die Installation durchführt.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE55](ice55.md)  
</dl>

 

 




