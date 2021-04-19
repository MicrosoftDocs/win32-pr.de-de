---
description: Gibt an, ob die angegebene Farbe eine besondere Fenster Farbe ist.
ms.assetid: 41f7d4fb-9718-42a8-89df-c29bd8c0665b
title: Fspecialwindowimecolorstyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialWindowIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 6fb667186789361a106a23f8daa82088b9bcb2ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370036"
---
# <a name="fspecialwindowimecolorstyle-function"></a><span data-ttu-id="1c5d0-103">Fspecialwindowimecolorstyle-Funktion</span><span class="sxs-lookup"><span data-stu-id="1c5d0-103">FSpecialWindowIMEColorStyle function</span></span>

<span data-ttu-id="1c5d0-104">Gibt an, ob die angegebene Farbe eine besondere Fenster Farbe ist.</span><span class="sxs-lookup"><span data-stu-id="1c5d0-104">Specifies whether the specified color is a special window color.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c5d0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c5d0-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialWindowIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="1c5d0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c5d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c5d0-107">*pcolorstyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c5d0-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c5d0-108">Eine **imecolorsty** -Struktur, die von einer [**pcolorstylebackfromimestyle**](pcolorstylebackfromimestyle.md) -oder [**pcolorstyletextfromimestyle**](pcolorstyletextfromimestyle.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1c5d0-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c5d0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c5d0-109">Return value</span></span>

<span data-ttu-id="1c5d0-110">Gibt **true** zurück, wenn die Farbe eine besondere Fenster Farbe (eine der besonderen Farben) ist.</span><span class="sxs-lookup"><span data-stu-id="1c5d0-110">Returns **TRUE** when the color is a special window color (one of special color).</span></span>

## <a name="remarks"></a><span data-ttu-id="1c5d0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c5d0-111">Remarks</span></span>

<span data-ttu-id="1c5d0-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1c5d0-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c5d0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c5d0-113">Requirements</span></span>



| <span data-ttu-id="1c5d0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c5d0-114">Requirement</span></span> | <span data-ttu-id="1c5d0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1c5d0-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c5d0-116">DLL</span><span class="sxs-lookup"><span data-stu-id="1c5d0-116">DLL</span></span><br/> | <dl> <span data-ttu-id="1c5d0-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c5d0-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c5d0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c5d0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c5d0-119">**Pcolorstylebackfromimestyle**</span><span class="sxs-lookup"><span data-stu-id="1c5d0-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="1c5d0-120">**Pcolorstyletextfromimestyle**</span><span class="sxs-lookup"><span data-stu-id="1c5d0-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
