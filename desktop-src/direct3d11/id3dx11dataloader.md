---
title: ID3DX11DataLoader-Schnittstelle (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Datenlade Objekt, das von der ID3DX11ThreadPump-Schnittstelle zum asynchronen Laden von Daten verwendet wird
ms.assetid: 878929ea-0228-4650-9ca0-f83d60d9f915
keywords:
- ID3DX11DataLoader-Schnittstelle Direct3D 11
- ID3DX11DataLoader Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11DataLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68236451bf2ba6f491d17541f7d4ca627f5063c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103071"
---
# <a name="id3dx11dataloader-interface"></a><span data-ttu-id="48eef-106">ID3DX11DataLoader-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="48eef-106">ID3DX11DataLoader interface</span></span>

> [!Note]  
> <span data-ttu-id="48eef-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48eef-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="48eef-108">Datenlade Objekt, das von der [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md) zum asynchronen Laden von Daten verwendet wird</span><span class="sxs-lookup"><span data-stu-id="48eef-108">Data loading object used by [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md) for loading data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="48eef-109">Member</span><span class="sxs-lookup"><span data-stu-id="48eef-109">Members</span></span>

<span data-ttu-id="48eef-110">Die **ID3DX11DataLoader** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="48eef-110">The **ID3DX11DataLoader** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="48eef-111">**ID3DX11DataLoader** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="48eef-111">**ID3DX11DataLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="48eef-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="48eef-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="48eef-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="48eef-113">Methods</span></span>

<span data-ttu-id="48eef-114">Die **ID3DX11DataLoader** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="48eef-114">The **ID3DX11DataLoader** interface has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="48eef-115">Methode</span><span class="sxs-lookup"><span data-stu-id="48eef-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="48eef-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48eef-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="48eef-117"><a href="id3dx11dataloader-decompress.md"><strong>Dekomprimieren</strong></a></span><span class="sxs-lookup"><span data-stu-id="48eef-117"><a href="id3dx11dataloader-decompress.md"><strong>Decompress</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="48eef-118">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48eef-118">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="48eef-119">Decodiert codierte Daten.</span><span class="sxs-lookup"><span data-stu-id="48eef-119">Decompresses encoded data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="48eef-120"><a href="id3dx11dataloader-destroy.md"><strong>Zerstören</strong></a></span><span class="sxs-lookup"><span data-stu-id="48eef-120"><a href="id3dx11dataloader-destroy.md"><strong>Destroy</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="48eef-121">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48eef-121">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="48eef-122">Zerstört das Lade Modul, nachdem ein Arbeits Element abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="48eef-122">Destroys the loader after a work item completes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="48eef-123"><a href="id3dx11dataloader-load.md"><strong>Laden</strong></a></span><span class="sxs-lookup"><span data-stu-id="48eef-123"><a href="id3dx11dataloader-load.md"><strong>Load</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="48eef-124">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48eef-124">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="48eef-125">Lädt Daten von einem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="48eef-125">Loads data from a disk.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="48eef-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48eef-126">Remarks</span></span>

<span data-ttu-id="48eef-127">Dieses Objekt kann geerbt und seine Member neu definiert werden.</span><span class="sxs-lookup"><span data-stu-id="48eef-127">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="48eef-128">Auf diese Weise können Sie die API zum Laden und Dekomprimieren ihrer eigenen benutzerdefinierten Dateiformate anpassen.</span><span class="sxs-lookup"><span data-stu-id="48eef-128">Doing so would enable you to customize the API for loading and decompressing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="48eef-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="48eef-129">Requirements</span></span>



| <span data-ttu-id="48eef-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48eef-130">Requirement</span></span> | <span data-ttu-id="48eef-131">Wert</span><span class="sxs-lookup"><span data-stu-id="48eef-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48eef-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48eef-132">Minimum supported client</span></span><br/> | <span data-ttu-id="48eef-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48eef-133">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="48eef-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48eef-134">Minimum supported server</span></span><br/> | <span data-ttu-id="48eef-135">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48eef-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="48eef-136">Header</span><span class="sxs-lookup"><span data-stu-id="48eef-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="48eef-137"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="48eef-137"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="48eef-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48eef-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="48eef-139"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48eef-139"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="48eef-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="48eef-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48eef-141">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="48eef-141">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

