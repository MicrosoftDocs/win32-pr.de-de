---
description: Die Struktur "expertenumschlag Info" enthält Informationen über den Experten.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: Expertensequenz Info-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTENUMINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 35b8d36f55838492eb71640228d7216e6e594738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343232"
---
# <a name="expertenuminfo-structure"></a><span data-ttu-id="53a10-103">Expertensequenz Info-Struktur</span><span class="sxs-lookup"><span data-stu-id="53a10-103">EXPERTENUMINFO structure</span></span>

<span data-ttu-id="53a10-104">Die Struktur " **expertenumschlag Info** " enthält Informationen über den Experten.</span><span class="sxs-lookup"><span data-stu-id="53a10-104">The **EXPERTENUMINFO** structure provides information about the expert.</span></span> <span data-ttu-id="53a10-105">Netzwerkmonitor weist der Struktur Arbeitsspeicher zu und übergibt sie an den Experten, wenn die Register- [**expertenfunktion**](register-expert.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="53a10-105">Network Monitor allocates memory for the structure, and passes it to the expert when it calls the [**Register Expert**](register-expert.md) function.</span></span> <span data-ttu-id="53a10-106">Wenn der Experte die Struktur empfängt, muss er alle Informationen ausfüllen, die Netzwerkmonitor Anforderungen sind.</span><span class="sxs-lookup"><span data-stu-id="53a10-106">When the expert receives the structure, it must then fill-in all the information that Network Monitor requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a10-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="53a10-107">Syntax</span></span>


```C++
typedef struct {
  char                szName[EXPERTSTRINGLENGTH];
  char                szVendor[EXPERTSTRINGLENGTH];
  char                szDescription[EXPERTSTRINGLENGTH];
  DWORD               Version;
  DWORD               Flags;
  HEXPERT             hExpert;
  char                szDllName[MAX_PATH];
  HINSTANCE           hModule;
  PEXPERTREGISTERPROC pRegisterProc;
  PEXPERTCONFIGPROC   pConfigProc;
  PEXPERTRUNPROC      pRunProc;
} EXPERTENUMINFO, *PEXPERTENUMINFO;
```



## <a name="members"></a><span data-ttu-id="53a10-108">Member</span><span class="sxs-lookup"><span data-stu-id="53a10-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="53a10-109">**szName**</span><span class="sxs-lookup"><span data-stu-id="53a10-109">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="53a10-110">Der Name des Experten.</span><span class="sxs-lookup"><span data-stu-id="53a10-110">Name of the expert.</span></span>

</dd> <dt>

<span data-ttu-id="53a10-111">**szvendor**</span><span class="sxs-lookup"><span data-stu-id="53a10-111">**szVendor**</span></span>
</dt> <dd>

<span data-ttu-id="53a10-112">Der Name des Herstellers, der den Experten erstellt.</span><span class="sxs-lookup"><span data-stu-id="53a10-112">Name of the vendor that creates the expert.</span></span>

</dd> <dt>

<span data-ttu-id="53a10-113">**szDescription**</span><span class="sxs-lookup"><span data-stu-id="53a10-113">**szDescription**</span></span>
</dt> <dd>

<span data-ttu-id="53a10-114">Die Beschreibung des Experten.</span><span class="sxs-lookup"><span data-stu-id="53a10-114">Description of the expert.</span></span> <span data-ttu-id="53a10-115">Der Wert des **szDescription** -Members kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="53a10-115">The value of the **szDescription** member may be **NULL**.</span></span> <span data-ttu-id="53a10-116">Wenn der Name zu lang ist, wird er in der Standard-Viewer-Konfiguration abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="53a10-116">If the name is too long, it is truncated in the default viewer configuration.</span></span>

</dd> <dt>

<span data-ttu-id="53a10-117">**Version**</span><span class="sxs-lookup"><span data-stu-id="53a10-117">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="53a10-118">Der Wert muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="53a10-118">The value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="53a10-119">**Flags**</span><span class="sxs-lookup"><span data-stu-id="53a10-119">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="53a10-120">Die folgenden Flags beschreiben den Experten.</span><span class="sxs-lookup"><span data-stu-id="53a10-120">The following flags describe the expert.</span></span>



| <span data-ttu-id="53a10-121">Wert</span><span class="sxs-lookup"><span data-stu-id="53a10-121">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="53a10-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="53a10-122">Meaning</span></span>                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <span data-ttu-id="53a10-123"><dt>**kennflag für expertenaufzählung \_ \_ \_ konfigurierbar**</dt></span><span class="sxs-lookup"><span data-stu-id="53a10-123"><dt>**EXPERT\_ENUM\_FLAG\_CONFIGURABLE**</dt></span></span> </dl>                                          | <span data-ttu-id="53a10-124">Der Experte unterstützt Aufrufe der [**configure**](configure.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="53a10-124">The expert supports calls to the [**Configure**](configure.md) method.</span></span> <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <span data-ttu-id="53a10-125"><dt>**Experte-Aufzählungs- \_ \_ Flag- \_ Viewer \_ Privat**</dt></span><span class="sxs-lookup"><span data-stu-id="53a10-125"><dt>**EXPERT\_ENUM\_FLAG\_VIEWER\_PRIVATE**</dt></span></span> </dl>                                   | <span data-ttu-id="53a10-126">Der Experte erfordert eine private (nicht freigegebene) Ereignisanzeige.</span><span class="sxs-lookup"><span data-stu-id="53a10-126">The expert requires a private (non-shared) Event Viewer.</span></span> <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <span data-ttu-id="53a10-127"><dt>**expertenaufzählungs \_ \_ Flag \_ No \_ Viewer**</dt></span><span class="sxs-lookup"><span data-stu-id="53a10-127"><dt>**EXPERT\_ENUM\_FLAG\_NO\_VIEWER**</dt></span></span> </dl>                                                  | <span data-ttu-id="53a10-128">Der Experte sendet keine Ereignis Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="53a10-128">The expert does not send event notifications.</span></span> <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <span data-ttu-id="53a10-129"><dt>**expertenaufzählungs \_ \_ Flag " \_ \_ \_ \_ RMC \_ \_ zusammenfassen"**</dt></span><span class="sxs-lookup"><span data-stu-id="53a10-129"><dt>**EXPERT\_ENUM\_FLAG\_ADD\_ME\_TO\_RMC\_IN\_SUMMARY**</dt></span></span> </dl> | <span data-ttu-id="53a10-130">Wenn sich der Fokus im Zusammenfassungs Bereich befindet, wird der Experte im Kontextmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="53a10-130">When the focus is in the summary pane, the expert appears on the context menu.</span></span> <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <span data-ttu-id="53a10-131"><dt>**expertenaufzählungs \_ \_ Flag " \_ \_ \_ \_ RMC \_ im \_ Detail hinzufügen"**</dt></span><span class="sxs-lookup"><span data-stu-id="53a10-131"><dt>**EXPERT\_ENUM\_FLAG\_ADD\_ME\_TO\_RMC\_IN\_DETAIL**</dt></span></span> </dl>    | <span data-ttu-id="53a10-132">Wenn sich der Fokus im Detailbereich befindet, wird der Experte im Kontextmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="53a10-132">When the focus is in the detail pane, the expert appears on the context menu.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="53a10-133">**hexpert**</span><span class="sxs-lookup"><span data-stu-id="53a10-133">**hExpert**</span></span>
</dt> <dd>

<span data-ttu-id="53a10-134">Handle für den Experten.</span><span class="sxs-lookup"><span data-stu-id="53a10-134">Handle to the expert.</span></span> <span data-ttu-id="53a10-135">Wenn die **expertenwert** -Struktur verwendet wird, um einen Experten zu registrieren, wird der-Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="53a10-135">When the **EXPERTENUMINFO** structure is used to register an expert, the parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="53a10-136">**szDllName**</span><span class="sxs-lookup"><span data-stu-id="53a10-136">**szDllName**</span></span>
</dt> <dd>

<span data-ttu-id="53a10-137">Privates Mitglied; Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="53a10-137">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="53a10-138">**HMODULE**</span><span class="sxs-lookup"><span data-stu-id="53a10-138">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="53a10-139">Privates Mitglied; Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="53a10-139">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="53a10-140">**pregisterproc**</span><span class="sxs-lookup"><span data-stu-id="53a10-140">**pRegisterProc**</span></span>
</dt> <dd>

<span data-ttu-id="53a10-141">Privates Mitglied; Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="53a10-141">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="53a10-142">**pconfigproc**</span><span class="sxs-lookup"><span data-stu-id="53a10-142">**pConfigProc**</span></span>
</dt> <dd>

<span data-ttu-id="53a10-143">Privates Mitglied; Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="53a10-143">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="53a10-144">**prunproc**</span><span class="sxs-lookup"><span data-stu-id="53a10-144">**pRunProc**</span></span>
</dt> <dd>

<span data-ttu-id="53a10-145">Privates Mitglied; Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="53a10-145">Private member; do not use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53a10-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53a10-146">Requirements</span></span>



| <span data-ttu-id="53a10-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53a10-147">Requirement</span></span> | <span data-ttu-id="53a10-148">Wert</span><span class="sxs-lookup"><span data-stu-id="53a10-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="53a10-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53a10-149">Minimum supported client</span></span><br/> | <span data-ttu-id="53a10-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53a10-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="53a10-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53a10-151">Minimum supported server</span></span><br/> | <span data-ttu-id="53a10-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53a10-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="53a10-153">Header</span><span class="sxs-lookup"><span data-stu-id="53a10-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="53a10-154"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="53a10-154"><dt>Netmon.h</dt></span></span> </dl> |



 

 




