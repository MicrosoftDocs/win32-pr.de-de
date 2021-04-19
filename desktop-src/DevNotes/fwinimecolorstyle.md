---
description: Gibt an, ob die angegebene Farbe eine Windows-Farbe ist.
ms.assetid: 0d2b2039-938c-4f9d-8ddc-9eb711f55009
title: Funktion "Funktion"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FWinIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 28731672f5f1aff385f9051ba8b641b7cdcdf83c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357602"
---
# <a name="fwinimecolorstyle-function"></a><span data-ttu-id="d11da-103">Funktion "Funktion"</span><span class="sxs-lookup"><span data-stu-id="d11da-103">FWinIMEColorStyle function</span></span>

<span data-ttu-id="d11da-104">Gibt an, ob die angegebene Farbe eine Windows-Farbe ist.</span><span class="sxs-lookup"><span data-stu-id="d11da-104">Specifies whether the specified color is a Windows color.</span></span>

## <a name="syntax"></a><span data-ttu-id="d11da-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d11da-105">Syntax</span></span>


```C++
BOOL __cdecl FWinIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="d11da-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d11da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d11da-107">*pcolorstyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d11da-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d11da-108">Eine **imecolorsty** -Struktur, die von einer [**pcolorstylebackfromimestyle**](pcolorstylebackfromimestyle.md) -oder [**pcolorstyletextfromimestyle**](pcolorstyletextfromimestyle.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d11da-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d11da-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d11da-109">Return value</span></span>

<span data-ttu-id="d11da-110">Gibt **true** zurück, wenn die Farbe eine Windows-Farbe ist.</span><span class="sxs-lookup"><span data-stu-id="d11da-110">Returns **TRUE** when the color is a Windows color.</span></span>

## <a name="remarks"></a><span data-ttu-id="d11da-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d11da-111">Remarks</span></span>

<span data-ttu-id="d11da-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d11da-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d11da-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d11da-113">Requirements</span></span>



| <span data-ttu-id="d11da-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d11da-114">Requirement</span></span> | <span data-ttu-id="d11da-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d11da-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d11da-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d11da-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d11da-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d11da-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d11da-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d11da-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d11da-119">**Pcolorstylebackfromimestyle**</span><span class="sxs-lookup"><span data-stu-id="d11da-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="d11da-120">**Pcolorstyletextfromimestyle**</span><span class="sxs-lookup"><span data-stu-id="d11da-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
