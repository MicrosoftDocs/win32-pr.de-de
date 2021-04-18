---
title: PICTYPE-Konstanten (OLECTL. h)
description: Beschreiben Sie den Typ eines Bildobjekts, das vom IPicture Get-Typ zurückgegeben \_ wird, und, um den Bildtyp im PICTYPE-Member der PICTDESC-Struktur zu beschreiben, die an olecreatepictureindirekte weitergeleitet wird.
ms.assetid: 79f10687-f0eb-4b5e-a1a9-9186dbd0b51f
topic_type:
- apiref
api_name:
- PICTYPE_UNINITIALIZED
- PICTYPE_NONE
- PICTYPE_BITMAP
- PICTYPE_METAFILE
- PICTYPE_ICON
- PICTYPE_ENHMETAFILE
api_location:
- OleCtl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebf8ad8f678e9b6e463ade9f149b2e1d4bab529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340575"
---
# <a name="pictype-constants"></a><span data-ttu-id="80d39-103">PICTYPE-Konstanten</span><span class="sxs-lookup"><span data-stu-id="80d39-103">PICTYPE Constants</span></span>

<span data-ttu-id="80d39-104">Beschreiben Sie den Typ eines Bildobjekts, das vom [**IPicture:: get- \_ Typ**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)zurückgegeben wird, und, um den Bildtyp im **PICTYPE** -Member der [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) -Struktur zu beschreiben, die an [**olecreatepictureindirekte**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="80d39-104">Describe the type of a picture object as returned by [**IPicture::get\_Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), as well as to describe the type of picture in the **picType** member of the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure that is passed to [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span></span>



| <span data-ttu-id="80d39-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="80d39-105">Constant/value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="80d39-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80d39-106">Description</span></span>                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <span data-ttu-id="80d39-107"><dt>**PICTYPE \_ Nicht initialisiert**</dt> <dt>(-1)</dt></span><span class="sxs-lookup"><span data-stu-id="80d39-107"><dt>**PICTYPE\_UNINITIALIZED**</dt> <dt>(-1)</dt></span></span> </dl> | <span data-ttu-id="80d39-108">Das Bild Objekt ist derzeit nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="80d39-108">The picture object is currently uninitialized.</span></span> <span data-ttu-id="80d39-109">Dieser Wert ist nur als Rückgabewert des [**IPicture:: get- \_ Typs**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) gültig und mit der [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) -Struktur ungültig.</span><span class="sxs-lookup"><span data-stu-id="80d39-109">This value is only valid as a return value from [**IPicture::get\_Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) and is not valid with the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure.</span></span><br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <span data-ttu-id="80d39-110"><dt>**PICTYPE \_ Keine**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="80d39-110"><dt>**PICTYPE\_NONE**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="80d39-111">Ein neues Bild Objekt soll ohne Initialisierungs Zustand erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="80d39-111">A new picture object is to be created without an initialized state.</span></span> <span data-ttu-id="80d39-112">Dieser Wert ist nur in der [**pictde**](/windows/win32/api/olectl/ns-olectl-pictdesc) -Struktur gültig.</span><span class="sxs-lookup"><span data-stu-id="80d39-112">This value is valid only in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure.</span></span><br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <span data-ttu-id="80d39-113"><dt>**PICTYPE \_ Bitmap**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="80d39-113"><dt>**PICTYPE\_BITMAP**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="80d39-114">Der Bildtyp ist eine Bitmap.</span><span class="sxs-lookup"><span data-stu-id="80d39-114">The picture type is a bitmap.</span></span> <span data-ttu-id="80d39-115">Wenn dieser Wert in der [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) -Struktur auftritt, bedeutet dies, dass das **BMP** -Feld dieser Struktur die relevanten Initialisierungs Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="80d39-115">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **bmp** field of that structure contains the relevant initialization parameters.</span></span><br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <span data-ttu-id="80d39-116"><dt>**PICTYPE \_ Metadatei**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="80d39-116"><dt>**PICTYPE\_METAFILE**</dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="80d39-117">Der Bildtyp ist eine Metadatei.</span><span class="sxs-lookup"><span data-stu-id="80d39-117">The picture type is a metafile.</span></span> <span data-ttu-id="80d39-118">Wenn dieser Wert in der [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) -Struktur auftritt, bedeutet dies, dass das **WMF** -Feld dieser Struktur die relevanten Initialisierungs Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="80d39-118">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **wmf** field of that structure contains the relevant initialization parameters.</span></span><br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <span data-ttu-id="80d39-119"><dt>**PICTYPE \_ Symbol**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="80d39-119"><dt>**PICTYPE\_ICON**</dt> <dt>3</dt></span></span> </dl>                               | <span data-ttu-id="80d39-120">Der Bildtyp ist ein Symbol.</span><span class="sxs-lookup"><span data-stu-id="80d39-120">The picture type is an icon.</span></span> <span data-ttu-id="80d39-121">Wenn dieser Wert in der [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) -Struktur auftritt, bedeutet dies, dass das **Symbol** Feld dieser Struktur die relevanten Initialisierungs Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="80d39-121">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **icon** field of that structure contains the relevant initialization parameters.</span></span><br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <span data-ttu-id="80d39-122"><dt>**PICTYPE \_ Enhmetafile**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="80d39-122"><dt>**PICTYPE\_ENHMETAFILE**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="80d39-123">Der Bildtyp ist eine erweiterte Metadatei.</span><span class="sxs-lookup"><span data-stu-id="80d39-123">The picture type is an enhanced metafile.</span></span> <span data-ttu-id="80d39-124">Wenn dieser Wert in der [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) -Struktur auftritt, bedeutet dies, dass das **EMF** -Feld dieser Struktur die relevanten Initialisierungs Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="80d39-124">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **emf** field of that structure contains the relevant initialization parameters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="80d39-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80d39-125">Requirements</span></span>



| <span data-ttu-id="80d39-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80d39-126">Requirement</span></span> | <span data-ttu-id="80d39-127">Wert</span><span class="sxs-lookup"><span data-stu-id="80d39-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="80d39-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80d39-128">Minimum supported client</span></span><br/> | <span data-ttu-id="80d39-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80d39-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="80d39-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80d39-130">Minimum supported server</span></span><br/> | <span data-ttu-id="80d39-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80d39-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="80d39-132">Header</span><span class="sxs-lookup"><span data-stu-id="80d39-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="80d39-133"><dt>OLECTL. h</dt></span><span class="sxs-lookup"><span data-stu-id="80d39-133"><dt>OleCtl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80d39-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80d39-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80d39-135">**IPicture:: get- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="80d39-135">**IPicture::get\_Type**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[<span data-ttu-id="80d39-136">**Olecreatepictureindirekte**</span><span class="sxs-lookup"><span data-stu-id="80d39-136">**OleCreatePictureIndirect**</span></span>](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[<span data-ttu-id="80d39-137">**Pictde**</span><span class="sxs-lookup"><span data-stu-id="80d39-137">**PICTDESC**</span></span>](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





