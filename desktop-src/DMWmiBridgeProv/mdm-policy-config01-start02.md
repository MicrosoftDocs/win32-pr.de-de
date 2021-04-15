---
title: MDM_Policy_Config01_Start02-Klasse
description: Die MDM \_ Policy \_ Config01 \_ Start02-Klasse stellt die verfügbaren Richtlinien für den Startbildschirm dar.
ms.assetid: 2aef29c8-164a-4111-9c1a-e63eeec2531e
keywords:
- MDM_Policy_Config01_Start02-Klasse
- MDM_Policy_Config01_Start02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Start02
- MDM_Policy_Config01_Start02.InstanceID
- MDM_Policy_Config01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9095fcf1611ef106fed5ad93f059e165ebcac15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476929"
---
# <a name="mdm_policy_config01_start02-class"></a><span data-ttu-id="e66d2-105">MDM- \_ Richtlinie \_ Config01 \_ Start02-Klasse</span><span class="sxs-lookup"><span data-stu-id="e66d2-105">MDM\_Policy\_Config01\_Start02 class</span></span>

<span data-ttu-id="e66d2-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="e66d2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e66d2-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="e66d2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e66d2-108">Die **MDM \_ Policy \_ Config01 \_ Start02** -Klasse stellt die verfügbaren Richtlinien für den Startbildschirm dar.</span><span class="sxs-lookup"><span data-stu-id="e66d2-108">The **MDM\_Policy\_Config01\_Start02** class represents the start screen policies available.</span></span>

