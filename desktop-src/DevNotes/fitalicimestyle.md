---
description: Gibt an, ob ein nicht-Farbstil den kursiv Formatierungs Stil aufweist.
ms.assetid: 4295c0b1-6e37-4fa9-9015-68bcc4784cda
title: Fitalicimestyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FItalicIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 828e701773d666830473e92afc73f80ccdae3bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359652"
---
# <a name="fitalicimestyle-function"></a><span data-ttu-id="579f4-103">Fitalicimestyle-Funktion</span><span class="sxs-lookup"><span data-stu-id="579f4-103">FItalicIMEStyle function</span></span>

<span data-ttu-id="579f4-104">Gibt an, ob ein nicht-Farbstil den kursiv Formatierungs Stil aufweist.</span><span class="sxs-lookup"><span data-stu-id="579f4-104">Specifies whether a non-color style has the italic style.</span></span>

## <a name="syntax"></a><span data-ttu-id="579f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="579f4-105">Syntax</span></span>


```C++
BOOL __cdecl FItalicIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="579f4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="579f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="579f4-107">*pimestyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="579f4-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="579f4-108">Eine **imestyle** -Struktur, die von der [**pimestylefromattr**](pimestylefromattr.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="579f4-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="579f4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="579f4-109">Return value</span></span>

<span data-ttu-id="579f4-110">**True** , wenn der Stil den kursiv Formatierungs Stil aufweist.</span><span class="sxs-lookup"><span data-stu-id="579f4-110">**TRUE** if the style has the italic style.</span></span>

## <a name="remarks"></a><span data-ttu-id="579f4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="579f4-111">Remarks</span></span>

<span data-ttu-id="579f4-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="579f4-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="579f4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="579f4-113">Requirements</span></span>



| <span data-ttu-id="579f4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="579f4-114">Requirement</span></span> | <span data-ttu-id="579f4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="579f4-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="579f4-116">DLL</span><span class="sxs-lookup"><span data-stu-id="579f4-116">DLL</span></span><br/> | <dl> <span data-ttu-id="579f4-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="579f4-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="579f4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="579f4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="579f4-119">**Pimestylefromattr**</span><span class="sxs-lookup"><span data-stu-id="579f4-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
