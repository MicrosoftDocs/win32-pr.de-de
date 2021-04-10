---
title: MDM_Policy_Result01_Start02-Klasse
description: Die MDM \_ Policy \_ Result01 \_ Start02-Klasse stellt die verfügbaren Richtlinien für den Startbildschirm dar.
ms.assetid: 997d64f9-b2be-47b8-8a84-97438e7fa842
keywords:
- MDM_Policy_Result01_Start02-Klasse
- MDM_Policy_Result01_Start02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Start02
- MDM_Policy_Result01_Start02.InstanceID
- MDM_Policy_Result01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412e9ccecdc9f691b03a94ba5528eb6b7e3d7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040488"
---
# <a name="mdm_policy_result01_start02-class"></a><span data-ttu-id="8dbdb-105">MDM- \_ Richtlinie \_ Result01 \_ Start02-Klasse</span><span class="sxs-lookup"><span data-stu-id="8dbdb-105">MDM\_Policy\_Result01\_Start02 class</span></span>

<span data-ttu-id="8dbdb-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="8dbdb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8dbdb-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="8dbdb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8dbdb-108">Die **MDM \_ Policy \_ Result01 \_ Start02** -Klasse stellt die verfügbaren Richtlinien für den Startbildschirm dar.</span><span class="sxs-lookup"><span data-stu-id="8dbdb-108">The **MDM\_Policy\_Result01\_Start02** class represents the start screen policies available.</span></span>

<span data-ttu-id="8dbdb-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8dbdb-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dbdb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dbdb-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Start02
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

## <a name="members"></a><span data-ttu-id="8dbdb-111">Member</span><span class="sxs-lookup"><span data-stu-id="8dbdb-111">Members</span></span>

<span data-ttu-id="8dbdb-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Start02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8dbdb-112">The **MDM\_Policy\_Result01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="8dbdb-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8dbdb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8dbdb-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8dbdb-114">Properties</span></span>

<span data-ttu-id="8dbdb-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Start02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8dbdb-115">The **MDM\_Policy\_Result01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8dbdb-116">Allowpinnedfolderdocuments</span><span class="sxs-lookup"><span data-stu-id="8dbdb-116">AllowPinnedFolderDocuments</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdocuments)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-119">Allowpinnedfolderdownloads</span><span class="sxs-lookup"><span data-stu-id="8dbdb-119">AllowPinnedFolderDownloads</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-122">Allowpinnedfolderfileexplorer</span><span class="sxs-lookup"><span data-stu-id="8dbdb-122">AllowPinnedFolderFileExplorer</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderfileexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-125">Allowpinnedfolderhomegroup</span><span class="sxs-lookup"><span data-stu-id="8dbdb-125">AllowPinnedFolderHomeGroup</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderhomegroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-128">Allowpinnedfoldermusic</span><span class="sxs-lookup"><span data-stu-id="8dbdb-128">AllowPinnedFolderMusic</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldermusic)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-131">Allowpinnedfoldernetwork</span><span class="sxs-lookup"><span data-stu-id="8dbdb-131">AllowPinnedFolderNetwork</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldernetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-134">Ordner "allowpinnedfolderpersonal"</span><span class="sxs-lookup"><span data-stu-id="8dbdb-134">AllowPinnedFolderPersonalFolder</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpersonalfolder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-137">Allowpinnedfolderpictures</span><span class="sxs-lookup"><span data-stu-id="8dbdb-137">AllowPinnedFolderPictures</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpictures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-140">Allowpinnedfoldersettings</span><span class="sxs-lookup"><span data-stu-id="8dbdb-140">AllowPinnedFolderSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldersettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-143">Allowpinnedfoldervideos</span><span class="sxs-lookup"><span data-stu-id="8dbdb-143">AllowPinnedFolderVideos</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldervideos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-146">Forcestartsize</span><span class="sxs-lookup"><span data-stu-id="8dbdb-146">ForceStartSize</span></span>](/windows/client-management/mdm/policy-csp-start#start-forcestartsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-149">Hideapplist</span><span class="sxs-lookup"><span data-stu-id="8dbdb-149">HideAppList</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideapplist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-152">Hidechangeaccountsettings</span><span class="sxs-lookup"><span data-stu-id="8dbdb-152">HideChangeAccountSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidechangeaccountsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-153">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-155">Hidefrequentlyusedapps</span><span class="sxs-lookup"><span data-stu-id="8dbdb-155">HideFrequentlyUsedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidefrequentlyusedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-156">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-158">Hidehibernate</span><span class="sxs-lookup"><span data-stu-id="8dbdb-158">HideHibernate</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidehibernate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-159">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-161">Hidelta</span><span class="sxs-lookup"><span data-stu-id="8dbdb-161">HideLock</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-162">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-164">Hidepowerbutton</span><span class="sxs-lookup"><span data-stu-id="8dbdb-164">HidePowerButton</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepowerbutton)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-165">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-167">Hiderecentjumplists</span><span class="sxs-lookup"><span data-stu-id="8dbdb-167">HideRecentJumplists</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentjumplists)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-168">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-170">Hiderecentlyadde dapps</span><span class="sxs-lookup"><span data-stu-id="8dbdb-170">HideRecentlyAddedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentlyaddedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-171">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-173">Hiderestart</span><span class="sxs-lookup"><span data-stu-id="8dbdb-173">HideRestart</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-174">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-176">Hideshutdown</span><span class="sxs-lookup"><span data-stu-id="8dbdb-176">HideShutDown</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideshutdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-177">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-179">Hidesignout</span><span class="sxs-lookup"><span data-stu-id="8dbdb-179">HideSignOut</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesignout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-180">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-182">Hidesleep</span><span class="sxs-lookup"><span data-stu-id="8dbdb-182">HideSleep</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesleep)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-183">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-185">Hideswitchaccount</span><span class="sxs-lookup"><span data-stu-id="8dbdb-185">HideSwitchAccount</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideswitchaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-186">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-188">Hideusertile</span><span class="sxs-lookup"><span data-stu-id="8dbdb-188">HideUserTile</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideusertile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-189">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8dbdb-191">Importedgeassets</span><span class="sxs-lookup"><span data-stu-id="8dbdb-191">ImportEdgeAssets</span></span>](/windows/client-management/mdm/policy-csp-start#start-importedgeassets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-193">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8dbdb-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dbdb-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-197">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8dbdb-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8dbdb-198">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="8dbdb-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="8dbdb-199">Für diese Klasse ist die Zeichenfolge "Start".</span><span class="sxs-lookup"><span data-stu-id="8dbdb-199">For this class, the string is "Start"</span></span>

