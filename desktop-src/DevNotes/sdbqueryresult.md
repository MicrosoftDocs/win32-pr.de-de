---
description: Enthält die Ergebnisse der Abfrage der Shimdatenbank nach einer passenden ausführbaren Datei.
ms.assetid: 6e6df118-fb64-4a97-9280-050e3b4e3a4b
title: Sdbqueryresult-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SDBQUERYRESULT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9c631438d36116d47bfcb8675c390fb2974271c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958282"
---
# <a name="sdbqueryresult-structure"></a><span data-ttu-id="4442e-103">Sdbqueryresult-Struktur</span><span class="sxs-lookup"><span data-stu-id="4442e-103">SDBQUERYRESULT structure</span></span>

<span data-ttu-id="4442e-104">Enthält die Ergebnisse der Abfrage der Shimdatenbank nach einer passenden ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="4442e-104">Contains the results from querying the shim database for a matching executable.</span></span>

## <a name="syntax"></a><span data-ttu-id="4442e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4442e-105">Syntax</span></span>


```C++
typedef struct tagSDBQUERYRESULT {
  TAGREF atrExes[SDB_MAX_EXES];
  DWORD  adwExeFlags[SDB_MAX_EXES];
  TAGREF atrLayers[SDB_MAX_LAYERS];
  DWORD  dwLayerFlags;
  TAGREF trApphelp;
  DWORD  dwExeCount;
  DWORD  dwLayerCount;
  GUID   guidID;
  DWORD  dwFlags;
  DWORD  dwCustomSDBMap;
  GUID   rgGuidDB[SDB_MAX_SDBS];
} SDBQUERYRESULT, *PSDBQUERYRESULT;
```



## <a name="members"></a><span data-ttu-id="4442e-106">Member</span><span class="sxs-lookup"><span data-stu-id="4442e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4442e-107">**atrexes**</span><span class="sxs-lookup"><span data-stu-id="4442e-107">**atrExes**</span></span>
</dt> <dd>

<span data-ttu-id="4442e-108">Die **tagref** -Werte der übereinstimmenden ausführbaren Dateien.</span><span class="sxs-lookup"><span data-stu-id="4442e-108">The **TAGREF** values of the matching executable files.</span></span> <span data-ttu-id="4442e-109">Beachten Sie, dass die **maximalen SDB- \_ \_ EXEs** als 16 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4442e-109">Note that **SDB\_MAX\_EXES** is defined as 16.</span></span>

</dd> <dt>

<span data-ttu-id="4442e-110">**adwexeflags**</span><span class="sxs-lookup"><span data-stu-id="4442e-110">**adwExeFlags**</span></span>
</dt> <dd>

<span data-ttu-id="4442e-111">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4442e-111">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4442e-112"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**Shimreg \_ \_Shim deaktivieren** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="4442e-112"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-113"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**Shimreg \_ \_AppHelp deaktivieren** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="4442e-113"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-114"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**Shimreg \_ AppHelp \_ NoUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="4442e-114"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-115"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**Shimreg \_ AppHelp \_ Abbrechen** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="4442e-115"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-116"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**Shimreg \_ \_SxS deaktivieren** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="4442e-116"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-117"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**Shimreg \_ \_Ebene deaktivieren** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="4442e-117"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-118"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**Shimreg \_ \_Treiber deaktivieren** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="4442e-118"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="4442e-119">**atrlayer**</span><span class="sxs-lookup"><span data-stu-id="4442e-119">**atrLayers**</span></span>
</dt> <dd>

<span data-ttu-id="4442e-120">Die **tagref** -Werte der übereinstimmenden Ebenen.</span><span class="sxs-lookup"><span data-stu-id="4442e-120">The **TAGREF** values of the matching layers.</span></span> <span data-ttu-id="4442e-121">Beachten Sie, dass die **maximalen SDB- \_ \_ Ebenen** als 8 definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4442e-121">Note that **SDB\_MAX\_LAYERS** is defined as 8.</span></span>

</dd> <dt>

<span data-ttu-id="4442e-122">**dwlayerflags**</span><span class="sxs-lookup"><span data-stu-id="4442e-122">**dwLayerFlags**</span></span>
</dt> <dd>

