---
title: Hinzufügen von Mitgliedern zu Gruppen in einer Domäne
description: In diesem Thema wird gezeigt, wie Sie Mitglieder zu Gruppen in einer Domäne hinzufügen.
ms.assetid: be65cd4e-df3e-416b-a673-774b71ab6996
ms.tgt_platform: multiple
keywords:
- Hinzufügen von Mitgliedern zu Gruppen in einer Domänen-AD-Domäne
- Gruppen AD , Hinzufügen von Mitgliedern zu Gruppen in einer Domäne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c9f0c85943752b42cf3d9d8b88d385aaba9e014b21aa9f538955cb49b1a750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024757"
---
# <a name="adding-members-to-groups-in-a-domain"></a>Hinzufügen von Mitgliedern zu Gruppen in einer Domäne

Eine Gruppe kann eine beliebige Anzahl von Benutzern, Kontakten oder anderen Gruppen als Mitglieder enthalten. In der folgenden Liste sind die Attribute des Gruppenobjekts aufgeführt, die die Gruppenmitgliedschaft steuern.



| attribute                                      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Mitglied**](/windows/desktop/ADSchema/a-member)<br/>     | Das [](/windows/desktop/ADSchema/a-member) Memberattribut enthält die Distinguished Names für die Objekte, die Mitglieder der Gruppe sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**memberOf**](/windows/desktop/ADSchema/a-memberof)<br/> | Das [**memberOf-Attribut**](/windows/desktop/ADSchema/a-memberof) enthält die Distinguished Names von Gruppen, die die Gruppe als direktes Mitglied enthalten. Das **memberOf-Attribut** enthält keine geerbten Gruppenmitgliedschaftsdaten. Wenn GroupA beispielsweise Mitglied von GroupB und GroupB Mitglied von GroupC ist, enthält das **memberOf-Attribut** für GroupA GroupB, aber nicht GroupC.<br/> Der Active Directory-Server verwaltet diese Eigenschaft. Wenn der Membereigenschaft einer [](/windows/desktop/ADSchema/a-member) anderen Gruppe ein Distinguished Name hinzugefügt wird, wird der Distinguished Name dieser Gruppe der [**memberOf-Eigenschaft dieser Gruppe**](/windows/desktop/ADSchema/a-memberof) hinzugefügt.<br/> |



 

Jede der folgenden Methoden kann verwendet werden, um einer Gruppe ein Mitglied hinzuzufügen. Sie können einen Member hinzufügen, indem Sie den Distinguished Name des Mitglieds oder der Bindung zum Memberobjekt verwenden und dann das Memberobjekt zum Gruppenobjekt hinzufügen.

Verwenden Sie die bindbare Form der SID-Zeichenfolge für den Distinguished Name, um einer Gruppe in einer uplevel-Domäne ein Mitglied hinzuzufügen, das zu einer Downleveldomäne gehört. Weitere Informationen und ein Codebeispiel, das zeigt, wie eine **objectSid** in eine bindbare Zeichenfolge konvertiert wird, finden Sie in der **Beispielfunktion GetLDAPSidBindStringFromVariantSID** im Beispielcode zum Konvertieren einer objectSid in eine [bindbare Zeichenfolge.](example-code-for-converting-an-objectsid-into-a-bindable-string-.md)

<dl> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IADsGroup"></span><span id="adding_members_to_a_group_by_using_iadsgroup"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IADSGROUP"></span>Hinzufügen von Mitgliedern zu einer Gruppe mithilfe von IADsGroup
</dt> <dd>

Die [**IADsGroup-Schnittstelle**](/windows/desktop/api/iads/nn-iads-iadsgroup) kann verwendet werden, um einer Gruppe Mithilfe der [**IADsGroup.Add-Methode Member**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) hinzuzufügen. Binden An und Abrufen der **IADsGroup-Schnittstelle** für das Gruppenobjekt. Anschließend kann die **IADsGroup.Add-Methode** verwendet werden, um der Gruppe Mitglieder hinzuzufügen.

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IDirectoryObject"></span><span id="adding_members_to_a_group_by_using_idirectoryobject"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IDIRECTORYOBJECT"></span>Hinzufügen von Mitgliedern zu einer Gruppe mithilfe von IDirectoryObject
</dt> <dd>

Die [**IDirectoryObject-Schnittstelle**](/windows/desktop/api/iads/nn-iads-idirectoryobject) kann zum Hinzufügen von Membern zu einer Gruppe verwendet werden, indem [](/windows/desktop/ADSchema/a-member) die [**IDirectoryObject::SetObjectAttributes-Methode**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) verwendet wird, um das Memberattribut für die Gruppe zu ändern. Binden Sie an die **IDirectoryObject-Schnittstelle** für das Gruppenobjekt, und beziehen Sie sie. Verwenden Sie dann die **IDirectoryObject::SetObjectAttributes-Methode,** um das **Memberattribut zu** ändern.

> [!Note]  
> Da das [**Memberattribut**](/windows/desktop/ADSchema/a-member) über mehrere Werte verfügt, stellen Sie sicher, dass Sie den **ADS \_ ATTR APPEND-Steuerungscode \_** verwenden, um dem Memberattribut einen Distinguished Name hinzuzufügen.  Die Verwendung **des ADS \_ ATTR UPDATE-Steuerungscodes \_** verursacht, dass die vorhandenen **Memberwerte** überschrieben werden.

 

Die [**IDirectoryObject-Schnittstelle**](/windows/desktop/api/iads/nn-iads-idirectoryobject) kann auch zum Hinzufügen von Mitgliedern zu einer Gruppe verwendet werden, wenn die Gruppe erstellt wird, indem die Member im *pAttributeEntries-Parameter* der [**IDirectoryObject::CreateDSObject-Methode**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) angegeben werden.

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_System.DirectoryServices"></span><span id="adding_members_to_a_group_by_using_system.directoryservices"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_SYSTEM.DIRECTORYSERVICES"></span>Hinzufügen von Mitgliedern zu einer Gruppe mithilfe von System.DirectoryServices
</dt> <dd>

Sie können den [System.DirectoryServices-Namespace](/dotnet/api/system.directoryservices) verwenden, um einer Gruppe Elemente hinzuzufügen, indem Sie die **PropertyValueCollection.Add-Methode** für die **Membereigenschaft** des Gruppenobjekts verwenden. Weitere Informationen finden Sie unter [Festlegen von Eigenschaften für Verzeichnisobjekte.](/previous-versions/ms180860(v=vs.90))

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_the_LDAP_API"></span><span id="adding_members_to_a_group_by_using_the_ldap_api"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_THE_LDAP_API"></span>Hinzufügen von Mitgliedern zu einer Gruppe mithilfe der LDAP-API
</dt> <dd>

Sie können die [Lightweight Directory Access Protocol-API](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) verwenden, um einer Gruppe Mitglieder hinzuzufügen, indem Sie eine der [**LDAP-Änderungsfunktionen \_ \***](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s) verwenden. Weitere Informationen finden Sie unter [Ändern eines Verzeichniseintrags.](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)

</dd> </dl>

 

