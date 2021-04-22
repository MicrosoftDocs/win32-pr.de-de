---
UID: NF:dwrite_3.IDWriteBitmapRenderTarget2.GetBitmapData
title: IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)
description: Ruft die Pixeldaten aus einem Bitmaprenderingziel ab.
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
ms.openlocfilehash: 3dbc87697750ee07939602dc694468aa68f5c66d
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881849"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a><span data-ttu-id="b3f58-103">IDWriteBitmapRenderTarget2::GetBitmapData-Methode (dwrite_3.h)</span><span class="sxs-lookup"><span data-stu-id="b3f58-103">IDWriteBitmapRenderTarget2::GetBitmapData method (dwrite_3.h)</span></span>

<span data-ttu-id="b3f58-104">Ruft die Pixeldaten aus einem Bitmaprenderingziel ab.</span><span class="sxs-lookup"><span data-stu-id="b3f58-104">Retrieves the pixel data from a bitmap render target.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3f58-105">Diese API ist als Teil der DWriteCore-Implementierung von [DirectWrite verfügbar.](../direct-write-portal.md)</span><span class="sxs-lookup"><span data-stu-id="b3f58-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="b3f58-106">DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="b3f58-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="b3f58-107">Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über DWriteCore.](/windows/win32/DirectWrite/dwrite/dwritecore-overview)</span><span class="sxs-lookup"><span data-stu-id="b3f58-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="b3f58-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3f58-108">Syntax</span></span>

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a><span data-ttu-id="b3f58-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3f58-109">Parameters</span></span>

`bitmapData`

<span data-ttu-id="b3f58-110">Typ: \_ Out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3f58-110">Type: \_Out\_**[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span></span>

<span data-ttu-id="b3f58-111">Ein Zeiger auf die Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="b3f58-111">A pointer to the pixel data.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3f58-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3f58-112">Return value</span></span>

<span data-ttu-id="b3f58-113">Typ: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="b3f58-113">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="b3f58-114">Wenn diese Methode erfolgreich ist, gibt <b xmlns:loc="http://microsoft.com/wdcml/l10n">sie</b>S_OK.</span><span class="sxs-lookup"><span data-stu-id="b3f58-114">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="b3f58-115">Andernfalls wird ein <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT-Fehlercode</b> zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b3f58-115">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="b3f58-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3f58-116">Examples</span></span>

<span data-ttu-id="b3f58-117">Weitere Informationen finden [Sie im DWriteCore-Übersichtsthema](/windows/win32/DirectWrite/dwrite/dwritecore-overview) und in der [DWriteCoreGallery-Beispiel-App.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="b3f58-117">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3f58-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3f58-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b3f58-119">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="b3f58-119">**Minimum supported client**</span></span> | <span data-ttu-id="b3f58-120">Windows 10, Project Reunion [Win32-Apps]</span><span class="sxs-lookup"><span data-stu-id="b3f58-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="b3f58-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="b3f58-121">**Header**</span></span> | <span data-ttu-id="b3f58-122">dwrite_3.h (include dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="b3f58-122">dwrite_3.h (include dwrite_core.h)</span></span> |
| <span data-ttu-id="b3f58-123">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="b3f58-123">**Library**</span></span> | <span data-ttu-id="b3f58-124">Dwrite.lib</span><span class="sxs-lookup"><span data-stu-id="b3f58-124">Dwrite.lib</span></span> |
| <span data-ttu-id="b3f58-125">**Dll**</span><span class="sxs-lookup"><span data-stu-id="b3f58-125">**DLL**</span></span> | <span data-ttu-id="b3f58-126">Dwrite.dll</span><span class="sxs-lookup"><span data-stu-id="b3f58-126">Dwrite.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="b3f58-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b3f58-127">See also</span></span>

[<span data-ttu-id="b3f58-128">IDWriteBitmapRenderTarget2</span><span class="sxs-lookup"><span data-stu-id="b3f58-128">IDWriteBitmapRenderTarget2</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)
