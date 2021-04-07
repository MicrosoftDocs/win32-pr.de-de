---
title: Erstellen von Gruppen in einer Domäne
description: Ein Gruppen Objekt wird in Active Directory Domain Services im Domänen Container erstellt, in dem die neue Gruppe enthalten sein wird.
ms.assetid: 40792878-4219-4242-8cf7-b092b28f2ff4
ms.tgt_platform: multiple
keywords:
- Gruppen anzeigen, Erstellen von Gruppen in einer Domäne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100700b08fb82b750ee68dfed6bcb26060929e87
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038780"
---
# <a name="creating-groups-in-a-domain"></a><span data-ttu-id="d08f3-104">Erstellen von Gruppen in einer Domäne</span><span class="sxs-lookup"><span data-stu-id="d08f3-104">Creating Groups in a Domain</span></span>

<span data-ttu-id="d08f3-105">Ein Gruppen Objekt wird in Active Directory Domain Services im Domänen Container erstellt, in dem die neue Gruppe enthalten sein wird.</span><span class="sxs-lookup"><span data-stu-id="d08f3-105">A group object is created in Active Directory Domain Services in the domain container where the new group will be contained.</span></span> <span data-ttu-id="d08f3-106">Gruppen können im Stammverzeichnis der Domäne, innerhalb einer Organisationseinheit oder innerhalb eines Containers erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d08f3-106">Groups can be created at the root of the domain, within an organizational unit, or within a container.</span></span> <span data-ttu-id="d08f3-107">Verwenden Sie die [**IADsContainer:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) -Methode oder die [**IDirectoryObject::**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) -Methode, um ein Gruppen Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d08f3-107">To create a group object, use the [**IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) or the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span>

<span data-ttu-id="d08f3-108">Die folgenden Attribute sind erforderlich, um das Gruppen Objekt zu einer gültigen Gruppe zu machen, die vom Active Directory Server und dem Windows-Sicherheitssystem erkannt wird:</span><span class="sxs-lookup"><span data-stu-id="d08f3-108">The following attributes are required to make the group object a legal group that the Active Directory server and the Windows security system will recognize:</span></span>

<dl> <dt>

<span data-ttu-id="d08f3-109"><span id="cn"></span><span id="CN"></span>**2.300**</span><span class="sxs-lookup"><span data-stu-id="d08f3-109"><span id="cn"></span><span id="CN"></span>**cn**</span></span>
</dt> <dd>

<span data-ttu-id="d08f3-110">Gibt den Namen des Gruppen Objekts im Verzeichnis an.</span><span class="sxs-lookup"><span data-stu-id="d08f3-110">Specifies the name of the group object in the directory.</span></span> <span data-ttu-id="d08f3-111">Dabei handelt es sich um den relativen Distinguished Name des Objekts innerhalb des Containers, in dem die Gruppe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d08f3-111">This will be the object's relative distinguished name within the container where the group is created.</span></span>

</dd> <dt>

<span data-ttu-id="d08f3-112"><span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**GroupType**</span><span class="sxs-lookup"><span data-stu-id="d08f3-112"><span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**</span></span>
</dt> <dd>

<span data-ttu-id="d08f3-113">Enthält eine ganze Zahl, die den Gruppentyp und den Bereich angibt.</span><span class="sxs-lookup"><span data-stu-id="d08f3-113">Contains an integer that specifies the group type and scope.</span></span> <span data-ttu-id="d08f3-114">Die Enumeration der [**ADS- \_ \_ Gruppentyp \_**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) Enumeration definiert die möglichen Werte für das **GroupType** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="d08f3-114">The [**ADS\_GROUP\_TYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) enumeration defines the possible values for the **groupType** attribute.</span></span>

<span data-ttu-id="d08f3-115">In der folgenden Liste sind allgemeine Gruppen Typen und Werte für dieses Attribut definiert.</span><span class="sxs-lookup"><span data-stu-id="d08f3-115">The following list defines common group types and values for this attribute.</span></span>

<dl> <dt>

<span data-ttu-id="d08f3-116"><span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Lokale Domänen Verteilung</span><span class="sxs-lookup"><span data-stu-id="d08f3-116"><span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Domain Local Distribution</span></span>
</dt> <dd>

<span data-ttu-id="d08f3-117">**AD \_ - \_ Gruppentyp \_ Domäne \_ lokale \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="d08f3-117">**ADS\_GROUP\_TYPE\_DOMAIN\_LOCAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="d08f3-118"><span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Lokale Sicherheit der Domäne</span><span class="sxs-lookup"><span data-stu-id="d08f3-118"><span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Domain Local Security</span></span>
</dt> <dd>

<span data-ttu-id="d08f3-119">**Anzeigen \_ \_Gruppentyp \_ Domäne \_ lokale \_ Gruppen** \| **anzeigen \_ Gruppen \_ \_ Sicherheit \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="d08f3-119">**ADS\_GROUP\_TYPE\_DOMAIN\_LOCAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>

