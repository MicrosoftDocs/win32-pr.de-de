---
description: Konvertiert eine imecolorsty-Struktur in eine COLORREF-Struktur.
ms.assetid: f7a3eab0-16ca-4c4e-9eda-bead8d1a91b8
title: Rgbfromimecolorstyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RGBFromIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 7993253e5e11c45cae3e062467db080201bc1228
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369389"
---
# <a name="rgbfromimecolorstyle-function"></a><span data-ttu-id="6cac8-103">Rgbfromimecolorstyle-Funktion</span><span class="sxs-lookup"><span data-stu-id="6cac8-103">RGBFromIMEColorStyle function</span></span>

<span data-ttu-id="6cac8-104">Konvertiert eine **imecolorsty** -Struktur in eine [**COLORREF**](../gdi/colorref.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6cac8-104">Converts an **IMECOLORSTY** structure to a [**COLORREF**](../gdi/colorref.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cac8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cac8-105">Syntax</span></span>


```C++
COLORREF RGBFromIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="6cac8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cac8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cac8-107">*pcolorstyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6cac8-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cac8-108">Eine **imecolorsty** -Struktur, die von einer [**pcolorstylebackfromimestyle**](pcolorstylebackfromimestyle.md) -oder [**pcolorstyletextfromimestyle**](pcolorstyletextfromimestyle.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6cac8-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cac8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6cac8-109">Return value</span></span>

<span data-ttu-id="6cac8-110">Gibt eine [**COLORREF**](../gdi/colorref.md) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="6cac8-110">Returns a [**COLORREF**](../gdi/colorref.md) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cac8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6cac8-111">Remarks</span></span>

<span data-ttu-id="6cac8-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6cac8-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cac8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6cac8-113">Requirements</span></span>



| <span data-ttu-id="6cac8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6cac8-114">Requirement</span></span> | <span data-ttu-id="6cac8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6cac8-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cac8-116">DLL</span><span class="sxs-lookup"><span data-stu-id="6cac8-116">DLL</span></span><br/> | <dl> <span data-ttu-id="6cac8-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cac8-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cac8-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cac8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cac8-119">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="6cac8-119">**COLORREF**</span></span>](../gdi/colorref.md)
</dt> <dt>

[<span data-ttu-id="6cac8-120">**Pcolorstylebackfromimestyle**</span><span class="sxs-lookup"><span data-stu-id="6cac8-120">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="6cac8-121">**Pcolorstyletextfromimestyle**</span><span class="sxs-lookup"><span data-stu-id="6cac8-121">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
