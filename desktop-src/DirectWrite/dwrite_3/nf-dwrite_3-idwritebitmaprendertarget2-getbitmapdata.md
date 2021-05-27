---
UID: NF:dwrite_3.IDWriteBitmapRenderTarget2.GetBitmapData
title: IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)
description: Ruft die Pixeldaten von einem Bitmaprenderziel ab.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2::GetBitmapData
- dwrite_3/IDWriteBitmapRenderTarget2::GetBitmapData
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2.GetBitmapData
ms.openlocfilehash: 15a51fdea0d7e579e427ab52af3016e58a39831a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550285"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a><span data-ttu-id="9c0eb-103">IDWriteBitmapRenderTarget2::GetBitmapData-Methode (dwrite_3.h)</span><span class="sxs-lookup"><span data-stu-id="9c0eb-103">IDWriteBitmapRenderTarget2::GetBitmapData method (dwrite_3.h)</span></span>

<span data-ttu-id="9c0eb-104">Ruft die Pixeldaten von einem Bitmaprenderziel ab.</span><span class="sxs-lookup"><span data-stu-id="9c0eb-104">Retrieves the pixel data from a bitmap render target.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9c0eb-105">Diese API ist als Teil der DWriteCore-Implementierung von [DirectWrite](../direct-write-portal.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9c0eb-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="9c0eb-106">DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="9c0eb-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="9c0eb-107">Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über DWriteCore.](../dwritecore-overview.md)</span><span class="sxs-lookup"><span data-stu-id="9c0eb-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9c0eb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c0eb-108">Syntax</span></span>

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a><span data-ttu-id="9c0eb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c0eb-109">Parameters</span></span>

`bitmapData`

<span data-ttu-id="9c0eb-110">Typ: \_ Out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c0eb-110">Type: \_Out\_**[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span></span>

<span data-ttu-id="9c0eb-111">Ein Zeiger auf die Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="9c0eb-111">A pointer to the pixel data.</span></span>

## <a name="return-value"></a><span data-ttu-id="9c0eb-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c0eb-112">Return value</span></span>

<span data-ttu-id="9c0eb-113">Typ: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="9c0eb-113">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="9c0eb-114">Wenn diese Methode erfolgreich ist, wird <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c0eb-114">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="9c0eb-115">Andernfalls wird ein <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT-Fehlercode</b> zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c0eb-115">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="9c0eb-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c0eb-116">Examples</span></span>

<span data-ttu-id="9c0eb-117">Weitere Informationen finden Sie im [Übersichtsthema DWriteCore](../dwritecore-overview.md) und in der [Beispiel-App DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="9c0eb-117">See the [DWriteCore overview](../dwritecore-overview.md) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c0eb-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c0eb-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9c0eb-119">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="9c0eb-119">**Minimum supported client**</span></span> | <span data-ttu-id="9c0eb-120">Windows 10, Project Reunion [Win32-Apps]</span><span class="sxs-lookup"><span data-stu-id="9c0eb-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="9c0eb-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="9c0eb-121">**Header**</span></span> | <span data-ttu-id="9c0eb-122">dwrite_3.h (include dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="9c0eb-122">dwrite_3.h (include dwrite_core.h)</span></span> |
| <span data-ttu-id="9c0eb-123">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="9c0eb-123">**Library**</span></span> | <span data-ttu-id="9c0eb-124">Dwrite.lib</span><span class="sxs-lookup"><span data-stu-id="9c0eb-124">Dwrite.lib</span></span> |
| <span data-ttu-id="9c0eb-125">**Dll**</span><span class="sxs-lookup"><span data-stu-id="9c0eb-125">**DLL**</span></span> | <span data-ttu-id="9c0eb-126">Dwrite.dll</span><span class="sxs-lookup"><span data-stu-id="9c0eb-126">Dwrite.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="9c0eb-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c0eb-127">See also</span></span>

[<span data-ttu-id="9c0eb-128">IDWriteBitmapRenderTarget2</span><span class="sxs-lookup"><span data-stu-id="9c0eb-128">IDWriteBitmapRenderTarget2</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)