---
description: Gibt an, ob ein nicht-Farbstil einen Unterstrich hat.
ms.assetid: 452dda6e-b12b-457c-9a01-c5363359c9f5
title: Fulimestyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: a49090d2ca192dfd3ec6d0064b92bd2233af79c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354109"
---
# <a name="fulimestyle-function"></a><span data-ttu-id="604f6-103">Fulimestyle-Funktion</span><span class="sxs-lookup"><span data-stu-id="604f6-103">FUlIMEStyle function</span></span>

<span data-ttu-id="604f6-104">Gibt an, ob ein nicht-Farbstil einen Unterstrich hat.</span><span class="sxs-lookup"><span data-stu-id="604f6-104">Specifies whether a non-color style has an underline style.</span></span>

## <a name="syntax"></a><span data-ttu-id="604f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="604f6-105">Syntax</span></span>


```C++
BOOL __cdecl FUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="604f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="604f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="604f6-107">*pimestyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="604f6-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="604f6-108">Eine **imestyle** -Struktur, die von der [**pimestylefromattr**](pimestylefromattr.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="604f6-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="604f6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="604f6-109">Return value</span></span>

<span data-ttu-id="604f6-110">TRUE, wenn der Stil einen Unterstrich hat.</span><span class="sxs-lookup"><span data-stu-id="604f6-110">TRUE if the style has an underline style.</span></span>

## <a name="remarks"></a><span data-ttu-id="604f6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="604f6-111">Remarks</span></span>

<span data-ttu-id="604f6-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="604f6-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="604f6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="604f6-113">Requirements</span></span>



| <span data-ttu-id="604f6-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="604f6-114">Requirement</span></span> | <span data-ttu-id="604f6-115">Wert</span><span class="sxs-lookup"><span data-stu-id="604f6-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="604f6-116">DLL</span><span class="sxs-lookup"><span data-stu-id="604f6-116">DLL</span></span><br/> | <dl> <span data-ttu-id="604f6-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="604f6-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="604f6-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="604f6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="604f6-119">**Pimestylefromattr**</span><span class="sxs-lookup"><span data-stu-id="604f6-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