<span data-ttu-id="e66d2-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e66d2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e66d2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e66d2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 AllowPinnedFolderVideos;
  sint32 AllowPinnedFolderSettings;
  sint32 AllowPinnedFolderPictures;
  sint32 AllowPinnedFolderPersonalFolder;
  sint32 AllowPinnedFolderNetwork;
  sint32 AllowPinnedFolderMusic;
  sint32 AllowPinnedFolderHomeGroup;
  sint32 AllowPinnedFolderFileExplorer;
  sint32 AllowPinnedFolderDownloads;
  sint32 AllowPinnedFolderDocuments;
  sint32 ForceStartSize;
  string StartLayout;
  sint32 NoPinningToTaskbar;
  string ImportEdgeAssets;
  sint32 HideUserTile;
  sint32 HideSwitchAccount;
  sint32 HideSleep;
  sint32 HideSignOut;
  sint32 HideShutDown;
  sint32 HideRestart;
  sint32 HideRecentlyAddedApps;
  sint32 HideRecentJumplists;
  sint32 HidePowerButton;
  sint32 HideLock;
  sint32 HideHibernate;
  sint32 HideFrequentlyUsedApps;
  sint32 HideChangeAccountSettings;
  sint32 HideAppList;
};
```

## <a name="members"></a><span data-ttu-id="e66d2-111">Member</span><span class="sxs-lookup"><span data-stu-id="e66d2-111">Members</span></span>

<span data-ttu-id="e66d2-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Start02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e66d2-112">The **MDM\_Policy\_Config01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="e66d2-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e66d2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e66d2-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e66d2-114">Properties</span></span>

<span data-ttu-id="e66d2-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Start02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e66d2-115">The **MDM\_Policy\_Config01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e66d2-116">Allowpinnedfolderdocuments</span><span class="sxs-lookup"><span data-stu-id="e66d2-116">AllowPinnedFolderDocuments</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdocuments)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-119">Allowpinnedfolderdownloads</span><span class="sxs-lookup"><span data-stu-id="e66d2-119">AllowPinnedFolderDownloads</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-122">Allowpinnedfolderfileexplorer</span><span class="sxs-lookup"><span data-stu-id="e66d2-122">AllowPinnedFolderFileExplorer</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderfileexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-125">Allowpinnedfolderhomegroup</span><span class="sxs-lookup"><span data-stu-id="e66d2-125">AllowPinnedFolderHomeGroup</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderhomegroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-128">Allowpinnedfoldermusic</span><span class="sxs-lookup"><span data-stu-id="e66d2-128">AllowPinnedFolderMusic</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldermusic)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-131">Allowpinnedfoldernetwork</span><span class="sxs-lookup"><span data-stu-id="e66d2-131">AllowPinnedFolderNetwork</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldernetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-134">Ordner "allowpinnedfolderpersonal"</span><span class="sxs-lookup"><span data-stu-id="e66d2-134">AllowPinnedFolderPersonalFolder</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpersonalfolder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-137">Allowpinnedfolderpictures</span><span class="sxs-lookup"><span data-stu-id="e66d2-137">AllowPinnedFolderPictures</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpictures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-140">Allowpinnedfoldersettings</span><span class="sxs-lookup"><span data-stu-id="e66d2-140">AllowPinnedFolderSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldersettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-143">Allowpinnedfoldervideos</span><span class="sxs-lookup"><span data-stu-id="e66d2-143">AllowPinnedFolderVideos</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldervideos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-146">Forcestartsize</span><span class="sxs-lookup"><span data-stu-id="e66d2-146">ForceStartSize</span></span>](/windows/client-management/mdm/policy-csp-start#start-forcestartsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-149">Hideapplist</span><span class="sxs-lookup"><span data-stu-id="e66d2-149">HideAppList</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideapplist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-152">Hidechangeaccountsettings</span><span class="sxs-lookup"><span data-stu-id="e66d2-152">HideChangeAccountSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidechangeaccountsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-153">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-155">Hidefrequentlyusedapps</span><span class="sxs-lookup"><span data-stu-id="e66d2-155">HideFrequentlyUsedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidefrequentlyusedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-156">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-158">Hidehibernate</span><span class="sxs-lookup"><span data-stu-id="e66d2-158">HideHibernate</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidehibernate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-159">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-161">Hidelta</span><span class="sxs-lookup"><span data-stu-id="e66d2-161">HideLock</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-162">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-164">Hidepowerbutton</span><span class="sxs-lookup"><span data-stu-id="e66d2-164">HidePowerButton</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepowerbutton)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-165">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-167">Hiderecentjumplists</span><span class="sxs-lookup"><span data-stu-id="e66d2-167">HideRecentJumplists</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentjumplists)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-168">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-170">Hiderecentlyadde dapps</span><span class="sxs-lookup"><span data-stu-id="e66d2-170">HideRecentlyAddedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentlyaddedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-171">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-173">Hiderestart</span><span class="sxs-lookup"><span data-stu-id="e66d2-173">HideRestart</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-174">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-176">Hideshutdown</span><span class="sxs-lookup"><span data-stu-id="e66d2-176">HideShutDown</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideshutdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-177">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-179">Hidesignout</span><span class="sxs-lookup"><span data-stu-id="e66d2-179">HideSignOut</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesignout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-180">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-182">Hidesleep</span><span class="sxs-lookup"><span data-stu-id="e66d2-182">HideSleep</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesleep)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-183">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-185">Hideswitchaccount</span><span class="sxs-lookup"><span data-stu-id="e66d2-185">HideSwitchAccount</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideswitchaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-186">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-188">Hideusertile</span><span class="sxs-lookup"><span data-stu-id="e66d2-188">HideUserTile</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideusertile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-189">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e66d2-191">Importedgeassets</span><span class="sxs-lookup"><span data-stu-id="e66d2-191">ImportEdgeAssets</span></span>](/windows/client-management/mdm/policy-csp-start#start-importedgeassets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e66d2-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-193">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e66d2-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e66d2-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e66d2-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e66d2-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-197">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e66d2-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e66d2-198">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="e66d2-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="e66d2-199">Für diese Klasse ist die Zeichenfolge "Start".</span><span class="sxs-lookup"><span data-stu-id="e66d2-199">For this class, the string is "Start"</span></span>

</dd> <dt>

[<span data-ttu-id="e66d2-200">Nopinningtotaskbar</span><span class="sxs-lookup"><span data-stu-id="e66d2-200">NoPinningToTaskbar</span></span>](/windows/client-management/mdm/policy-csp-start#start-nopinningtotaskbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-201">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e66d2-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-202">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e66d2-203">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e66d2-203">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e66d2-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e66d2-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-206">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e66d2-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e66d2-207">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="e66d2-207">Describes the full path to the parent node.</span></span> <span data-ttu-id="e66d2-208">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="e66d2-208">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="e66d2-209">StartLayout</span><span class="sxs-lookup"><span data-stu-id="e66d2-209">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e66d2-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e66d2-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e66d2-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e66d2-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e66d2-212">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e66d2-212">Requirements</span></span>



| <span data-ttu-id="e66d2-213">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e66d2-213">Requirement</span></span> | <span data-ttu-id="e66d2-214">Wert</span><span class="sxs-lookup"><span data-stu-id="e66d2-214">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e66d2-215">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e66d2-215">Minimum supported client</span></span><br/> | <span data-ttu-id="e66d2-216">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e66d2-216">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e66d2-217">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e66d2-217">Minimum supported server</span></span><br/> | <span data-ttu-id="e66d2-218">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e66d2-218">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e66d2-219">Namespace</span><span class="sxs-lookup"><span data-stu-id="e66d2-219">Namespace</span></span><br/>                | <span data-ttu-id="e66d2-220">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="e66d2-220">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="e66d2-221">MOF</span><span class="sxs-lookup"><span data-stu-id="e66d2-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e66d2-222"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e66d2-222"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e66d2-223">DLL</span><span class="sxs-lookup"><span data-stu-id="e66d2-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e66d2-224"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e66d2-224"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e66d2-225">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e66d2-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e66d2-226">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="e66d2-226">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