<span data-ttu-id="d08f3-120"><span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Globale Verteilung</span><span class="sxs-lookup"><span data-stu-id="d08f3-120"><span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Global Distribution</span></span>
</dt> <dd>

<span data-ttu-id="d08f3-121">**\_ \_ \_ globale Gruppe "ADS Group Type" \_**</span><span class="sxs-lookup"><span data-stu-id="d08f3-121">**ADS\_GROUP\_TYPE\_GLOBAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="d08f3-122"><span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Globale Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d08f3-122"><span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Global Security</span></span>
</dt> <dd>

<span data-ttu-id="d08f3-123">**Anzeigen \_ Gruppentyp der \_ \_ globalen \_ Gruppe** \| **ADS- \_ \_ Gruppentyp \_ Sicherheit \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="d08f3-123">**ADS\_GROUP\_TYPE\_GLOBAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>

<span data-ttu-id="d08f3-124"><span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Universelle Verteilung</span><span class="sxs-lookup"><span data-stu-id="d08f3-124"><span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Universal Distribution</span></span>
</dt> <dd>

<span data-ttu-id="d08f3-125">**\_ \_ \_ universelle Gruppe ADS-Gruppentyp \_**</span><span class="sxs-lookup"><span data-stu-id="d08f3-125">**ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="d08f3-126"><span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Universelle Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d08f3-126"><span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Universal Security</span></span>
</dt> <dd>

<span data-ttu-id="d08f3-127">**Anzeigen \_ \_Gruppentyp \_ \_** -Gruppentyp-Gruppentyp \| **\_ \_ \_ Sicherheit \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="d08f3-127">**ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>


</dt> <dd>

</dd> </dl>

<span data-ttu-id="d08f3-128">Wenn die Gruppe für das Festlegen der Zugriffs Steuerung für Verzeichnisobjekte vorgesehen ist, sollte die Gruppe eine globale Sicherheits-oder universelle Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="d08f3-128">If the group is intended for setting access control on directory objects, the group should be a Global Security or Universal Security group.</span></span>

<span data-ttu-id="d08f3-129">Beachten Sie, dass universelle Sicherheitsgruppen nur auf Windows 2000-Domänen erstellt werden können, die im einheitlichen Modus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d08f3-129">Be aware that Universal Security groups can only be created on Windows 2000 domains running in native mode.</span></span> <span data-ttu-id="d08f3-130">Weitere Informationen zum Erkennen von gemischtem und einheitlichem Modus finden Sie unter [Ermitteln des Betriebsmodus einer Domäne](detecting-the-operation-mode-of-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="d08f3-130">For more information about detecting mixed and native mode, see [Detecting the Operation Mode of a Domain](detecting-the-operation-mode-of-a-domain.md).</span></span>

</dd> <dt>

<span data-ttu-id="d08f3-131"><span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**</span><span class="sxs-lookup"><span data-stu-id="d08f3-131"><span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**</span></span>
</dt> <dd>

<span data-ttu-id="d08f3-132">Enthält eine Zeichenfolge, die den Namen für die Unterstützung von Clients und Servern aus einer früheren Version enthält.</span><span class="sxs-lookup"><span data-stu-id="d08f3-132">Contains a string that is the name used to support clients and servers from a previous version.</span></span> <span data-ttu-id="d08f3-133">Der **sAMAccountName** sollte weniger als 20 Zeichen lang sein, damit Clients einer früheren Version von Windows unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d08f3-133">The **sAMAccountName** should be less than 20 characters to support clients of a previous version of Windows.</span></span>

<span data-ttu-id="d08f3-134">Der **sAMAccountName** muss für alle Sicherheits Prinzipal Objekte innerhalb der Domäne eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d08f3-134">The **sAMAccountName** must be unique among all security principal objects within the domain.</span></span> <span data-ttu-id="d08f3-135">Eine Abfrage sollte für die Domäne ausgeführt werden, um zu überprüfen, ob **sAMAccountName** innerhalb der Domäne eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="d08f3-135">A query should be performed against the domain to verify that the **sAMAccountName** is unique within the domain.</span></span>

</dd> </dl>

<span data-ttu-id="d08f3-136">Die Mitglieder der Gruppe können zur Erstellungszeit mithilfe der [**IDirectoryObject:: deedsobject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) -Methode hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d08f3-136">The members of the group can be added at creation time using the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span> <span data-ttu-id="d08f3-137">Optional können Mitglieder der Gruppe nach der Erstellung mithilfe der [**IADsGroup:: Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) -Methode hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d08f3-137">Optionally, members can be added to the group after creation using the [**IADsGroup::Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) method.</span></span> <span data-ttu-id="d08f3-138">Weitere Informationen zum Hinzufügen von Mitgliedern zu einer Gruppe finden Sie unter [Hinzufügen von Mitgliedern zu Gruppen in einer Domäne](adding-members-to-groups-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="d08f3-138">For more information about adding members to a group, see [Adding Members to Groups in a Domain](adding-members-to-groups-in-a-domain.md).</span></span>

 

 