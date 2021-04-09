---
title: Erstellen eines Benutzers
description: Um einen Benutzer in Active Directory Domain Services zu erstellen, erstellen Sie ein Benutzerobjekt im Domänen Container der Domäne, in der Sie den Benutzer platzieren möchten.
ms.assetid: fb51895f-71e1-45b6-b8bc-ed674e822734
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, Erstellen eines Benutzers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea10d0142af650d58b61967b008b207abca2c11
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103858516"
---
# <a name="creating-a-user"></a>Erstellen eines Benutzers

Um einen Benutzer in Active Directory Domain Services zu erstellen, erstellen Sie ein Benutzerobjekt im Domänen Container der Domäne, in der Sie den Benutzer platzieren möchten. Benutzer können im Stammverzeichnis der Domäne, innerhalb einer Organisationseinheit oder innerhalb eines Containers erstellt werden.

Wenn Sie ein Benutzerobjekt erstellen, müssen Sie auch die in der folgenden Tabelle aufgeführten Attribute festlegen, um das Objekt als einen juristischen Benutzer festzulegen, der von Active Directory Domain Services und dem Windows-Sicherheitssystem erkannt wird.



| Attribut                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**2.300**](/windows/desktop/ADSchema/a-cn)                         | Gibt den Namen des Benutzer Objekts im Verzeichnis an. Dies ist der Relative Distinguished Name (RDN) des Objekts.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) | Gibt eine Zeichenfolge mit dem Namen an, der zur Unterstützung von Clients und Servern aus einer früheren Version von Windows verwendet wird. Der [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) sollte weniger als 20 Zeichen lang sein, damit Clients aus einer früheren Version von Windows unterstützt werden.<br/> Der [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) muss für alle Sicherheits Prinzipal Objekte innerhalb der Domäne eindeutig sein. Sie sollten eine Abfrage für die Domäne durchführen, um zu überprüfen, ob **sAMAccountName** innerhalb der Domäne eindeutig ist.<br/> [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) ist ein optionales Attribut. Der Server erstellt einen zufälligen **sAMAccountName** -Wert, wenn kein Wert angegeben wird.<br/> |



 

Sie können auch andere Attribute festlegen. Die folgenden Benutzerattribute werden mit Standardwerten festgelegt, wenn Sie Sie nicht explizit zur Erstellungszeit festlegen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-accountexpires"><strong>AccountExpires</strong></a></td>
<td>Gibt an, wann das Konto abläuft. Der Standardwert ist <strong>TIMEQ_FOREVER</strong>, womit angegeben wird, dass das Konto nie abläuft.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-ntsecuritydescriptor"><strong>ntSecurityDescriptor</strong></a></td>
<td>Eine Sicherheits Beschreibung wird auf der Grundlage spezifischer Regeln erstellt. Weitere Informationen finden Sie unter <a href="how-security-descriptors-are-set-on-new-directory-objects.md">Festlegen von Sicherheits Deskriptoren für neue Verzeichnisobjekte</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-objectcategory"><strong>objectCategory</strong></a></td>
<td>Gibt die Benutzer Kategorie an. Der Standardwert ist &quot; Person &quot; .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-name"><strong>Benennen</strong></a></td>
<td>Gibt den Benutzernamen an. Der Standardwert ist der für <a href="/windows/desktop/ADSchema/a-cn"><strong>CN</strong></a>festgelegte Wert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-pwdlastset"><strong>pwdLastSet</strong></a></td>
<td>Gibt an, wann der Benutzer das Kennwort zuletzt festgelegt hat. Der Standardwert ist 0 (null) und gibt an, dass der Benutzer das Kennwort bei der nächsten Anmeldung ändern muss.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-useraccountcontrol"><strong>userAccountControl</strong></a></td>
<td>Enthält Werte, mit denen mehrere Anmelde-und Kontofunktionen für den Benutzer bestimmt werden.<br/> Standardmäßig sind die folgenden Flags festgelegt:<br/>
<ul>
<li><strong>UF_ACCOUNTDISABLE</strong> - Das Konto ist deaktiviert.</li>
<li><strong>UF_PASSWD_NOTREQD</strong> - Es ist kein Kennwort erforderlich.</li>
<li><strong>UF_NORMAL_ACCOUNT</strong> - Der Standard Kontotyp, der einen typischen Benutzer darstellt.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-memberof"><strong>memberOf</strong></a></td>
<td>Gibt die Gruppe oder Gruppen an, denen der Benutzer als direktes Mitglied angehört. Der Standardwert ist &quot; Domänen Benutzer &quot; .<br/></td>
</tr>
</tbody>
</table>



 

