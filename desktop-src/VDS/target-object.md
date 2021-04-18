---
description: Zielobjekt
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: Zielobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1e81ea94a2f608378eba069defc83a721e0fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352726"
---
# <a name="target-object"></a><span data-ttu-id="cccb2-103">Zielobjekt</span><span class="sxs-lookup"><span data-stu-id="cccb2-103">Target Object</span></span>

<span data-ttu-id="cccb2-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="cccb2-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="cccb2-105">Ein Zielobjekt modelliert ein iSCSI-Ziel, das in einem iSCSI-Subsystem enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cccb2-105">A target object models an iSCSI target that is contained within an iSCSI subsystem.</span></span>

<span data-ttu-id="cccb2-106">Verwenden Sie die [**ivdssubsystemiscsi:: querytargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) -Methode, um die iSCSI-Ziele des Subsystems zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="cccb2-106">Use the [**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) method to determine the iSCSI targets of the subsystem.</span></span> <span data-ttu-id="cccb2-107">Aufrufer können einen Zeiger auf ein bestimmtes Ziel abrufen, indem Sie das gewünschte Zielobjekt aus der-Enumeration auswählen, das von der **querytargets** -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cccb2-107">Callers can get a pointer to a specific target by selecting the desired target object from the enumeration that is returned by the **QueryTargets** method.</span></span> <span data-ttu-id="cccb2-108">Mit einem Zielobjekt können Sie den anzeigen amen des Ziels festlegen und die Zieleigenschaften, zugeordneten LUNs und das Subsystem, das das Ziel enthält, Abfragen.</span><span class="sxs-lookup"><span data-stu-id="cccb2-108">With a target object, you can set the target's friendly name and query for target properties, associated LUNs, and the subsystem that contains the target.</span></span>

<span data-ttu-id="cccb2-109">Host Computer müssen sich bei Zielen anmelden, damit Sie auf die zugehörigen LUNs zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="cccb2-109">Host computers must log on to targets to access their associated LUNs.</span></span> <span data-ttu-id="cccb2-110">Um eine Anmeldung bei einem Ziel durchzuführen, muss das Ziel mindestens über ein zugeordnetes Portal in einer der zugehörigen Portal Gruppen verfügen.</span><span class="sxs-lookup"><span data-stu-id="cccb2-110">To perform a logon to a target, the target must have at least one associated portal in one of its portal groups.</span></span> <span data-ttu-id="cccb2-111">Eingaben und Ausgaben von zugeordneten LUNs werden über diese Anmelde Sitzung behandelt.</span><span class="sxs-lookup"><span data-stu-id="cccb2-111">Input to and output from associated LUNs is handled through this logon session.</span></span>

<span data-ttu-id="cccb2-112">Zu den Zielobjekt Eigenschaften gehören ein Objekt Bezeichner, ein iSCSI-Name, ein Anzeige Name und ein CHAP-aktiviertes Flag.</span><span class="sxs-lookup"><span data-stu-id="cccb2-112">Target object properties include an object identifier, an iSCSI name, a friendly name, and a CHAP-enabled flag.</span></span>

<span data-ttu-id="cccb2-113">In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cccb2-113">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="cccb2-114">type</span><span class="sxs-lookup"><span data-stu-id="cccb2-114">Type</span></span>                                                                                      | <span data-ttu-id="cccb2-115">Element</span><span class="sxs-lookup"><span data-stu-id="cccb2-115">Element</span></span>                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cccb2-116">Schnittstellen, die von diesem Objekt immer nur in VDS 1,1-und 2,0-iSCSI-Anbietern verfügbar gemacht werden</span><span class="sxs-lookup"><span data-stu-id="cccb2-116">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="cccb2-117">[**Ivdsiscsitarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).</span><span class="sxs-lookup"><span data-stu-id="cccb2-117">[**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).</span></span>                                                                                 |
| <span data-ttu-id="cccb2-118">Zugehörige Enumerationen</span><span class="sxs-lookup"><span data-stu-id="cccb2-118">Associated enumerations</span></span>                                                                   | <span data-ttu-id="cccb2-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="cccb2-119">None.</span></span>                                                                                                                       |
| <span data-ttu-id="cccb2-120">Zugeordnete Strukturen</span><span class="sxs-lookup"><span data-stu-id="cccb2-120">Associated structures</span></span>                                                                     | <span data-ttu-id="cccb2-121">[**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) Ziel-und [**VDS- \_ Ziel \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_target_notification)für iSCSI-Ziel.</span><span class="sxs-lookup"><span data-stu-id="cccb2-121">[**VDS\_ISCSI\_TARGET\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) and [**VDS\_TARGET\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_target_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cccb2-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cccb2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cccb2-123">Hardware Anbieter Objekte</span><span class="sxs-lookup"><span data-stu-id="cccb2-123">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="cccb2-124">**Ivdssubsystemiscsi:: querytargets**</span><span class="sxs-lookup"><span data-stu-id="cccb2-124">**IVdsSubSystemIscsi::QueryTargets**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
