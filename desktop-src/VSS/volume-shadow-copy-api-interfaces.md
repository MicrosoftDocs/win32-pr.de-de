---
description: Die Volumeschattenkopie-Dienst (VSS)-API stellt sowohl com-als auch C++-Schnittstellen zur Unterstützung der Erstellung von Anforderern und Writern bereit.
ms.assetid: 3a0c60df-666c-4e33-a54c-7fa5ddbfde13
title: Volumeschattenkopie-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc1291f0e63b18530f92d99f9d526202df078fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129304"
---
# <a name="volume-shadow-copy-api-interfaces"></a><span data-ttu-id="8bd3b-103">Volumeschattenkopie-API</span><span class="sxs-lookup"><span data-stu-id="8bd3b-103">Volume Shadow Copy API Interfaces</span></span>

<span data-ttu-id="8bd3b-104">Die Volumeschattenkopie-Dienst (VSS)-API stellt sowohl com-als auch C++-Schnittstellen zur Unterstützung der Erstellung von Anforderern und Writern bereit.</span><span class="sxs-lookup"><span data-stu-id="8bd3b-104">The Volume Shadow Copy Service (VSS) API provides both COM and C++ interfaces to support the creation of requesters and writers.</span></span>

## <a name="vss-requester-specific-interfaces"></a><span data-ttu-id="8bd3b-105">VSS-Requester-Specific Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8bd3b-105">VSS Requester-Specific Interfaces</span></span>

-   [<span data-ttu-id="8bd3b-106">**IVssBackupComponents**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-106">**IVssBackupComponents**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
-   [<span data-ttu-id="8bd3b-107">**Ivssbackupcomponentsex**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-107">**IVssBackupComponentsEx**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex)
-   [<span data-ttu-id="8bd3b-108">**IVssBackupComponentsEx2**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-108">**IVssBackupComponentsEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
-   [<span data-ttu-id="8bd3b-109">**IVssBackupComponentsEx3**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-109">**IVssBackupComponentsEx3**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)
-   [<span data-ttu-id="8bd3b-110">**Ivssexamineschreibmetadaten**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-110">**IVssExamineWriterMetadata**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)
-   [<span data-ttu-id="8bd3b-111">**IVssExamineWriterMetadataEx**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-111">**IVssExamineWriterMetadataEx**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex)
-   [<span data-ttu-id="8bd3b-112">**IVssExamineWriterMetadataEx2**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-112">**IVssExamineWriterMetadataEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)
-   [<span data-ttu-id="8bd3b-113">**Ivsswmcomponent**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-113">**IVssWMComponent**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)
-   [<span data-ttu-id="8bd3b-114">**Ivssschreitercomponentsxt**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-114">**IVssWriterComponentsExt**</span></span>](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext)

## <a name="vss-writer-specific-interfaces"></a><span data-ttu-id="8bd3b-115">VSS-Writer-Specific Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8bd3b-115">VSS Writer-Specific Interfaces</span></span>

-   [<span data-ttu-id="8bd3b-116">**Ivsskreateexpressschreitermetadata**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-116">**IVssCreateExpressWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)
-   [<span data-ttu-id="8bd3b-117">**Ivsskreateschreitermetadata**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-117">**IVssCreateWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)
-   [<span data-ttu-id="8bd3b-118">**IVssCreateWriterMetadataEx**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-118">**IVssCreateWriterMetadataEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)
-   [<span data-ttu-id="8bd3b-119">**Ivssexpresswriter**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-119">**IVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)
-   [<span data-ttu-id="8bd3b-120">**Ivssschreitercomponents**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-120">**IVssWriterComponents**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents)

## <a name="vss-hardware-provider-specific-interfaces"></a><span data-ttu-id="8bd3b-121">VSS-Hardware Provider-Specific Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8bd3b-121">VSS Hardware Provider-Specific Interfaces</span></span>

-   [<span data-ttu-id="8bd3b-122">**Ivssadmin**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-122">**IVssAdmin**</span></span>](/windows/desktop/api/VsAdmin/nn-vsadmin-ivssadmin)
-   [<span data-ttu-id="8bd3b-123">**Ivsshardwaresnapshotprovider**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-123">**IVssHardwareSnapshotProvider**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider)
-   [<span data-ttu-id="8bd3b-124">**Ivsshardwaresnapshotproviderex**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-124">**IVssHardwareSnapshotProviderEx**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)
-   [<span data-ttu-id="8bd3b-125">**Ivssproviderkreatesnapshotset**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-125">**IVssProviderCreateSnapshotSet**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset)
-   [<span data-ttu-id="8bd3b-126">**Ivssprovidernotification**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-126">**IVssProviderNotifications**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications)

## <a name="vss-software-provider-specific-interfaces"></a><span data-ttu-id="8bd3b-127">VSS-Software Provider-Specific Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8bd3b-127">VSS Software Provider-Specific Interfaces</span></span>

-   [<span data-ttu-id="8bd3b-128">**Ivsssoftwaresnapshotprovider**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-128">**IVssSoftwareSnapshotProvider**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsssoftwaresnapshotprovider)

## <a name="vss-shared-interfaces"></a><span data-ttu-id="8bd3b-129">Freigegebene VSS-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8bd3b-129">VSS Shared Interfaces</span></span>

-   [<span data-ttu-id="8bd3b-130">**IVssAsync**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-130">**IVssAsync**</span></span>](/windows/desktop/api/Vss/nn-vss-ivssasync)
-   [<span data-ttu-id="8bd3b-131">**IVssComponent**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-131">**IVssComponent**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)
-   [<span data-ttu-id="8bd3b-132">**Ivsscomponstex**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-132">**IVssComponentEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)
-   [<span data-ttu-id="8bd3b-133">**IVssComponentEx2**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-133">**IVssComponentEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)
-   [<span data-ttu-id="8bd3b-134">**Ivssenumuject**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-134">**IVssEnumObject**</span></span>](/windows/desktop/api/Vss/nn-vss-ivssenumobject)
-   [<span data-ttu-id="8bd3b-135">**Ivsswmabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-135">**IVssWMDependency**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)
-   [<span data-ttu-id="8bd3b-136">**Ivsswmfiledebug**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-136">**IVssWMFiledesc**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)

## <a name="vss-management-interfaces"></a><span data-ttu-id="8bd3b-137">VSS-Verwaltungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8bd3b-137">VSS Management Interfaces</span></span>

-   [<span data-ttu-id="8bd3b-138">**Ivssdifferenalsoftwaresnapshotmgmt**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-138">**IVssDifferentialSoftwareSnapshotMgmt**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt)
-   [<span data-ttu-id="8bd3b-139">**IVssDifferentialSoftwareSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-139">**IVssDifferentialSoftwareSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)
-   [<span data-ttu-id="8bd3b-140">**IVssDifferentialSoftwareSnapshotMgmt3**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-140">**IVssDifferentialSoftwareSnapshotMgmt3**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)
-   [<span data-ttu-id="8bd3b-141">**Ivssenumschlag-gmtobject**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-141">**IVssEnumMgmtObject**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssenummgmtobject)
-   [<span data-ttu-id="8bd3b-142">**Ivsssnapshotmgmt**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-142">**IVssSnapshotMgmt**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt)
-   [<span data-ttu-id="8bd3b-143">**IVssSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="8bd3b-143">**IVssSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 