Ein Benutzer wird durch Binden an den gewünschten Container erstellt und verwendet dann eine der folgenden Methoden. Das [**CN**](/windows/desktop/ADSchema/a-cn) -Attribut und das [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) -Attribut müssen festgelegt werden, bevor der Benutzer an den Server übertragen wird.



| Methode                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)                        | Das [**CN**](/windows/desktop/ADSchema/a-cn) -Attribut wird aus dem *bstraurelativename* -Parameter entnommen. Für den neuen Benutzer muss ein Commit ausgeführt werden, indem [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) aufgerufen wird, oder das Objekt wird nicht erstellt. Weitere Informationen finden Sie unter [Beispiel Code zum Erstellen eines Benutzers](example-code-for-creating-a-user.md).<br/>                                                                                            |
| [**IDirectoryObject:: kreatedsobject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) | Das [**CN**](/windows/desktop/ADSchema/a-cn) -Attribut wird aus dem *pszrdnname* -Parameter entnommen. Für den neuen Benutzer wird ein Commit ausgeführt, wenn " [**kreatedsobject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) " aufgerufen wird. Weitere Informationen finden Sie unter [Beispiel Code zum Erstellen eines Benutzers](example-code-for-creating-a-user.md).<br/>                                                                                                                |
| [Director Entries. Add](/dotnet/api/system.directoryservices.directoryentries.add?view=dotnet-plat-ext-3.1)       | Das [**CN**](/windows/desktop/ADSchema/a-cn) -Attribut wird aus dem *Name* -Parameter entnommen. Für das neue Benutzerobjekt muss ein Commit ausgeführt werden, indem [DirectoryEntry. CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) aufgerufen wird, oder das Objekt wird nicht erstellt. Weitere Informationen finden Sie unter [Hinzufügen von Verzeichnis Objekten](/previous-versions/ms180851(v=vs.90)).<br/> |



 

Für den neuen Benutzer muss ein Commit an den Server ausgeführt werden, damit andere Attribute als [**CN**](/windows/desktop/ADSchema/a-cn) und [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) geändert werden können. Dies liegt daran, dass das Benutzerkonto erst vorhanden ist, wenn der Benutzer ein Commit ausgeführt hat. Wenn ein Attribut für ein Objekt, das auf dem Server nicht vorhanden ist, abgerufen oder geändert wird, tritt ein Fehler auf. Dies schließt das Aufrufen der [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) -Methode ein. Beim Erstellen eines Benutzers mit [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)folgt z. b. die folgende Sequenz:

1.  Rufen Sie [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) auf, um den Benutzer im lokalen Cache mit der angegebenen [**CN**](/windows/desktop/ADSchema/a-cn)zu erstellen.
2.  Legen Sie das [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) -Attribut mit der [**IADs. Put**](/windows/desktop/api/iads/nf-iads-iads-put) -Methode auf den gewünschten Wert fest.
3.  Ändern Sie nun andere Attribute, z. b. " [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)". Diese Einschränkung gilt auch für die ADSI-Eigenschaften, z [**. b. IADsUser. accountdeaktiviert**](/windows/desktop/ADSI/iadsuser-property-methods), und Methoden wie [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword).
4.  Nennen Sie [**IADs. abtinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) , um den neuen Benutzer an den Server zu übergeben.

Wenn ein neues Benutzerkonto erstellt wird, ist es standardmäßig deaktiviert. Das Konto muss manuell oder Programm gesteuert aktiviert werden. Wenn Sie ein Benutzerkonto Programm gesteuert aktivieren möchten, entfernen Sie das Flag "ADS-Konto **\_ \_ Deaktivieren** " aus dem [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) -Attribut.

Wenn ein neues Benutzerkonto erstellt wird, wird für das [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) -Attribut für das Konto automatisch das Flag " **UF \_ passwd \_ notreqd** " festgelegt, was darauf hinweist, dass für das Konto kein Kennwort erforderlich ist. Wenn für die Sicherheitsrichtlinien der Domäne, in der das Konto erstellt wird, ein Kennwort für alle Benutzerkonten erforderlich ist, muss das Flag " **UF \_ passwd \_ notreqd** " aus dem Attribut " **userAccountControl** " für das Konto entfernt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel Code zum Erstellen eines Benutzers](example-code-for-creating-a-user.md)
</dt> </dl>