</dd> <dt>

[<span data-ttu-id="8dbdb-200">Nopinningtotaskbar</span><span class="sxs-lookup"><span data-stu-id="8dbdb-200">NoPinningToTaskbar</span></span>](/windows/client-management/mdm/policy-csp-start#start-nopinningtotaskbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-201">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-202">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8dbdb-203">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-203">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dbdb-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-206">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8dbdb-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8dbdb-207">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="8dbdb-207">Describes the full path to the parent node.</span></span> <span data-ttu-id="8dbdb-208">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="8dbdb-208">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="8dbdb-209">StartLayout</span><span class="sxs-lookup"><span data-stu-id="8dbdb-209">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dbdb-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dbdb-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dbdb-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dbdb-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8dbdb-212">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8dbdb-212">Requirements</span></span>



| <span data-ttu-id="8dbdb-213">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8dbdb-213">Requirement</span></span> | <span data-ttu-id="8dbdb-214">Wert</span><span class="sxs-lookup"><span data-stu-id="8dbdb-214">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dbdb-215">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8dbdb-215">Minimum supported client</span></span><br/> | <span data-ttu-id="8dbdb-216">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8dbdb-216">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8dbdb-217">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8dbdb-217">Minimum supported server</span></span><br/> | <span data-ttu-id="8dbdb-218">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8dbdb-218">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8dbdb-219">Namespace</span><span class="sxs-lookup"><span data-stu-id="8dbdb-219">Namespace</span></span><br/>                | <span data-ttu-id="8dbdb-220">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="8dbdb-220">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="8dbdb-221">MOF</span><span class="sxs-lookup"><span data-stu-id="8dbdb-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8dbdb-222"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8dbdb-222"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8dbdb-223">DLL</span><span class="sxs-lookup"><span data-stu-id="8dbdb-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8dbdb-224"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8dbdb-224"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dbdb-225">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dbdb-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dbdb-226">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="8dbdb-226">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

