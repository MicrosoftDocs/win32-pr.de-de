---
description: Datei Versionsverlauf-API
ms.assetid: 7488BA36-DEBE-42F1-8A12-A2DB1DE8B827
title: Datei Versionsverlauf-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb612a0bbbbd28b703a82bc65c5cd4d33640f760
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958286"
---
# <a name="file-history-api"></a><span data-ttu-id="9fd36-103">Datei Versionsverlauf-API</span><span class="sxs-lookup"><span data-stu-id="9fd36-103">File History API</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9fd36-104">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9fd36-104">In this section</span></span>

-   [<span data-ttu-id="9fd36-105">**FH- \_ Sicherungs \_ Status**</span><span class="sxs-lookup"><span data-stu-id="9fd36-105">**FH\_BACKUP\_STATUS**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_backup_status)
-   [<span data-ttu-id="9fd36-106">**Ergebnis der FH- \_ Geräte \_ Validierung \_**</span><span class="sxs-lookup"><span data-stu-id="9fd36-106">**FH\_DEVICE\_VALIDATION\_RESULT**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_device_validation_result)
-   [<span data-ttu-id="9fd36-107">**lokaler FH- \_ Richtlinientyp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9fd36-107">**FH\_LOCAL\_POLICY\_TYPE**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_local_policy_type)
-   [<span data-ttu-id="9fd36-108">**\_Kategorie der geschützten \_ Elemente \_ des FH**</span><span class="sxs-lookup"><span data-stu-id="9fd36-108">**FH\_PROTECTED\_ITEM\_CATEGORY**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_protected_item_category)
-   [<span data-ttu-id="9fd36-109">**FH- \_ Beibehaltungs \_ Typen**</span><span class="sxs-lookup"><span data-stu-id="9fd36-109">**FH\_RETENTION\_TYPES**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_retention_types)
-   [<span data-ttu-id="9fd36-110">**FH- \_ Ziel \_ Laufwerks \_ Typen**</span><span class="sxs-lookup"><span data-stu-id="9fd36-110">**FH\_TARGET\_DRIVE\_TYPES**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_target_drive_types)
-   [<span data-ttu-id="9fd36-111">**FH \_ - \_ Ziel \_ Eigenschaftentyp**</span><span class="sxs-lookup"><span data-stu-id="9fd36-111">**FH\_TARGET\_PROPERTY\_TYPE**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_target_property_type)
-   [<span data-ttu-id="9fd36-112">**"Fihconfigmgr"**</span><span class="sxs-lookup"><span data-stu-id="9fd36-112">**FhConfigMgr**</span></span>](fhconfigmgr.md)
-   [<span data-ttu-id="9fd36-113">FhManagew.exe</span><span class="sxs-lookup"><span data-stu-id="9fd36-113">FhManagew.exe</span></span>](fhmanagew-exe.md)
-   [<span data-ttu-id="9fd36-114">**Ordnungs Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="9fd36-114">**FhReassociation**</span></span>](fhreassociation.md)
-   [<span data-ttu-id="9fd36-115">**"F"**</span><span class="sxs-lookup"><span data-stu-id="9fd36-115">**FhServiceClosePipe**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceclosepipe)
-   [<span data-ttu-id="9fd36-116">**"Hhserviceopenpipe"**</span><span class="sxs-lookup"><span data-stu-id="9fd36-116">**FhServiceOpenPipe**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceopenpipe)
-   [<span data-ttu-id="9fd36-117">**"F"**</span><span class="sxs-lookup"><span data-stu-id="9fd36-117">**FhServiceReloadConfiguration**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicereloadconfiguration)
-   [<span data-ttu-id="9fd36-118">**"F"-serviceblockbackup**</span><span class="sxs-lookup"><span data-stu-id="9fd36-118">**FhServiceBlockBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceblockbackup)
-   [<span data-ttu-id="9fd36-119">**"Hhservicestartbackup"**</span><span class="sxs-lookup"><span data-stu-id="9fd36-119">**FhServiceStartBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicestartbackup)
-   [<span data-ttu-id="9fd36-120">**"Lhservicestopbackup"**</span><span class="sxs-lookup"><span data-stu-id="9fd36-120">**FhServiceStopBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicestopbackup)
-   [<span data-ttu-id="9fd36-121">**"Hhserviceunblockbackup"**</span><span class="sxs-lookup"><span data-stu-id="9fd36-121">**FhServiceUnblockBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceunblockbackup)
-   [<span data-ttu-id="9fd36-122">**Ifhconfigmgr**</span><span class="sxs-lookup"><span data-stu-id="9fd36-122">**IFhConfigMgr**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr)
-   [<span data-ttu-id="9fd36-123">**Ifhreassociation**</span><span class="sxs-lookup"><span data-stu-id="9fd36-123">**IFhReassociation**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation)
-   [<span data-ttu-id="9fd36-124">**Ifhscopeiterator**</span><span class="sxs-lookup"><span data-stu-id="9fd36-124">**IFhScopeIterator**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhscopeiterator)
-   [<span data-ttu-id="9fd36-125">**Ifhtarget**</span><span class="sxs-lookup"><span data-stu-id="9fd36-125">**IFhTarget**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhtarget)

 

 



