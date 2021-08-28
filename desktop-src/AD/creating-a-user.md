---
title: Erstellen eines Benutzers
description: Um einen Benutzer in Active Directory Domain Services zu erstellen, erstellen Sie ein Benutzerobjekt im Domänencontainer der Domäne, in der Sie den Benutzer platzieren möchten.
ms.assetid: fb51895f-71e1-45b6-b8bc-ed674e822734
ms.tgt_platform: multiple
keywords:
- 'Active Directory-Beispiele: Active Directory, Erstellen eines Benutzers'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3422d269351ae29fd15d12585ca02b91a4b9c23
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469227"
---
# <a name="creating-a-user"></a>Erstellen eines Benutzers

Um einen Benutzer in Active Directory Domain Services zu erstellen, erstellen Sie ein Benutzerobjekt im Domänencontainer der Domäne, in der Sie den Benutzer platzieren möchten. Benutzer können am Stamm der Domäne, innerhalb einer Organisationseinheit oder innerhalb eines Containers erstellt werden.

Wenn Sie ein Benutzerobjekt erstellen, müssen Sie auch die in der folgenden Tabelle aufgeführten Attribute festlegen, um das Objekt als einen rechtlichen Benutzer festzulegen, der von Active Directory Domain Services und dem Windows-Sicherheit System erkannt wird.



| Attribut                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cn**](/windows/desktop/ADSchema/a-cn)                         | Gibt den Namen des Benutzerobjekts im Verzeichnis an. Dies ist der relative Distinguished Name (RDN) des Objekts.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**Samaccountname**](/windows/desktop/ADSchema/a-samaccountname) | Gibt eine Zeichenfolge an, die der Name ist, der zur Unterstützung von Clients und Servern aus einer früheren Version von Windows verwendet wird. Der [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) sollte weniger als 20 Zeichen lang sein, um Clients aus einer früheren Version von Windows zu unterstützen.<br/> [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) muss für alle Sicherheitsprinzipalobjekte innerhalb der Domäne eindeutig sein. Sie sollten eine Abfrage für die Domäne ausführen, um zu überprüfen, ob **sAMAccountName** innerhalb der Domäne eindeutig ist.<br/> [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) ist ein optionales Attribut. Der Server erstellt einen zufälligen **sAMAccountName-Wert,** wenn kein Wert angegeben ist.<br/> |



 

Sie können auch andere Attribute festlegen. Die folgenden Benutzerattribute werden mit Standardwerten festgelegt, wenn Sie sie zum Zeitpunkt der Erstellung nicht explizit festlegen.




| attribute | BESCHREIBUNG | 
|-----------|-------------|
| <a href="/windows/desktop/ADSchema/a-accountexpires"><strong>accountExpires</strong></a> | Gibt an, wann das Konto abläuft. Der Standardwert ist <strong>TIMEQ_FOREVER</strong>, was angibt, dass das Konto nie abläuft.<br /> | 
| <a href="/windows/desktop/ADSchema/a-ntsecuritydescriptor"><strong>Ntsecuritydescriptor</strong></a> | Eine Sicherheitsbeschreibung wird basierend auf bestimmten Regeln erstellt. Weitere Informationen finden Sie unter Festlegen von <a href="how-security-descriptors-are-set-on-new-directory-objects.md">Sicherheitsbeschreibungen für neue Verzeichnisobjekte.</a><br /> | 
| <a href="/windows/desktop/ADSchema/a-objectcategory"><strong>objectCategory</strong></a> | Gibt die Benutzerkategorie an. Der Standardwert ist "Person".<br /> | 
| <a href="/windows/desktop/ADSchema/a-name"><strong>Namen</strong></a> | Gibt den Benutzernamen an. Der Standardwert ist der für <a href="/windows/desktop/ADSchema/a-cn"><strong>cn</strong></a>festgelegte Wert.<br /> | 
| <a href="/windows/desktop/ADSchema/a-pwdlastset"><strong>pwdLastSet</strong></a> | Gibt an, wann der Benutzer das Kennwort zuletzt festgelegt hat. Der Standardwert ist 0 (null), was angibt, dass der Benutzer das Kennwort bei der nächsten Anmeldung ändern muss.<br /> | 
| <a href="/windows/desktop/ADSchema/a-useraccountcontrol"><strong>userAccountControl</strong></a> | Enthält Werte, die mehrere Anmelde- und Kontofunktionen für den Benutzer bestimmen.<br /> Standardmäßig werden die folgenden Flags festgelegt:<br /><ul><li><strong>UF_ACCOUNTDISABLE:</strong> Das Konto ist deaktiviert.</li><li><strong>UF_PASSWD_NOTREQD:</strong> Es ist kein Kennwort erforderlich.</li><li><strong>UF_NORMAL_ACCOUNT:</strong> Standardkontotyp, der einen typischen Benutzer darstellt.</li></ul> | 
| <a href="/windows/desktop/ADSchema/a-memberof"><strong>memberOf</strong></a> | Gibt die Gruppe oder Gruppen an, der bzw. denen der Benutzer direkt angehört. Der Standardwert ist "Domänenbenutzer".<br /> | 




 

