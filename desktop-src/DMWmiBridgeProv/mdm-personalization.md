---
title: MDM_Personalization-Klasse
description: Die MDM \_ -Personalisierungs Klasse wird verwendet, um den Sperrbildschirm und die Desktop Hintergrundbilder festzulegen. Durch Festlegen dieser Richtlinien wird auch verhindert, dass der Benutzer das Image ändert.
ms.assetid: 99b60767-b321-4ec6-9802-76221d26c830
keywords:
- MDM_Personalization-Klasse
- MDM_Personalization-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Personalization
- MDM_Personalization.InstanceID
- MDM_Personalization.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78986422cce15d750e1ae678aef352bbb369bfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949683"
---
# <a name="mdm_personalization-class"></a><span data-ttu-id="3492c-106">MDM- \_ Personalisierungs Klasse</span><span class="sxs-lookup"><span data-stu-id="3492c-106">MDM\_Personalization class</span></span>

<span data-ttu-id="3492c-107">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="3492c-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3492c-108">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="3492c-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3492c-109">Die MDM \_ -Personalisierungs Klasse wird verwendet, um den Sperrbildschirm und die Desktop Hintergrundbilder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3492c-109">The MDM\_Personalization class is used to set the lock screen and desktop background images.</span></span> <span data-ttu-id="3492c-110">Durch Festlegen dieser Richtlinien wird auch verhindert, dass der Benutzer das Image ändert.</span><span class="sxs-lookup"><span data-stu-id="3492c-110">Setting these policies also prevents the user from changing the image.</span></span>

<span data-ttu-id="3492c-111">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="3492c-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3492c-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="3492c-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Personalization
{
  string InstanceID;
  string ParentID;
  string DesktopImageUrl;
  sint32 DesktopImageStatus;
  string LockScreenImageUrl;
  sint32 LockScreenImageStatus;
};
```

## <a name="members"></a><span data-ttu-id="3492c-113">Member</span><span class="sxs-lookup"><span data-stu-id="3492c-113">Members</span></span>

<span data-ttu-id="3492c-114">Die **MDM- \_ Personalisierungs** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3492c-114">The **MDM\_Personalization** class has these types of members:</span></span>

-   [<span data-ttu-id="3492c-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3492c-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3492c-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3492c-116">Properties</span></span>

<span data-ttu-id="3492c-117">Die **MDM- \_ Personalisierungs** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3492c-117">The **MDM\_Personalization** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3492c-118">Desktopimagestatus</span><span class="sxs-lookup"><span data-stu-id="3492c-118">DesktopImageStatus</span></span>](/windows/client-management/mdm/personalization-csp#desktopimagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3492c-119">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3492c-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3492c-120">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3492c-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3492c-121">Desktopimageurl</span><span class="sxs-lookup"><span data-stu-id="3492c-121">DesktopImageUrl</span></span>](/windows/client-management/mdm/personalization-csp#desktopimageurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3492c-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3492c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3492c-123">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3492c-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3492c-124">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3492c-124">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3492c-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3492c-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3492c-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3492c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3492c-127">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3492c-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3492c-128">Lockscreenimagestatus</span><span class="sxs-lookup"><span data-stu-id="3492c-128">LockScreenImageStatus</span></span>](/windows/client-management/mdm/personalization-csp#lockscreenimagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3492c-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3492c-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3492c-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3492c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3492c-131">Lockscreenimageurl</span><span class="sxs-lookup"><span data-stu-id="3492c-131">LockScreenImageUrl</span></span>](/windows/client-management/mdm/personalization-csp#lockscreenimageurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3492c-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3492c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3492c-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3492c-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3492c-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3492c-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3492c-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3492c-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3492c-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3492c-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3492c-137">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3492c-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3492c-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3492c-138">Requirements</span></span>



| <span data-ttu-id="3492c-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3492c-139">Requirement</span></span> | <span data-ttu-id="3492c-140">Wert</span><span class="sxs-lookup"><span data-stu-id="3492c-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3492c-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3492c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3492c-142">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3492c-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3492c-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3492c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3492c-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3492c-144">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="3492c-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="3492c-145">Namespace</span></span><br/>                | <span data-ttu-id="3492c-146">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="3492c-146">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="3492c-147">MOF</span><span class="sxs-lookup"><span data-stu-id="3492c-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3492c-148"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3492c-148"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="3492c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="3492c-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3492c-150"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3492c-150"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

