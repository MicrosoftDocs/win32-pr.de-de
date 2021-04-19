---
description: Enthält Informationen zu AppHelp-Daten.
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: APPHELP_DATA Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPHELP_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 20c66779dcb3d89746de5f90b2817ddcdb37b59f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338888"
---
# <a name="apphelp_data-structure"></a><span data-ttu-id="47c14-103">AppHelp- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="47c14-103">APPHELP\_DATA structure</span></span>

<span data-ttu-id="47c14-104">Enthält Informationen zu AppHelp-Daten.</span><span class="sxs-lookup"><span data-stu-id="47c14-104">Contains Apphelp data information.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c14-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47c14-105">Syntax</span></span>


```C++
typedef struct tagAPPHELP_DATA {
  DWORD  dwFlags;
  DWORD  dwSeverity;
  DWORD  dwHTMLHelpID;
  LPTSTR szAppName;
  TAGREF trExe;
  LPTSTR szURL;
  LPTSTR szLink;
  LPTSTR szAppTitle;
  LPTSTR szContact;
  LPTSTR szDetails;
  DWORD  dwData;
  BOOL   bSPEntry;
} APPHELP_DATA, *PAPPHELP_DATA;
```



## <a name="members"></a><span data-ttu-id="47c14-106">Member</span><span class="sxs-lookup"><span data-stu-id="47c14-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="47c14-107">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="47c14-107">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="47c14-108">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="47c14-108">This parameter can be one of more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="47c14-109"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**Shimreg \_ \_Shim deaktivieren** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="47c14-109"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="47c14-110"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**Shimreg \_ \_AppHelp deaktivieren** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="47c14-110"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="47c14-111"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**Shimreg \_ AppHelp \_ NoUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="47c14-111"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="47c14-112"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**Shimreg \_ AppHelp \_ Abbrechen** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="47c14-112"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="47c14-113"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**Shimreg \_ \_SxS deaktivieren** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="47c14-113"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="47c14-114"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**Shimreg \_ \_Ebene deaktivieren** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="47c14-114"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="47c14-115"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**Shimreg \_ \_Treiber deaktivieren** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="47c14-115"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="47c14-116">**dwschwere Grad**</span><span class="sxs-lookup"><span data-stu-id="47c14-116">**dwSeverity**</span></span>
</dt> <dd>

<span data-ttu-id="47c14-117">Dieser Parameter kann apptype \_ None (0) sein.</span><span class="sxs-lookup"><span data-stu-id="47c14-117">This parameter can be APPTYPE\_NONE (0).</span></span>

</dd> <dt>

<span data-ttu-id="47c14-118">**dwhtmlhelpid**</span><span class="sxs-lookup"><span data-stu-id="47c14-118">**dwHTMLHelpID**</span></span>
</dt> <dd>

<span data-ttu-id="47c14-119">Der HTML-Hilfe Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="47c14-119">The HTML Help identifier.</span></span>

</dd> <dt>

<span data-ttu-id="47c14-120">**szappname**</span><span class="sxs-lookup"><span data-stu-id="47c14-120">**szAppName**</span></span>
</dt> <dd>

<span data-ttu-id="47c14-121">Der Anwendungsname.</span><span class="sxs-lookup"><span data-stu-id="47c14-121">The application name.</span></span>

</dd> <dt>

<span data-ttu-id="47c14-122">**trexe**</span><span class="sxs-lookup"><span data-stu-id="47c14-122">**trExe**</span></span>
</dt> <dd>

<span data-ttu-id="47c14-123">Die [**tagref**](tagref.md) der entsprechenden ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="47c14-123">The [**TAGREF**](tagref.md) of the corresponding executable file.</span></span>

</dd> <dt>

<span data-ttu-id="47c14-124">**szURL**</span><span class="sxs-lookup"><span data-stu-id="47c14-124">**szURL**</span></span>
</dt> <dd>

<span data-ttu-id="47c14-125">Die URL für den AppHelp Online-Link.</span><span class="sxs-lookup"><span data-stu-id="47c14-125">The URL for Apphelp online link.</span></span>

</dd> <dt>

<span data-ttu-id="47c14-126">**szlink**</span><span class="sxs-lookup"><span data-stu-id="47c14-126">**szLink**</span></span>
</dt> <dd>

<span data-ttu-id="47c14-127">Der Linktext für **szURL**.</span><span class="sxs-lookup"><span data-stu-id="47c14-127">The link text for **szURL**.</span></span>

</dd> <dt>

<span data-ttu-id="47c14-128">**szapptitle**</span><span class="sxs-lookup"><span data-stu-id="47c14-128">**szAppTitle**</span></span>
</dt> <dd>

<span data-ttu-id="47c14-129">Der Titel für die AppHelp-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="47c14-129">The title for the Apphelp message.</span></span>

</dd> <dt>

<span data-ttu-id="47c14-130">**szcontact**</span><span class="sxs-lookup"><span data-stu-id="47c14-130">**szContact**</span></span>
</dt> <dd>

<span data-ttu-id="47c14-131">Die Kontaktinformationen des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="47c14-131">The vendor contact information.</span></span>

</dd> <dt>

<span data-ttu-id="47c14-132">**szdetails**</span><span class="sxs-lookup"><span data-stu-id="47c14-132">**szDetails**</span></span>
</dt> <dd>

<span data-ttu-id="47c14-133">Die ausführliche AppHelp-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="47c14-133">The detailed Apphelp message.</span></span>

</dd> <dt>

<span data-ttu-id="47c14-134">**dwdata**</span><span class="sxs-lookup"><span data-stu-id="47c14-134">**dwData**</span></span>
</dt> <dd>

<span data-ttu-id="47c14-135">Benutzerdefinierte Daten, die von der Anwendung verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="47c14-135">User-defined data managed by the application.</span></span>

</dd> <dt>

<span data-ttu-id="47c14-136">**bspentry**</span><span class="sxs-lookup"><span data-stu-id="47c14-136">**bSPEntry**</span></span>
</dt> <dd>

<span data-ttu-id="47c14-137">Dieser Member ist **true** , wenn sich dieser Eintrag in der Service Pack Datenbank befindet, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="47c14-137">This member is **TRUE** if this entry is in the service pack database and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47c14-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47c14-138">Requirements</span></span>



| <span data-ttu-id="47c14-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47c14-139">Requirement</span></span> | <span data-ttu-id="47c14-140">Wert</span><span class="sxs-lookup"><span data-stu-id="47c14-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="47c14-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47c14-141">Minimum supported client</span></span><br/> | <span data-ttu-id="47c14-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47c14-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="47c14-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47c14-143">Minimum supported server</span></span><br/> | <span data-ttu-id="47c14-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47c14-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47c14-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47c14-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c14-146">**Sdbreadapphelpdetailsdata**</span><span class="sxs-lookup"><span data-stu-id="47c14-146">**SdbReadApphelpDetailsData**</span></span>](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




