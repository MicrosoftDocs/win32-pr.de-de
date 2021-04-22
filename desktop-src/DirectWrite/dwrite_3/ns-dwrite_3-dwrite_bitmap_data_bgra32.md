---
UID: NS:dwrite_3.DWRITE_BITMAP_DATA_BGRA32
title: DWRITE_BITMAP_DATA_BGRA32 (dwrite_3.h)
description: Stellt Bitmapdaten im BGRA32-Format dar.
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_BITMAP_DATA_BGRA32
- dwrite_3/DWRITE_BITMAP_DATA_BGRA32
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_3.h
api_name:
- DWRITE_BITMAP_DATA_BGRA32
ms.openlocfilehash: 3d5b2168e5154f2e55b6f5acb83897f68d4a029c
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881829"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a><span data-ttu-id="b6cae-103">DWRITE_BITMAP_DATA_BGRA32-Struktur (dwrite_3.h)</span><span class="sxs-lookup"><span data-stu-id="b6cae-103">DWRITE_BITMAP_DATA_BGRA32 structure (dwrite_3.h)</span></span>

<span data-ttu-id="b6cae-104">Stellt Bitmapdaten im BGRA32-Format dar.</span><span class="sxs-lookup"><span data-stu-id="b6cae-104">Represents bitmap data in BGRA32 format.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6cae-105">Diese API ist als Teil der DWriteCore-Implementierung von [DirectWrite](../direct-write-portal.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b6cae-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="b6cae-106">DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="b6cae-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="b6cae-107">Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über DWriteCore.](/windows/win32/DirectWrite/dwrite/dwritecore-overview)</span><span class="sxs-lookup"><span data-stu-id="b6cae-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="b6cae-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6cae-108">Syntax</span></span>

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a><span data-ttu-id="b6cae-109">Member</span><span class="sxs-lookup"><span data-stu-id="b6cae-109">Members</span></span>

`width`

<span data-ttu-id="b6cae-110">Typ: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6cae-110">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6cae-111">Die Breite der Bitmap in Pixel.</span><span class="sxs-lookup"><span data-stu-id="b6cae-111">The width, in pixels, of the bitmap.</span></span>


`height`

<span data-ttu-id="b6cae-112">Typ: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6cae-112">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6cae-113">Die Höhe der Bitmap in Pixel.</span><span class="sxs-lookup"><span data-stu-id="b6cae-113">The height, in pixels, of the bitmap.</span></span>


`pixels`

<span data-ttu-id="b6cae-114">Typ: \_ \_ Feldgröße \_ (Breite \* Höhe)**[UINT32](../../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b6cae-114">Type: \_Field\_size\_(width \* height)**[UINT32](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b6cae-115">Ein Zeiger auf die Position der Bitwerte für die Bitmap.</span><span class="sxs-lookup"><span data-stu-id="b6cae-115">A pointer to the location of the bit values for the bitmap.</span></span>


## <a name="examples"></a><span data-ttu-id="b6cae-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6cae-116">Examples</span></span>

<span data-ttu-id="b6cae-117">Weitere Informationen finden Sie im Übersichtsthema [DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) und in der [Beispiel-App DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="b6cae-117">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6cae-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6cae-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b6cae-119">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="b6cae-119">**Minimum supported client**</span></span> | <span data-ttu-id="b6cae-120">Windows 10, Project Reunion [Win32-Apps]</span><span class="sxs-lookup"><span data-stu-id="b6cae-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="b6cae-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="b6cae-121">**Header**</span></span> | <span data-ttu-id="b6cae-122">dwrite_3.h (include dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="b6cae-122">dwrite_3.h (include dwrite_core.h)</span></span> |