<span data-ttu-id="4442e-123">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4442e-123">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4442e-124"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**Shimreg \_ \_Shim deaktivieren** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="4442e-124"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-125"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**Shimreg \_ \_AppHelp deaktivieren** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="4442e-125"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-126"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**Shimreg \_ AppHelp \_ NoUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="4442e-126"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-127"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**Shimreg \_ AppHelp \_ Abbrechen** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="4442e-127"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-128"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**Shimreg \_ \_SxS deaktivieren** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="4442e-128"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-129"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**Shimreg \_ \_Ebene deaktivieren** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="4442e-129"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-130"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**Shimreg \_ \_Treiber deaktivieren** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="4442e-130"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="4442e-131">**trapphelp**</span><span class="sxs-lookup"><span data-stu-id="4442e-131">**trApphelp**</span></span>
</dt> <dd>

<span data-ttu-id="4442e-132">Der **tagref** -Wert der "AppHelp"-Meldung der entsprechenden ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="4442e-132">The **TAGREF** value of the apphelp message of the corresponding executable.</span></span>

</dd> <dt>

<span data-ttu-id="4442e-133">**dwexecount**</span><span class="sxs-lookup"><span data-stu-id="4442e-133">**dwExeCount**</span></span>
</dt> <dd>

<span data-ttu-id="4442e-134">Die Anzahl der Elemente in **atrexes**.</span><span class="sxs-lookup"><span data-stu-id="4442e-134">The number of elements in **atrExes**.</span></span>

</dd> <dt>

<span data-ttu-id="4442e-135">**dwlayercount**</span><span class="sxs-lookup"><span data-stu-id="4442e-135">**dwLayerCount**</span></span>
</dt> <dd>

<span data-ttu-id="4442e-136">Die Anzahl der Elemente in **atrlayer**.</span><span class="sxs-lookup"><span data-stu-id="4442e-136">The number of elements in **atrLayers**.</span></span>

</dd> <dt>

<span data-ttu-id="4442e-137">**guidid darf**</span><span class="sxs-lookup"><span data-stu-id="4442e-137">**guidID**</span></span>
</dt> <dd>

<span data-ttu-id="4442e-138">Die GUID der letzten ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="4442e-138">The GUID of the last executable file.</span></span>

</dd> <dt>

<span data-ttu-id="4442e-139">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="4442e-139">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="4442e-140">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4442e-140">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4442e-141"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**Shimreg \_ \_Shim deaktivieren** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="4442e-141"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-142"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**Shimreg \_ \_AppHelp deaktivieren** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="4442e-142"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-143"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**Shimreg \_ AppHelp \_ NoUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="4442e-143"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-144"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**Shimreg \_ AppHelp \_ Abbrechen** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="4442e-144"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-145"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**Shimreg \_ \_SxS deaktivieren** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="4442e-145"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-146"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**Shimreg \_ \_Ebene deaktivieren** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="4442e-146"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="4442e-147"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**Shimreg \_ \_Treiber deaktivieren** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="4442e-147"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="4442e-148">**dwcustomsdbmap**</span><span class="sxs-lookup"><span data-stu-id="4442e-148">**dwCustomSDBMap**</span></span>
</dt> <dd>

<span data-ttu-id="4442e-149">Eine Zuordnung der benutzerdefinierten Shimdatenbanken.</span><span class="sxs-lookup"><span data-stu-id="4442e-149">A map of the custom shim databases.</span></span> <span data-ttu-id="4442e-150">Wenn **rgguiddb** gültig ist, werden die entsprechenden Bits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4442e-150">The corresponding bits are set if **rgGuidDB** is valid.</span></span>

</dd> <dt>

<span data-ttu-id="4442e-151">**rgguiddb**</span><span class="sxs-lookup"><span data-stu-id="4442e-151">**rgGuidDB**</span></span>
</dt> <dd>

<span data-ttu-id="4442e-152">Die GUIDs der Shimdatenbanken.</span><span class="sxs-lookup"><span data-stu-id="4442e-152">The GUIDs of the shim databases.</span></span> <span data-ttu-id="4442e-153">Beachten Sie, dass **Maximale SDB- \_ \_ SDSB** als 16 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4442e-153">Note that **SDB\_MAX\_SDBS** is defined as 16.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4442e-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4442e-154">Requirements</span></span>



| <span data-ttu-id="4442e-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4442e-155">Requirement</span></span> | <span data-ttu-id="4442e-156">Wert</span><span class="sxs-lookup"><span data-stu-id="4442e-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4442e-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4442e-157">Minimum supported client</span></span><br/> | <span data-ttu-id="4442e-158">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4442e-158">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4442e-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4442e-159">Minimum supported server</span></span><br/> | <span data-ttu-id="4442e-160">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4442e-160">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4442e-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4442e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4442e-162">**Sdbgetmatchingexe**</span><span class="sxs-lookup"><span data-stu-id="4442e-162">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> </dl>

 

 




