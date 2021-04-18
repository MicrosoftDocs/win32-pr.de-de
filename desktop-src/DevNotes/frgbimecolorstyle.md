---
description: Gibt an, ob die angegebene Farbe eine RGB-Farbe ist.
ms.assetid: 16b48644-c2d5-4383-836a-122f44504638
title: Frgbimecolorstyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRGBIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: df11a2ad972791eaf7049bdef5fa927aaa4119da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368431"
---
# <a name="frgbimecolorstyle-function"></a><span data-ttu-id="49cb2-103">Frgbimecolorstyle-Funktion</span><span class="sxs-lookup"><span data-stu-id="49cb2-103">FRGBIMEColorStyle function</span></span>

<span data-ttu-id="49cb2-104">Gibt an, ob die angegebene Farbe eine RGB-Farbe ist.</span><span class="sxs-lookup"><span data-stu-id="49cb2-104">Specifies whether the specified color is an RGB color.</span></span>

## <a name="syntax"></a><span data-ttu-id="49cb2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="49cb2-105">Syntax</span></span>


```C++
BOOL __cdecl FRGBIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="49cb2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="49cb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49cb2-107">*pcolorstyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49cb2-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49cb2-108">Eine **imecolorsty** -Struktur, die von einer [**pcolorstylebackfromimestyle**](pcolorstylebackfromimestyle.md) -oder [**pcolorstyletextfromimestyle**](pcolorstyletextfromimestyle.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="49cb2-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49cb2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49cb2-109">Return value</span></span>

<span data-ttu-id="49cb2-110">Gibt **true** zurück, wenn die Farbe eine RGB-Farbe ist.</span><span class="sxs-lookup"><span data-stu-id="49cb2-110">Returns **TRUE** when the color is an RGB color.</span></span>

## <a name="remarks"></a><span data-ttu-id="49cb2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49cb2-111">Remarks</span></span>

<span data-ttu-id="49cb2-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="49cb2-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="49cb2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49cb2-113">Requirements</span></span>



| <span data-ttu-id="49cb2-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49cb2-114">Requirement</span></span> | <span data-ttu-id="49cb2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="49cb2-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49cb2-116">DLL</span><span class="sxs-lookup"><span data-stu-id="49cb2-116">DLL</span></span><br/> | <dl> <span data-ttu-id="49cb2-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49cb2-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49cb2-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49cb2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49cb2-119">**Pcolorstylebackfromimestyle**</span><span class="sxs-lookup"><span data-stu-id="49cb2-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="49cb2-120">**Pcolorstyletextfromimestyle**</span><span class="sxs-lookup"><span data-stu-id="49cb2-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
