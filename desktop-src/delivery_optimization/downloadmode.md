---
title: Downloadmode-Enumeration (deliveryoptimization. h)
description: Definiert die verschiedenen Download Modi, die von der Übermittlungs Optimierung verwendet werden.
ms.assetid: 7E9407C6-A22F-459E-B316-5E7809F0067A
keywords:
- In diesem Modus wird die Übermittlungsoptimierung umgangen und stattdessen BITS verwendet. Sie können diesen Modus beispielsweise auswählen, damit Clients BranchCache verwenden können. Enumeration
topic_type:
- apiref
api_name:
- DownloadMode
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cde44a3d211040e2cc1dd62afd54f8284f5493e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040526"
---
# <a name="downloadmode-enumeration"></a><span data-ttu-id="21059-106">Downloadmode-Enumeration</span><span class="sxs-lookup"><span data-stu-id="21059-106">DownloadMode enumeration</span></span>

<span data-ttu-id="21059-107">Definiert die verschiedenen Download Modi, die von der Übermittlungs Optimierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21059-107">Defines the different download modes that Delivery Optimization uses.</span></span>

## <a name="syntax"></a><span data-ttu-id="21059-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="21059-108">Syntax</span></span>


```C++
typedef enum _DownloadMode { 
  DownloadMode_CdnOnly   = 0,
  DownloadMode_Lan       = 1,
  DownloadMode_Group     = 2,
  DownloadMode_Internet  = 3,
  DownloadMode_Simple    = 99,
  DownloadMode_Bypass    = 100
} DownloadMode;
```



## <a name="constants"></a><span data-ttu-id="21059-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="21059-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="21059-110"><span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**</span><span class="sxs-lookup"><span data-stu-id="21059-110"><span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**</span></span>
</dt> <dd>

<span data-ttu-id="21059-111">Mit dieser Einstellung wird die Peer-zu-Peer-Zwischenspeicherung deaktiviert, aber dennoch ist es möglich, Inhalte von Microsoft-Servern herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="21059-111">This setting disables peer-to-peer caching but still allows Delivery Optimization to download content from Microsoft servers.</span></span> <span data-ttu-id="21059-112">Dieser Modus verwendet zusätzliche Metadaten, die von den Clouddiensten für die Übermittlungs Optimierung bereitgestellt werden, um eine zuverlässige und effiziente Download Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="21059-112">This mode uses additional metadata provided by the Delivery Optimization cloud services for a peerless reliable and efficient download experience.</span></span>

</dd> <dt>

<span data-ttu-id="21059-113"><span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**</span><span class="sxs-lookup"><span data-stu-id="21059-113"><span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**</span></span>
</dt> <dd>

<span data-ttu-id="21059-114">Dieser Standardbetriebsmodus für die Übermittlungsoptimierung aktiviert die Freigabe über Peers im gleichen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="21059-114">This default operating mode for Delivery Optimization enables peer sharing on the same network.</span></span>

</dd> <dt>

<span data-ttu-id="21059-115"><span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**</span><span class="sxs-lookup"><span data-stu-id="21059-115"><span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**</span></span>
</dt> <dd>

<span data-ttu-id="21059-116">Wenn der Gruppenmodus festgelegt ist, wird die Gruppe automatisch basierend auf den Geräten Active Directory Domain Services (AD DS) (Windows 10, Version 1607) oder der Domäne, bei der das Gerät authentifiziert wird, ausgewählt (Windows 10, Version 1511).</span><span class="sxs-lookup"><span data-stu-id="21059-116">When group mode is set, the group is automatically selected based on the device s Active Directory Domain Services (AD DS) site (Windows 10, version 1607) or the domain the device is authenticated to (Windows 10, version 1511).</span></span> <span data-ttu-id="21059-117">Im Gruppenmodus erfolgt die Peerfreigabe über interne Subnetze zwischen Geräten, die zur gleichen Gruppe gehören, einschließlich Geräten in Zweigstellen.</span><span class="sxs-lookup"><span data-stu-id="21059-117">In group mode, peering occurs across internal subnets, between devices that belong to the same group, including devices in remote offices.</span></span> <span data-ttu-id="21059-118">Sie können die GroupID-Option verwenden, um eine eigene benutzerdefinierte Gruppe zu erstellen, unabhängig von Domänen und AD DS-Sites.</span><span class="sxs-lookup"><span data-stu-id="21059-118">You can use the GroupID option to create your own custom group independently of domains and AD DS sites.</span></span> <span data-ttu-id="21059-119">Der Downloadmodus „Gruppe“ wird den meisten Organisationen empfohlen, die die beste Bandbreitenoptimierung mit Übermittlungsoptimierung anstreben.</span><span class="sxs-lookup"><span data-stu-id="21059-119">Group download mode is the recommended option for most organizations looking to achieve the best bandwidth optimization with Delivery Optimization.</span></span>

