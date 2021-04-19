---
title: Wmdmrights-Struktur
description: Die wmdmrights-Struktur beschreibt Inhalts Nutzungsrechte.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- Wmdmrights-Struktur Windows Media Device Manager
- Pwmdmrights-Struktur Zeiger Windows Media-Device Manager
topic_type:
- apiref
api_name:
- WMDMRIGHTS
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8bc3bcd61efc64d32daa3179b77a9aaa518d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350784"
---
# <a name="wmdmrights-structure"></a><span data-ttu-id="97028-105">Wmdmrights-Struktur</span><span class="sxs-lookup"><span data-stu-id="97028-105">WMDMRIGHTS structure</span></span>

<span data-ttu-id="97028-106">Die **wmdmrights** -Struktur beschreibt Inhalts Nutzungsrechte.</span><span class="sxs-lookup"><span data-stu-id="97028-106">The **WMDMRIGHTS** structure describes content-use rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="97028-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="97028-107">Syntax</span></span>


```C++
typedef struct __WMDMRIGHTS {
  UINT         cbSize;
  DWORD        dwContentType;
  DWORD        fuFlags;
  DWORD        fuRights;
  DWORD        dwAppSec;
  DWORD        dwPlaybackCount;
  WMDMDATETIME ExpirationDate;
} WMDMRIGHTS, *PWMDMRIGHTS;
```



## <a name="members"></a><span data-ttu-id="97028-108">Member</span><span class="sxs-lookup"><span data-stu-id="97028-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="97028-109">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="97028-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="97028-110">Größe der Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="97028-110">Size of the structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="97028-111">**dwcontenttype**</span><span class="sxs-lookup"><span data-stu-id="97028-111">**dwContentType**</span></span>
</dt> <dd>

<span data-ttu-id="97028-112">**DWORD** , das den Inhaltstyp enthält.</span><span class="sxs-lookup"><span data-stu-id="97028-112">**DWORD** containing the type of content.</span></span>

</dd> <dt>

<span data-ttu-id="97028-113">**fuflags**</span><span class="sxs-lookup"><span data-stu-id="97028-113">**fuFlags**</span></span>
</dt> <dd>

<span data-ttu-id="97028-114">Bitfeld, das die Rechte Optionen angibt, die für den Inhalt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97028-114">Bit field specifying the rights options in use for the content.</span></span>



| <span data-ttu-id="97028-115">Wert</span><span class="sxs-lookup"><span data-stu-id="97028-115">Value</span></span>                        | <span data-ttu-id="97028-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97028-116">Description</span></span>                                  |
|------------------------------|----------------------------------------------|
| <span data-ttu-id="97028-117">playbackcount für WMDM- \_ Rechte \_</span><span class="sxs-lookup"><span data-stu-id="97028-117">WMDM\_RIGHTS\_PLAYBACKCOUNT</span></span>  | <span data-ttu-id="97028-118">Gibt an, wie oft die Datei wiedergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="97028-118">Number of times that the file can be played.</span></span> |
| <span data-ttu-id="97028-119">WMDM- \_ Rechte \_ ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="97028-119">WMDM\_RIGHTS\_EXPIRATIONDATE</span></span> | <span data-ttu-id="97028-120">Ablaufdatum der Datei.</span><span class="sxs-lookup"><span data-stu-id="97028-120">Expiration date of the file.</span></span>                 |
| <span data-ttu-id="97028-121">WMDM- \_ Rechte \_ freeserialids</span><span class="sxs-lookup"><span data-stu-id="97028-121">WMDM\_RIGHTS\_FREESERIALIDS</span></span>  | <span data-ttu-id="97028-122">Der freie serielle Bezeichner der Datei.</span><span class="sxs-lookup"><span data-stu-id="97028-122">Free serial identifier of the file.</span></span>          |
| <span data-ttu-id="97028-123">Gruppen für WMDM- \_ Rechte \_ Gruppen</span><span class="sxs-lookup"><span data-stu-id="97028-123">WMDM\_RIGHTS\_GROUPID Group</span></span>  | <span data-ttu-id="97028-124">Der Bezeichner der Datei.</span><span class="sxs-lookup"><span data-stu-id="97028-124">Identifier of the file.</span></span>                      |
| <span data-ttu-id="97028-125">WMDM- \_ Rechte \_ namedserialids</span><span class="sxs-lookup"><span data-stu-id="97028-125">WMDM\_RIGHTS\_NAMEDSERIALIDS</span></span> | <span data-ttu-id="97028-126">Der benannte serielle Bezeichner der Datei.</span><span class="sxs-lookup"><span data-stu-id="97028-126">Named serial identifier of the file.</span></span>         |



 

</dd> <dt>

