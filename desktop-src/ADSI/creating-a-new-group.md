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
# <a name="creating-a-new-group"></a><span data-ttu-id="1dd71-103">Erstellen einer neuen Gruppe</span><span class="sxs-lookup"><span data-stu-id="1dd71-103">Creating a New Group</span></span>

<span data-ttu-id="1dd71-104">Joe von, der Unternehmens Administrator, muss eine neue Gruppe erstellen.</span><span class="sxs-lookup"><span data-stu-id="1dd71-104">Joe Worden, the enterprise administrator, must create a new group.</span></span> <span data-ttu-id="1dd71-105">Er möchte einige Ressourcen, z. b. Datei, Active Directory Objekte oder andere Objekte, basierend auf der Mitgliedschaft dieser Gruppe sichern.</span><span class="sxs-lookup"><span data-stu-id="1dd71-105">He would like to secure some resources, such as file, Active Directory objects, or other objects, based on the membership of this group.</span></span> <span data-ttu-id="1dd71-106">Im folgenden Codebeispiel wird gezeigt, wie eine neue Gruppe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1dd71-106">The following code example shows how to create a new group.</span></span>


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



<span data-ttu-id="1dd71-107">Diese Gruppe, Verwaltung, wird in der Organisationseinheit "Sales" erstellt.</span><span class="sxs-lookup"><span data-stu-id="1dd71-107">This group, Management, will be created in the Sales organizational unit.</span></span> <span data-ttu-id="1dd71-108">Zunächst muss Joe ein ADSI-Objekt für die Vertriebs Organisationseinheit erstellen.</span><span class="sxs-lookup"><span data-stu-id="1dd71-108">First, Joe must create an ADSI object for the Sales organizational unit.</span></span> <span data-ttu-id="1dd71-109">Zweitens muss er das [**sAMAccountName**](/windows/desktop/AD/group-objects) -Attribut für dieses Objekt festlegen, da es sich um ein obligatorisches Attribut für die Abwärtskompatibilität handelt.</span><span class="sxs-lookup"><span data-stu-id="1dd71-109">Second, he must set the [**samAccountName**](/windows/desktop/AD/group-objects) attribute on this object, because it is a mandatory attribute for backward compatibility.</span></span> <span data-ttu-id="1dd71-110">Wenn **sAMAccountName** festgelegt ist, wird das Attribut in Windows NT 4,0-Tools wie z. b. Benutzer-Manager als **Mgmt** anstelle der **Verwaltung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1dd71-110">For this example, when **samAccountName** is set, Windows NT 4.0 tools such as User Manager see the attribute as **mgmt** instead of **Management**.</span></span>

<span data-ttu-id="1dd71-111">Drittens muss Joe den Typ der Gruppe angeben.</span><span class="sxs-lookup"><span data-stu-id="1dd71-111">Third, Joe must specify the type of group.</span></span> <span data-ttu-id="1dd71-112">In einer Windows 2000-Domäne gibt es drei Arten von Gruppen: Global, lokale Domäne und Universal.</span><span class="sxs-lookup"><span data-stu-id="1dd71-112">In a Windows 2000 domain, there are three types of groups: Global, Domain Local, and Universal.</span></span> <span data-ttu-id="1dd71-113">Außerdem verfügt die Gruppe über die Sicherheitsmerkmale.</span><span class="sxs-lookup"><span data-stu-id="1dd71-113">In addition, the group carries its security characteristic.</span></span> <span data-ttu-id="1dd71-114">Bei einer Gruppe kann es sich entweder um eine aktivierte oder nicht gesicherte Gruppe handeln.</span><span class="sxs-lookup"><span data-stu-id="1dd71-114">A group can be either a security-enabled or a non-secured group.</span></span> <span data-ttu-id="1dd71-115">Sicherheits aktivierte Gruppen sind im Wesentlichen diejenigen, denen die Zugriffsrechte für Ressourcen ähnlich wie bei einem Benutzer erteilt oder verweigert werden können.</span><span class="sxs-lookup"><span data-stu-id="1dd71-115">Essentially, security-enabled groups are those that can be granted or denied access rights to resources, similar to a user.</span></span> <span data-ttu-id="1dd71-116">Wenn Sie z. b. einer Gruppe Zugriff auf eine Dateifreigabe gewähren, bedeutet dies, dass alle Mitglieder der Gruppe auf die Dateifreigabe zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="1dd71-116">Granting a group access to a file share, for example, implies that all members of the group can access the file share.</span></span> <span data-ttu-id="1dd71-117">Verteilerlisten können nicht auf ähnliche Weise verwendet werden – Sie können z. b. eine Verteilerliste nicht für den Zugriff auf eine Dateifreigabe erteilen.</span><span class="sxs-lookup"><span data-stu-id="1dd71-117">Distribution lists cannot be used in a similar manner—you cannot, for example, grant a distribution list the right to access a file share.</span></span> <span data-ttu-id="1dd71-118">Während des Upgrades werden Windows NT 4,0-Gruppen als Gruppen mit aktivierter Sicherheit migriert.</span><span class="sxs-lookup"><span data-stu-id="1dd71-118">During the upgrade, Windows NT 4.0 groups are migrated as security-enabled groups.</span></span> <span data-ttu-id="1dd71-119">Nicht gesicherte Gruppen in Active Directory ähneln Verteilerlisten in Exchange.</span><span class="sxs-lookup"><span data-stu-id="1dd71-119">Non-secured groups in Active Directory are similar to distribution lists in Exchange.</span></span> <span data-ttu-id="1dd71-120">Daher sind das Erstellen von Gruppen oder Verteilerlisten ähnliche Vorgänge in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1dd71-120">Hence, creating groups or distribution lists are similar operations in Windows 2000.</span></span> <span data-ttu-id="1dd71-121">Im einheitlichen Modus von Windows 2000 (einheitlicher Modus bedeutet dies, dass alle Domänen Controller in einer Domäne Computer mit Windows 2000 Server sind). die Gruppen können auf jede beliebige Ebene eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="1dd71-121">In the Windows 2000 native mode (native mode means that all domain controllers in a domain are computers running Windows 2000 Server), the groups can be nested to any level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dd71-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1dd71-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dd71-123">Auflisten von Objekten</span><span class="sxs-lookup"><span data-stu-id="1dd71-123">Enumerating Objects</span></span>](enumerating-objects.md)
</dt> </dl>

 

 