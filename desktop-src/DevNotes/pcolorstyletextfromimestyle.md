---
description: Ruft den textfarbstil des angegebenen Stils ab.
ms.assetid: 242c37af-5b39-4b18-9c8f-4e692f41c497
title: Pcolorstyletextfromimestyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleTextFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 791fdaca4a93b0a44099306b8ae14ae4d5cb11cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361596"
---
# <a name="pcolorstyletextfromimestyle-function"></a><span data-ttu-id="c381c-103">Pcolorstyletextfromimestyle-Funktion</span><span class="sxs-lookup"><span data-stu-id="c381c-103">PColorStyleTextFromIMEStyle function</span></span>

<span data-ttu-id="c381c-104">Ruft den textfarbstil des angegebenen Stils ab.</span><span class="sxs-lookup"><span data-stu-id="c381c-104">Retrieves the text color style of the specified style.</span></span>

## <a name="syntax"></a><span data-ttu-id="c381c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c381c-105">Syntax</span></span>


```C++
const IMECOLORSTY* __cdecl PColorStyleTextFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="c381c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c381c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c381c-107">*pimestyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c381c-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c381c-108">Eine **imestyle** -Struktur, die von der [**pimestylefromattr**](pimestylefromattr.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c381c-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c381c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c381c-109">Return value</span></span>

<span data-ttu-id="c381c-110">Zeiger auf eine **imecolorsty** -Struktur, die den textfarbstil darstellt.</span><span class="sxs-lookup"><span data-stu-id="c381c-110">Pointer to an **IMECOLORSTY** structure representing the text color style.</span></span>

## <a name="remarks"></a><span data-ttu-id="c381c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c381c-111">Remarks</span></span>

<span data-ttu-id="c381c-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c381c-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="c381c-113">Die **imecolorsty** -Struktur ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="c381c-113">The **IMECOLORSTY** structure is defined as follows:</span></span>

``` syntax
typedef struct {
    UINT colorId;
    union {
        COLORREF    rgb;
        UINT        colorWin;
        UINT        colorSpec;
        UINT        colorFund;
    };
} IMECOLORSTY;
```

## <a name="requirements"></a><span data-ttu-id="c381c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c381c-114">Requirements</span></span>



| <span data-ttu-id="c381c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c381c-115">Requirement</span></span> | <span data-ttu-id="c381c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c381c-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c381c-117">DLL</span><span class="sxs-lookup"><span data-stu-id="c381c-117">DLL</span></span><br/> | <dl> <span data-ttu-id="c381c-118"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c381c-118"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c381c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c381c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c381c-120">**Pimestylefromattr**</span><span class="sxs-lookup"><span data-stu-id="c381c-120">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