<span data-ttu-id="97028-127">**furights**</span><span class="sxs-lookup"><span data-stu-id="97028-127">**fuRights**</span></span>
</dt> <dd>

<span data-ttu-id="97028-128">Bitfeld, das die Rechte Bits für den Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="97028-128">Bit field containing the rights bits for the content.</span></span>



| <span data-ttu-id="97028-129">Wert</span><span class="sxs-lookup"><span data-stu-id="97028-129">Value</span></span>                                     | <span data-ttu-id="97028-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97028-130">Description</span></span>                                   |
|-------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="97028-131">WMDM- \_ Rechte \_ spielen auf dem \_ \_ PC</span><span class="sxs-lookup"><span data-stu-id="97028-131">WMDM\_RIGHTS\_PLAY\_ON\_PC</span></span>                | <span data-ttu-id="97028-132">Inhalt kann auf einem PC wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="97028-132">Content can be played on a personal computer.</span></span> |
| <span data-ttu-id="97028-133">WMDM- \_ Rechte \_ Kopie \_ auf nicht- \_ \_ SDMI- \_ Gerät kopieren</span><span class="sxs-lookup"><span data-stu-id="97028-133">WMDM\_RIGHTS\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="97028-134">Der Inhalt kann auf ein nicht-SDMI-Gerät kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="97028-134">Content can be copied to a non-SDMI device.</span></span>   |
| <span data-ttu-id="97028-135">WMDM \_ - \_ Rechte \_ in \_ CD kopieren</span><span class="sxs-lookup"><span data-stu-id="97028-135">WMDM\_RIGHTS\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="97028-136">Der Inhalt kann auf eine CD kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="97028-136">Content can be copied to a CD.</span></span>                |
| <span data-ttu-id="97028-137">WMDM- \_ Rechte \_ Kopie \_ auf \_ SDMI- \_ Gerät kopieren</span><span class="sxs-lookup"><span data-stu-id="97028-137">WMDM\_RIGHTS\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="97028-138">Der Inhalt kann auf ein SDMI-Gerät kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="97028-138">Content can be copied to an SDMI device.</span></span>      |



 

</dd> <dt>

<span data-ttu-id="97028-139">**dwappsec**</span><span class="sxs-lookup"><span data-stu-id="97028-139">**dwAppSec**</span></span>
</dt> <dd>

<span data-ttu-id="97028-140">Bytearray, das die minimale Ebene der Anwendungssicherheit angibt.</span><span class="sxs-lookup"><span data-stu-id="97028-140">Byte array that specifies the minimum level of application security.</span></span>

</dd> <dt>

<span data-ttu-id="97028-141">**dwplaybackcount**</span><span class="sxs-lookup"><span data-stu-id="97028-141">**dwPlaybackCount**</span></span>
</dt> <dd>

<span data-ttu-id="97028-142">**DWORD** , das die Anzahl der verbleibenden Zeiten enthält, zu denen der Inhalt gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="97028-142">**DWORD** containing the number of remaining times that the content can be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="97028-143">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="97028-143">**ExpirationDate**</span></span>
</dt> <dd>

<span data-ttu-id="97028-144">Die [**wmdmdatetime**](wmdmdatetime.md) -Struktur, die das Ablaufdatum und die Ablaufzeit für den Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="97028-144">[**WMDMDATETIME**](wmdmdatetime.md) structure containing the expiration date and time for the content.</span></span> <span data-ttu-id="97028-145">Wenn die Lizenz kein Ablaufdatum hat, wird das **wYear** -Element auf 0xFFFF festgelegt, und alle anderen Member von **wmdmdatetime** werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="97028-145">If the license has no expiration date, the **wYear** member is set to 0xFFFF, and all other members of **WMDMDATETIME** are ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97028-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97028-146">Requirements</span></span>



| <span data-ttu-id="97028-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97028-147">Requirement</span></span> | <span data-ttu-id="97028-148">Wert</span><span class="sxs-lookup"><span data-stu-id="97028-148">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="97028-149">Header</span><span class="sxs-lookup"><span data-stu-id="97028-149">Header</span></span><br/> | <dl> <span data-ttu-id="97028-150"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97028-150"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97028-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97028-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97028-152">**Imdspstorage:: GetRights**</span><span class="sxs-lookup"><span data-stu-id="97028-152">**IMDSPStorage::GetRights**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[<span data-ttu-id="97028-153">**Iwmdmstorage:: GetRights**</span><span class="sxs-lookup"><span data-stu-id="97028-153">**IWMDMStorage::GetRights**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[<span data-ttu-id="97028-154">**Wmdmdatetime**</span><span class="sxs-lookup"><span data-stu-id="97028-154">**WMDMDATETIME**</span></span>](wmdmdatetime.md)
</dt> <dt>

[<span data-ttu-id="97028-155">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="97028-155">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





