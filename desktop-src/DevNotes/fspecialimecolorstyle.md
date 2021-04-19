---
description: Gibt an, ob die angegebene Farbe eine besondere Farbe ist.
ms.assetid: fda856c4-37b9-444f-9c54-d9eb848a4b05
title: Funktion "Funktion"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: af6edf14f4c2167a4609cd8cbb671e85e297368d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366961"
---
# <a name="fspecialimecolorstyle-function"></a><span data-ttu-id="c75f7-103">Funktion "Funktion"</span><span class="sxs-lookup"><span data-stu-id="c75f7-103">FSpecialIMEColorStyle function</span></span>

<span data-ttu-id="c75f7-104">Gibt an, ob die angegebene Farbe eine besondere Farbe ist.</span><span class="sxs-lookup"><span data-stu-id="c75f7-104">Specifies whether the specified color is a special color.</span></span>

## <a name="syntax"></a><span data-ttu-id="c75f7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c75f7-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="c75f7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c75f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c75f7-107">*pcolorstyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c75f7-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c75f7-108">Eine **imecolorsty** -Struktur, die von einer [**pcolorstylebackfromimestyle**](pcolorstylebackfromimestyle.md) -oder [**pcolorstyletextfromimestyle**](pcolorstyletextfromimestyle.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c75f7-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c75f7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c75f7-109">Return value</span></span>

<span data-ttu-id="c75f7-110">Gibt **true** zurück, wenn die Farbe eine besondere Farbe ist.</span><span class="sxs-lookup"><span data-stu-id="c75f7-110">Returns **TRUE** when the color is a special color.</span></span>

## <a name="remarks"></a><span data-ttu-id="c75f7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c75f7-111">Remarks</span></span>

<span data-ttu-id="c75f7-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c75f7-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c75f7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c75f7-113">Requirements</span></span>



| <span data-ttu-id="c75f7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c75f7-114">Requirement</span></span> | <span data-ttu-id="c75f7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c75f7-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c75f7-116">DLL</span><span class="sxs-lookup"><span data-stu-id="c75f7-116">DLL</span></span><br/> | <dl> <span data-ttu-id="c75f7-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c75f7-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c75f7-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c75f7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c75f7-119">**Pcolorstylebackfromimestyle**</span><span class="sxs-lookup"><span data-stu-id="c75f7-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="c75f7-120">**Pcolorstyletextfromimestyle**</span><span class="sxs-lookup"><span data-stu-id="c75f7-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