</dd> <dt>

<span data-ttu-id="21059-120"><span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**</span><span class="sxs-lookup"><span data-stu-id="21059-120"><span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**</span></span>
</dt> <dd>

<span data-ttu-id="21059-121">Lässt Peerquellen im Internet für die Übermittlungsoptimierung zu.</span><span class="sxs-lookup"><span data-stu-id="21059-121">Enable Internet peer sources for Delivery Optimization.</span></span>

</dd> <dt>

<span data-ttu-id="21059-122"><span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**</span><span class="sxs-lookup"><span data-stu-id="21059-122"><span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**</span></span>
</dt> <dd>

<span data-ttu-id="21059-123">Im Einfachmodus wird die Verwendung von Clouddiensten für die Übermittlungsoptimierung vollständig deaktiviert (für Offlineumgebungen).</span><span class="sxs-lookup"><span data-stu-id="21059-123">Simple mode disables the use of Delivery Optimization cloud services completely (for offline environments).</span></span> <span data-ttu-id="21059-124">Die Übermittlungs Optimierung wechselt automatisch in diesen Modus, wenn die Clouddienste für die Übermittlungs Optimierung nicht verfügbar sind, nicht erreichbar sind oder wenn die Größe der Inhalts Datei weniger als 10 MB beträgt.</span><span class="sxs-lookup"><span data-stu-id="21059-124">Delivery Optimization switches to this mode automatically when the Delivery Optimization cloud services are unavailable, unreachable or when the content file size is less than 10 MB.</span></span> <span data-ttu-id="21059-125">In diesem Modus bietet die Übermittlungs Optimierung einen zuverlässigen Download, ohne Peer-zu-Peer-Caching.</span><span class="sxs-lookup"><span data-stu-id="21059-125">In this mode, Delivery Optimization provides a reliable download experience, with no peer-to-peer caching.</span></span>

</dd> <dt>

<span data-ttu-id="21059-126"><span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**</span><span class="sxs-lookup"><span data-stu-id="21059-126"><span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**</span></span>
</dt> <dd>

<span data-ttu-id="21059-127">In diesem Modus wird die Übermittlungsoptimierung umgangen und stattdessen BITS verwendet.</span><span class="sxs-lookup"><span data-stu-id="21059-127">Bypass Delivery Optimization and use BITS, instead.</span></span> <span data-ttu-id="21059-128">Sie können diesen Modus beispielsweise auswählen, damit Clients BranchCache verwenden können.</span><span class="sxs-lookup"><span data-stu-id="21059-128">For example, select this mode so that clients can use BranchCache.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21059-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21059-129">Requirements</span></span>

| <span data-ttu-id="21059-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21059-130">Requirement</span></span> | <span data-ttu-id="21059-131">Wert</span><span class="sxs-lookup"><span data-stu-id="21059-131">Value</span></span> |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="21059-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21059-132">Minimum supported client</span></span><br/> | <span data-ttu-id="21059-133">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21059-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="21059-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21059-134">Minimum supported server</span></span><br/> | <span data-ttu-id="21059-135">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21059-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>  |
| <span data-ttu-id="21059-136">Header</span><span class="sxs-lookup"><span data-stu-id="21059-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="21059-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="21059-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>               |
