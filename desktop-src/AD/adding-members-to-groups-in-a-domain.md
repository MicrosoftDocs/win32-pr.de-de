---
title: Hinzufügen von Mitgliedern zu Gruppen in einer Domäne
description: In diesem Thema wird gezeigt, wie Sie Gruppen in einer Domäne Mitglieder hinzufügen.
ms.assetid: be65cd4e-df3e-416b-a673-774b71ab6996
ms.tgt_platform: multiple
keywords:
- Hinzufügen von Mitgliedern zu Gruppen in einer Domänen-AD
- Gruppen anzeigen, Hinzufügen von Mitgliedern zu Gruppen in einer Domäne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbd454348dc3eb519d03a7c5574746025c79a3f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472709"
---
# <a name="adding-members-to-groups-in-a-domain"></a>Hinzufügen von Mitgliedern zu Gruppen in einer Domäne

Eine Gruppe kann eine beliebige Anzahl von Benutzern, Kontakten oder anderen Gruppen als Mitglieder enthalten. In der folgenden Liste sind die Attribute des Group-Objekts aufgelistet, mit denen die Gruppenmitgliedschaft gesteuert wird.



| Attribut                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Kollege**](/windows/desktop/ADSchema/a-member)<br/>     | Das [**Member**](/windows/desktop/ADSchema/a-member) -Attribut enthält die Distinguished Names für die Objekte, die Mitglieder der Gruppe sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**memberOf**](/windows/desktop/ADSchema/a-memberof)<br/> | Das Attribut " [**Member**](/windows/desktop/ADSchema/a-memberof) " enthält die Distinguished Names von Gruppen, die die Gruppe als direktes Mitglied enthalten. Das Attribut " **Member** " enthält keine geerbten Gruppen Mitgliedschafts Daten. Wenn groupA z. b. ein Mitglied von GroupB ist und GroupB Mitglied von groupc ist, enthält die Attribut **Mitgliedschaft** für groupA GroupB, jedoch nicht groupc.<br/> Der Active Directory Server verwaltet diese Eigenschaft. Wenn ein definierter Name der Element Eigenschaft einer anderen Gruppe hinzugefügt wird, [**wird der Distinguished**](/windows/desktop/ADSchema/a-member) Name dieser Gruppe dieser Gruppe hinzugefügt. [](/windows/desktop/ADSchema/a-memberof)<br/> |



 

Jede der folgenden Methoden kann verwendet werden, um einer Gruppe ein Mitglied hinzuzufügen. Sie können einen Member hinzufügen, indem Sie den Distinguished Name des Members oder die Bindung zum Member-Objekt verwenden und dann das Member-Objekt dem Group-Objekt hinzufügen.

Verwenden Sie zum Hinzufügen eines Members, der zu einer Downleveldomäne gehört, einer Gruppe in einer komplexer Darstellung-Domäne das bindbare Format der SID-Zeichenfolge für den Distinguished Name. Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie eine **objectSID** in eine bindbare Zeichenfolge konvertieren, finden **Sie unter Beispiel** [Code für die Konvertierung von objectSID in eine bindbare Zeichen](example-code-for-converting-an-objectsid-into-a-bindable-string-.md)Folge.

<dl> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IADsGroup"></span><span id="adding_members_to_a_group_by_using_iadsgroup"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IADSGROUP"></span>Hinzufügen von Mitgliedern zu einer Gruppe mithilfe von "IADsGroup"
</dt> <dd>

Die [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) -Schnittstelle kann verwendet werden, um mithilfe der [**IADsGroup. Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) -Methode Mitglieder zu einer Gruppe hinzuzufügen. Binden an und Abrufen der **IADsGroup** -Schnittstelle für das Group-Objekt. Anschließend kann die **IADsGroup. Add** -Methode zum Hinzufügen von Mitgliedern zur Gruppe verwendet werden.

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IDirectoryObject"></span><span id="adding_members_to_a_group_by_using_idirectoryobject"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IDIRECTORYOBJECT"></span>Hinzufügen von Mitgliedern zu einer Gruppe mithilfe von IDirectoryObject
</dt> <dd>

Die [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) -Schnittstelle kann verwendet werden, um mithilfe der [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) -Methode Member zu einer Gruppe hinzuzufügen, um das [**Member**](/windows/desktop/ADSchema/a-member) -Attribut für die Gruppe zu ändern. Binden an und Abrufen der **IDirectoryObject** -Schnittstelle für das Group-Objekt. Verwenden Sie dann die **IDirectoryObject:: setobjectattributes** -Methode, um das **Member** -Attribut zu ändern.

> [!Note]  
> Da das [**Member**](/windows/desktop/ADSchema/a-member) -Attribut über mehrere Werte verfügt, stellen Sie sicher, dass Sie den AD-Steuerelement Code anfügen verwenden, um dem **Member** -Attribut einen Distinguished Name hinzuzufügen. **\_ \_** Durch die Verwendung des **ADS zum \_ \_ Update** -Code des ADS werden **die vorhandenen Element** Werte überschrieben.

 

Die [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) -Schnittstelle kann auch zum Hinzufügen von Mitgliedern zu einer Gruppe verwendet werden, wenn die Gruppe durch Angabe der Elemente im *pattributeentries* -Parameter der [**IDirectoryObject:: foratedsobject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) -Methode erstellt wird.

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_System.DirectoryServices"></span><span id="adding_members_to_a_group_by_using_system.directoryservices"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_SYSTEM.DIRECTORYSERVICES"></span>Hinzufügen von Mitgliedern zu einer Gruppe mithilfe von System. DirectoryServices
</dt> <dd>

Mithilfe des [System. DirectoryServices](/dotnet/api/system.directoryservices) -Namespace können Sie einer Gruppe Mitglieder hinzufügen, indem Sie die **PropertyValueCollection. Add** -Methode für die **Member** -Eigenschaft des Group-Objekts verwenden. Weitere Informationen finden Sie unter [Festlegen von Eigenschaften für Verzeichnisobjekte](/previous-versions/ms180860(v=vs.90)).

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_the_LDAP_API"></span><span id="adding_members_to_a_group_by_using_the_ldap_api"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_THE_LDAP_API"></span>Hinzufügen von Mitgliedern zu einer Gruppe mithilfe der LDAP-API
</dt> <dd>

Mithilfe der [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) -API können Sie Mitglieder zu einer Gruppe hinzufügen, indem Sie eine [**der \_ \* LDAP**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s) -Änderungs Funktionen verwenden. Weitere Informationen finden Sie unter [Ändern eines Verzeichniseintrags](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry).

</dd> </dl>

 

