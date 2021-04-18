---
description: Gibt an, ob die angegebene Farbe eine besondere Textfarbe ist.
ms.assetid: 527806f5-5046-48b0-a8db-86a5b8c0db08
title: Fspecialtextimecolorstyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialTextIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: cfaf83aeb2fcb03ab61c1280ec821174117026fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351260"
---
# <a name="fspecialtextimecolorstyle-function"></a><span data-ttu-id="47b3d-103">Fspecialtextimecolorstyle-Funktion</span><span class="sxs-lookup"><span data-stu-id="47b3d-103">FSpecialTextIMEColorStyle function</span></span>

<span data-ttu-id="47b3d-104">Gibt an, ob die angegebene Farbe eine besondere Textfarbe ist.</span><span class="sxs-lookup"><span data-stu-id="47b3d-104">Specifies whether the specified color is a special text color.</span></span>

## <a name="syntax"></a><span data-ttu-id="47b3d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47b3d-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialTextIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="47b3d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="47b3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47b3d-107">*pcolorstyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47b3d-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47b3d-108">Eine **imecolorsty** -Struktur, die von einer [**pcolorstylebackfromimestyle**](pcolorstylebackfromimestyle.md) -oder [**pcolorstyletextfromimestyle**](pcolorstyletextfromimestyle.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="47b3d-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47b3d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47b3d-109">Return value</span></span>

<span data-ttu-id="47b3d-110">Gibt **true** zurück, wenn die Farbe eine besondere Textfarbe ist.</span><span class="sxs-lookup"><span data-stu-id="47b3d-110">Returns **TRUE** when the color is a special text color.</span></span>

## <a name="remarks"></a><span data-ttu-id="47b3d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47b3d-111">Remarks</span></span>

<span data-ttu-id="47b3d-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="47b3d-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="47b3d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47b3d-113">Requirements</span></span>



| <span data-ttu-id="47b3d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47b3d-114">Requirement</span></span> | <span data-ttu-id="47b3d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="47b3d-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47b3d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="47b3d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="47b3d-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47b3d-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47b3d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47b3d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47b3d-119">**Pcolorstylebackfromimestyle**</span><span class="sxs-lookup"><span data-stu-id="47b3d-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="47b3d-120">**Pcolorstyletextfromimestyle**</span><span class="sxs-lookup"><span data-stu-id="47b3d-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
