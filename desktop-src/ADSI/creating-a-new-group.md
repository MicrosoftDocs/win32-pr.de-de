---
title: Erstellen einer neuen Gruppe
description: Joe Worden, der Unternehmensadministrator, muss eine neue Gruppe erstellen.
ms.assetid: a1bea695-d43f-47e6-af74-ba5abb0116a2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3f778e9eb953b60ca45665bcd92ff30efb9c111c959e78cf1824407d0a459c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962009"
---
# <a name="creating-a-new-group"></a>Erstellen einer neuen Gruppe

Joe Worden, der Unternehmensadministrator, muss eine neue Gruppe erstellen. Er möchte einige Ressourcen, z. B. Datei, Active Directory-Objekte oder andere Objekte, basierend auf der Mitgliedschaft in dieser Gruppe schützen. Das folgende Codebeispiel zeigt, wie Sie eine neue Gruppe erstellen.


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



Diese Gruppe,Verwaltung, wird in der Organisationseinheit Vertrieb erstellt. Zunächst muss Joe ein ADSI-Objekt für die Organisationseinheit Sales erstellen. Zweitens muss er das [**samAccountName-Attribut**](/windows/desktop/AD/group-objects) für dieses Objekt festlegen, da es ein obligatorisches Attribut für die Abwärtskompatibilität ist. Wenn **samAccountName** für dieses Beispiel festgelegt ist, wird Windows NT 4.0-Tools wie User Manager das Attribut als **mgmt** anstelle von **Management** angezeigt.

Drittens muss Joe den Typ der Gruppe angeben. In einer Windows 2000-Domäne gibt es drei Arten von Gruppen: Global, Domain Local und Universal. Darüber hinaus weist die Gruppe ihr Sicherheitsmerkmal auf. Eine Gruppe kann entweder eine sicherheitsfähige oder eine nicht gesicherte Gruppe sein. Im Wesentlichen handelt es sich bei sicherheitsfähigen Gruppen um Gruppen, denen Zugriffsrechte für Ressourcen gewährt oder verweigert werden können, ähnlich wie bei einem Benutzer. Das Gewähren von Gruppenzugriff auf eine Dateifreigabe bedeutet beispielsweise, dass alle Mitglieder der Gruppe auf die Dateifreigabe zugreifen können. Verteilerlisten können nicht auf ähnliche Weise verwendet werden. Beispielsweise können Sie einer Verteilerliste nicht das Recht gewähren, auf eine Dateifreigabe zuzugreifen. Während des Upgrades werden Windows NT 4.0-Gruppen als sicherheitsfähige Gruppen migriert. Nicht gesicherte Gruppen in Active Directory ähneln Verteilerlisten in Exchange. Daher sind das Erstellen von Gruppen oder Verteilerlisten ähnliche Vorgänge in Windows 2000. Im einheitlichen Modus Windows 2000 (der native Modus bedeutet, dass alle Domänencontroller in einer Domäne Computer sind, auf denen Windows Server 2000 ausgeführt wird) können die Gruppen auf eine beliebige Ebene geschachtelt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzählen von Objekten](enumerating-objects.md)
</dt> </dl>

 

 