Ein Benutzer wird erstellt, indem er an den gewünschten Container gebunden und dann eine der folgenden Methoden verwendet. Die Attribute [**cn**](/windows/desktop/ADSchema/a-cn) und [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) müssen festgelegt werden, bevor für den Benutzer ein Commit auf dem Server ausgeführt wird.



| Methode                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)                        | Das [**cn-Attribut**](/windows/desktop/ADSchema/a-cn) wird aus dem *bstrRelativeName-Parameter* entnommen. Für den neuen Benutzer muss ein Commit ausgeführt werden, indem [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) aufgerufen wird. Andernfalls wird das Objekt nicht erstellt. Weitere Informationen finden Sie unter [Beispielcode zum Erstellen eines Benutzers.](example-code-for-creating-a-user.md)<br/>                                                                                            |
| [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) | Das [**cn-Attribut**](/windows/desktop/ADSchema/a-cn) wird aus dem *parameter pszRDNName* übernommen. Für den neuen Benutzer wird ein Commit ausgeführt, wenn [**CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) aufgerufen wird. Weitere Informationen finden Sie unter [Beispielcode zum Erstellen eines Benutzers.](example-code-for-creating-a-user.md)<br/>                                                                                                                |
| [DirectoryEntries.Add](/dotnet/api/system.directoryservices.directoryentries.add?view=dotnet-plat-ext-3.1)       | Das [**cn-Attribut**](/windows/desktop/ADSchema/a-cn) wird aus dem *name-Parameter* übernommen. Für das neue Benutzerobjekt muss ein Commit ausgeführt werden, indem [DirectoryEntry.CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) aufgerufen wird. Andernfalls wird das Objekt nicht erstellt. Weitere Informationen finden Sie unter [Hinzufügen von Verzeichnisobjekten.](/previous-versions/ms180851(v=vs.90))<br/> |



 

Für den neuen Benutzer muss ein Commit auf dem Server ausgeführt werden, bevor andere Attribute als [**cn**](/windows/desktop/ADSchema/a-cn) und [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) geändert werden können. Dies liegt daran, dass das Benutzerkonto erst vorhanden ist, wenn ein Commit für den Benutzer ausgeführt wurde. Wenn ein Attribut für ein Objekt abgerufen oder geändert wird, das auf dem Server nicht vorhanden ist, tritt ein Fehler auf. Dies schließt das Aufrufen der [**IADsUser.SetPassword-Methode**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) ein. Beispielsweise würde die folgende Sequenz beim Erstellen eines Benutzers mit [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)befolgt werden:

1.  Rufen Sie [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) auf, um den Benutzer im lokalen Cache mit dem angegebenen [**cn**](/windows/desktop/ADSchema/a-cn)zu erstellen.
2.  Legen Sie das [**sAMAccountName-Attribut**](/windows/desktop/ADSchema/a-samaccountname) mit der [**IADs.Put-Methode**](/windows/desktop/api/iads/nf-iads-iads-put) auf den gewünschten Wert fest.
3.  Ändern Sie nun andere Attribute, z. B. [**userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol) Diese Einschränkung gilt auch für die ADSI-Eigenschaften wie [**IADsUser.AccountDisabled**](/windows/desktop/ADSI/iadsuser-property-methods)und Methoden wie [**IADsUser.SetPassword.**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword)
4.  Rufen Sie [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) auf, um den neuen Benutzer an den Server zu committen.

Wenn ein neues Benutzerkonto erstellt wird, ist es standardmäßig deaktiviert. Das Konto muss manuell oder programmgesteuert aktiviert werden. Um ein Benutzerkonto programmgesteuert zu aktivieren, entfernen Sie das **ADS \_ UF \_ ACCOUNTDISABLE-Flag** aus dem [**userAccountControl-Attribut.**](/windows/desktop/ADSchema/a-useraccountcontrol)

Wenn ein neues Benutzerkonto erstellt wird, ist für das [**userAccountControl-Attribut**](/windows/desktop/ADSchema/a-useraccountcontrol) für das Konto automatisch das **UF \_ PASSWD \_ NOTREQD-Flag** festgelegt, das angibt, dass für das Konto kein Kennwort erforderlich ist. Wenn die Sicherheitsrichtlinien der Domäne, in der das Konto erstellt wird, ein Kennwort für alle Benutzerkonten erfordern, muss das **UF \_ PASSWD \_ NOTREQD-Flag** aus dem **userAccountControl-Attribut** für das Konto entfernt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispielcode zum Erstellen eines Benutzers](example-code-for-creating-a-user.md)
</dt> </dl>
