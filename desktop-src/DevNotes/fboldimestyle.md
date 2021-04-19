---
description: Gibt an, ob ein nicht Farbstil den fett formatierten Stil hat.
ms.assetid: fd34af7f-8847-43aa-9e69-264a08eba98b
title: Funktion "Funktion"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FBoldIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: f54e62feae710dd51cae688d380ccf7da1eda4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367757"
---
# <a name="fboldimestyle-function"></a><span data-ttu-id="d6664-103">Funktion "Funktion"</span><span class="sxs-lookup"><span data-stu-id="d6664-103">FBoldIMEStyle function</span></span>

<span data-ttu-id="d6664-104">Gibt an, ob ein nicht Farbstil den fett formatierten Stil hat.</span><span class="sxs-lookup"><span data-stu-id="d6664-104">Specifies whether a non-color style has the bold style.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6664-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6664-105">Syntax</span></span>


```C++
BOOL FBoldIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="d6664-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6664-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6664-107">*pimestyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6664-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6664-108">Eine **imestyle** -Struktur, die von der [**pimestylefromattr**](pimestylefromattr.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d6664-108">An **IMESTYLE** structure returned from the [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6664-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6664-109">Return value</span></span>

<span data-ttu-id="d6664-110">**True** , wenn der Stil das Fett formatierte Format aufweist.</span><span class="sxs-lookup"><span data-stu-id="d6664-110">**TRUE** if the style has the bold style.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6664-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6664-111">Remarks</span></span>

<span data-ttu-id="d6664-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d6664-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6664-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6664-113">Requirements</span></span>



| <span data-ttu-id="d6664-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6664-114">Requirement</span></span> | <span data-ttu-id="d6664-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d6664-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6664-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d6664-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d6664-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6664-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6664-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6664-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6664-119">**Pimestylefromattr**</span><span class="sxs-lookup"><span data-stu-id="d6664-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
