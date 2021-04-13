---
title: IDWriteFont2-Schnittstelle
description: Stellt eine physische Schriftart in einer Schriftart Auflistung dar.
ms.assetid: 4E3069AE-5882-4A26-A36D-BE7D7EE1B0C3
keywords:
- IDWriteFont2 Interface Direct Write
- IDWriteFont2 Interface Direct Write, beschrieben
topic_type:
- apiref
api_name:
- IDWriteFont2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82a47e56915747b0e118a6f63484b9dd3dcdbd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340838"
---
# <a name="idwritefont2-interface"></a><span data-ttu-id="1316b-105">IDWriteFont2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1316b-105">IDWriteFont2 interface</span></span>

<span data-ttu-id="1316b-106">Stellt eine physische Schriftart in einer Schriftart Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="1316b-106">Represents a physical font in a font collection.</span></span>

<span data-ttu-id="1316b-107">Diese Schnittstelle bietet die Möglichkeit, zu überprüfen, ob möglicherweise ein farbrenderingpfad erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1316b-107">This interface adds the ability to check if a color rendering path is potentially necessary.</span></span>

## <a name="members"></a><span data-ttu-id="1316b-108">Member</span><span class="sxs-lookup"><span data-stu-id="1316b-108">Members</span></span>

<span data-ttu-id="1316b-109">Die **IDWriteFont2** -Schnittstelle erbt von [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1).</span><span class="sxs-lookup"><span data-stu-id="1316b-109">The **IDWriteFont2** interface inherits from [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1).</span></span> <span data-ttu-id="1316b-110">**IDWriteFont2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1316b-110">**IDWriteFont2** also has these types of members:</span></span>

-   [<span data-ttu-id="1316b-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="1316b-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1316b-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="1316b-112">Methods</span></span>

<span data-ttu-id="1316b-113">Die **IDWriteFont2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1316b-113">The **IDWriteFont2** interface has these methods.</span></span>



| <span data-ttu-id="1316b-114">Methode</span><span class="sxs-lookup"><span data-stu-id="1316b-114">Method</span></span>                                          | <span data-ttu-id="1316b-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1316b-115">Description</span></span>                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="1316b-116">**Iscolorfont**</span><span class="sxs-lookup"><span data-stu-id="1316b-116">**IsColorFont**</span></span>](idwritefont2-iscolorfont.md) | <span data-ttu-id="1316b-117">Ermöglicht die Ermittlung, ob ein farbrenderingpfad möglicherweise erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1316b-117">Enables determining if a color rendering path is potentially necessary.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1316b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1316b-118">Requirements</span></span>



| <span data-ttu-id="1316b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1316b-119">Requirement</span></span> | <span data-ttu-id="1316b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1316b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1316b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1316b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1316b-122">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1316b-122">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="1316b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1316b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1316b-124">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1316b-124">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="1316b-125">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="1316b-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="1316b-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="1316b-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="1316b-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1316b-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="1316b-128"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1316b-128"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1316b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1316b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1316b-130"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1316b-130"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1316b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1316b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1316b-132">**IDWriteFont1**</span><span class="sxs-lookup"><span data-stu-id="1316b-132">**IDWriteFont1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
</dt> </dl>

 

