---
description: Die dibdata-Struktur enthält Informationen über eine GDI-geräteunabhängige Bitmap (DIB).
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: Dibdata-Struktur (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIBDATA
api_type:
- HeaderDef
api_location:
- Winutil.h
ms.openlocfilehash: 87590013ef905ffbdd13dd3b767435a907b08783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352040"
---
# <a name="dibdata-structure"></a><span data-ttu-id="75062-103">Dibdata-Struktur</span><span class="sxs-lookup"><span data-stu-id="75062-103">DIBDATA structure</span></span>

<span data-ttu-id="75062-104">Die `DIBDATA` Struktur enthält Informationen über eine GDI-geräteunabhängige Bitmap (DIB).</span><span class="sxs-lookup"><span data-stu-id="75062-104">The `DIBDATA` structure contains information about a GDI device-independent bitmap (DIB).</span></span>

## <a name="syntax"></a><span data-ttu-id="75062-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75062-105">Syntax</span></span>


```C++
typedef struct tagDIBDATA {
  LONG       PaletteVersion;
  DIBSECTION DibSection;
  HBITMAP    hBitmap;
  HANDLE     hMapping;
  BYTE       *pBase;
} DIBDATA;
```



## <a name="members"></a><span data-ttu-id="75062-106">Member</span><span class="sxs-lookup"><span data-stu-id="75062-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="75062-107">**Paletteversion**</span><span class="sxs-lookup"><span data-stu-id="75062-107">**PaletteVersion**</span></span>
</dt> <dd>

<span data-ttu-id="75062-108">Dieser Member sollte immer dann erhöht werden, wenn die Palette geändert wird.</span><span class="sxs-lookup"><span data-stu-id="75062-108">This member should be incremented whenever the palette changes.</span></span>

</dd> <dt>

<span data-ttu-id="75062-109">**DIBsection**</span><span class="sxs-lookup"><span data-stu-id="75062-109">**DibSection**</span></span>
</dt> <dd>

<span data-ttu-id="75062-110">Die **DIBsection** -Struktur, die Informationen über das DIB enthält.</span><span class="sxs-lookup"><span data-stu-id="75062-110">**DIBSECTION** structure that contains information about the DIB.</span></span> <span data-ttu-id="75062-111">Weitere Informationen finden Sie in der GDI-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="75062-111">See the GDI documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="75062-112">**HBITMAP**</span><span class="sxs-lookup"><span data-stu-id="75062-112">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="75062-113">Handle für die Bitmap.</span><span class="sxs-lookup"><span data-stu-id="75062-113">Handle to the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="75062-114">**hmapping**</span><span class="sxs-lookup"><span data-stu-id="75062-114">**hMapping**</span></span>
</dt> <dd>

<span data-ttu-id="75062-115">Handle für ein Datei Zuordnungsobjekt, das zum Freigeben von Arbeitsspeicher zwischen GDI und einem [**cimagesample**](cimagesample.md) -Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="75062-115">Handle to a file-mapping object that is used to share memory between GDI and a [**CImageSample**](cimagesample.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="75062-116">**pBase**</span><span class="sxs-lookup"><span data-stu-id="75062-116">**pBase**</span></span>
</dt> <dd>

<span data-ttu-id="75062-117">Adresse der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="75062-117">Address of the bitmap.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75062-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75062-118">Requirements</span></span>



| <span data-ttu-id="75062-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75062-119">Requirement</span></span> | <span data-ttu-id="75062-120">Wert</span><span class="sxs-lookup"><span data-stu-id="75062-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75062-121">Header</span><span class="sxs-lookup"><span data-stu-id="75062-121">Header</span></span><br/> | <dl> <span data-ttu-id="75062-122"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75062-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl> |



 

 




