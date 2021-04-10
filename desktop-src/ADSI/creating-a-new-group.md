---
title: Erstellen einer neuen Gruppe
description: Joe von, der Unternehmens Administrator, muss eine neue Gruppe erstellen.
ms.assetid: a1bea695-d43f-47e6-af74-ba5abb0116a2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a4f46d595aa892ac75aa67d14bbc0356122271
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949121"
---
# <a name="creating-a-new-group"></a>Erstellen einer neuen Gruppe

Joe von, der Unternehmens Administrator, muss eine neue Gruppe erstellen. Er möchte einige Ressourcen, z. b. Datei, Active Directory Objekte oder andere Objekte, basierend auf der Mitgliedschaft dieser Gruppe sichern. Im folgenden Codebeispiel wird gezeigt, wie eine neue Gruppe erstellt wird.


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



Diese Gruppe, Verwaltung, wird in der Organisationseinheit "Sales" erstellt. Zunächst muss Joe ein ADSI-Objekt für die Vertriebs Organisationseinheit erstellen. Zweitens muss er das [**sAMAccountName**](/windows/desktop/AD/group-objects) -Attribut für dieses Objekt festlegen, da es sich um ein obligatorisches Attribut für die Abwärtskompatibilität handelt. Wenn **sAMAccountName** festgelegt ist, wird das Attribut in Windows NT 4,0-Tools wie z. b. Benutzer-Manager als **Mgmt** anstelle der **Verwaltung** angezeigt.

Drittens muss Joe den Typ der Gruppe angeben. In einer Windows 2000-Domäne gibt es drei Arten von Gruppen: Global, lokale Domäne und Universal. Außerdem verfügt die Gruppe über die Sicherheitsmerkmale. Bei einer Gruppe kann es sich entweder um eine aktivierte oder nicht gesicherte Gruppe handeln. Sicherheits aktivierte Gruppen sind im Wesentlichen diejenigen, denen die Zugriffsrechte für Ressourcen ähnlich wie bei einem Benutzer erteilt oder verweigert werden können. Wenn Sie z. b. einer Gruppe Zugriff auf eine Dateifreigabe gewähren, bedeutet dies, dass alle Mitglieder der Gruppe auf die Dateifreigabe zugreifen können. Verteilerlisten können nicht auf ähnliche Weise verwendet werden – Sie können z. b. eine Verteilerliste nicht für den Zugriff auf eine Dateifreigabe erteilen. Während des Upgrades werden Windows NT 4,0-Gruppen als Gruppen mit aktivierter Sicherheit migriert. Nicht gesicherte Gruppen in Active Directory ähneln Verteilerlisten in Exchange. Daher sind das Erstellen von Gruppen oder Verteilerlisten ähnliche Vorgänge in Windows 2000. Im einheitlichen Modus von Windows 2000 (einheitlicher Modus bedeutet dies, dass alle Domänen Controller in einer Domäne Computer mit Windows 2000 Server sind). die Gruppen können auf jede beliebige Ebene eingebettet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auflisten von Objekten](enumerating-objects.md)
</dt> </dl>

 

 