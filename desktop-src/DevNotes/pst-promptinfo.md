---
description: Definiert das Aufforderungs Verhalten des geschützten Speicher, wenn eine Benutzeroberfläche angezeigt wird.
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: PST_PROMPTINFO Struktur (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_PROMPTINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: da499ea3d6f5037e9f1e745771112840a462f11d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368423"
---
# <a name="pst_promptinfo-structure"></a><span data-ttu-id="5f607-103">PST \_ promptinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="5f607-103">PST\_PROMPTINFO structure</span></span>

<span data-ttu-id="5f607-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5f607-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="5f607-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5f607-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="5f607-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="5f607-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="5f607-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="5f607-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="5f607-108">Definiert das Aufforderungs Verhalten des geschützten Speicher, wenn eine Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5f607-108">Defines the prompting behavior of the Protected Store whenever it displays a user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f607-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f607-109">Syntax</span></span>


```C++
typedef struct {
  DWORD      cbSize;
  DWORD      dwPromptFlags;
  DWORD_PTR  hwndApp;
  LPCWSTR    szPrompt;
} PST_PROMPTINFO, *PPST_PROMPTINFO;
```



## <a name="members"></a><span data-ttu-id="5f607-110">Member</span><span class="sxs-lookup"><span data-stu-id="5f607-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="5f607-111">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="5f607-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="5f607-112">Die Größe dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="5f607-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="5f607-113">**dwpromptflags**</span><span class="sxs-lookup"><span data-stu-id="5f607-113">**dwPromptFlags**</span></span>
</dt> <dd>

<span data-ttu-id="5f607-114">Dieses Flag wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5f607-114">This flag is ignored.</span></span>



| <span data-ttu-id="5f607-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5f607-115">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="5f607-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5f607-116">Meaning</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> <span data-ttu-id="5f607-117"><dt>**PST \_ PF \_ \_ zeigt immer**</dt> <dt>0x00000001</dt> an</span><span class="sxs-lookup"><span data-stu-id="5f607-117"><dt>**PST\_PF\_ALWAYS\_SHOW**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="5f607-118">Fordert an, dass der Anbieter das Eingabe Aufforderungs Dialogfeld für den Benutzer anzeigt, auch wenn es für diesen Zugriff nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5f607-118">Requests that the provider show the prompt dialog to the user even if it is not required for this access.</span></span> <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> <span data-ttu-id="5f607-119"><dt>**PST \_ PF \_ \_ zeigt nie**</dt> <dt>0x00000002</dt> an</span><span class="sxs-lookup"><span data-stu-id="5f607-119"><dt>**PST\_PF\_NEVER\_SHOW**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="5f607-120">Zeigen Sie dem Benutzer nicht das Dialogfeld für die Eingabeaufforderung an.</span><span class="sxs-lookup"><span data-stu-id="5f607-120">Do not show the prompt dialog to the user.</span></span><br/>                                                                 |



 

</dd> <dt>

<span data-ttu-id="5f607-121">**hwndApp**</span><span class="sxs-lookup"><span data-stu-id="5f607-121">**hwndApp**</span></span>
</dt> <dd>

<span data-ttu-id="5f607-122">Das Handle für das übergeordnete Fenster für die Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="5f607-122">The handle to the parent window for the user interface.</span></span> <span data-ttu-id="5f607-123">Das **hwndApp** -Element bestimmt, wo die Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5f607-123">The **hwndApp** member determines where the user interface appears.</span></span> <span data-ttu-id="5f607-124">Wenn **null** übermittelt wird, wird der Desktop als übergeordnetes Fenster betrachtet.</span><span class="sxs-lookup"><span data-stu-id="5f607-124">If **NULL** is passed, the desktop is considered to be the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="5f607-125">**szprompt**</span><span class="sxs-lookup"><span data-stu-id="5f607-125">**szPrompt**</span></span>
</dt> <dd>

<span data-ttu-id="5f607-126">Die Zeichenfolge der Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="5f607-126">The prompt string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f607-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f607-127">Requirements</span></span>



| <span data-ttu-id="5f607-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f607-128">Requirement</span></span> | <span data-ttu-id="5f607-129">Wert</span><span class="sxs-lookup"><span data-stu-id="5f607-129">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5f607-130">Header</span><span class="sxs-lookup"><span data-stu-id="5f607-130">Header</span></span><br/> | <dl> <span data-ttu-id="5f607-131"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f607-131"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f607-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f607-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f607-133">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="5f607-133">**DeleteItem**</span></span>](ipstore-deleteitem.md)
</dt> <dt>

[<span data-ttu-id="5f607-134">**OpenItem**</span><span class="sxs-lookup"><span data-stu-id="5f607-134">**OpenItem**</span></span>](ipstore-openitem.md)
</dt> <dt>

[<span data-ttu-id="5f607-135">**"ReadItem"**</span><span class="sxs-lookup"><span data-stu-id="5f607-135">**ReadItem**</span></span>](ipstore-readitem.md)
</dt> <dt>

[<span data-ttu-id="5f607-136">**Schreib Element**</span><span class="sxs-lookup"><span data-stu-id="5f607-136">**WriteItem**</span></span>](ipstore-writeitem.md)
</dt> </dl>

 

 
