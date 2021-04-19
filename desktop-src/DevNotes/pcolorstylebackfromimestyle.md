---
description: Ruft den Hintergrund Farbstil des angegebenen Stils ab.
ms.assetid: 1b0acac1-c36d-49b6-8154-f69bda008e9a
title: Pcolorstylebackfromimestyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleBackFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 33ff9072fc5e850654f932817cd4ecf0e9372aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351357"
---
# <a name="pcolorstylebackfromimestyle-function"></a><span data-ttu-id="3d701-103">Pcolorstylebackfromimestyle-Funktion</span><span class="sxs-lookup"><span data-stu-id="3d701-103">PColorStyleBackFromIMEStyle function</span></span>

<span data-ttu-id="3d701-104">Ruft den Hintergrund Farbstil des angegebenen Stils ab.</span><span class="sxs-lookup"><span data-stu-id="3d701-104">Retrieves the background color style of the specified style.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d701-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d701-105">Syntax</span></span>


```C++
const IMECOLORSTY* __cdecl PColorStyleBackFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="3d701-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d701-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d701-107">*pimestyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d701-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d701-108">Eine **imestyle** -Struktur, die von der [**pimestylefromattr**](pimestylefromattr.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3d701-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d701-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d701-109">Return value</span></span>

<span data-ttu-id="3d701-110">Ein Zeiger auf eine **imecolorsty** -Struktur, die den Hintergrund Farbstil darstellt.</span><span class="sxs-lookup"><span data-stu-id="3d701-110">Pointer to an **IMECOLORSTY** structure representing the background color style.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d701-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d701-111">Remarks</span></span>

<span data-ttu-id="3d701-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3d701-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="3d701-113">Die **imecolorsty** -Struktur ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="3d701-113">The **IMECOLORSTY** structure is defined as follows:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="3d701-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d701-114">Requirements</span></span>



| <span data-ttu-id="3d701-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d701-115">Requirement</span></span> | <span data-ttu-id="3d701-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3d701-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d701-117">DLL</span><span class="sxs-lookup"><span data-stu-id="3d701-117">DLL</span></span><br/> | <dl> <span data-ttu-id="3d701-118"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d701-118"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d701-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d701-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d701-120">**Pimestylefromattr**</span><span class="sxs-lookup"><span data-stu-id="3d701-120">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
