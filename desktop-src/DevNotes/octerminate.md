---
description: Schließt den OC-Manager.
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: Ocend-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcTerminate
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 2e747c19db5e5a79e2827dc3bcfb88b97fae2ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371029"
---
# <a name="octerminate-function"></a><span data-ttu-id="a5aa3-103">Ocend-Funktion</span><span class="sxs-lookup"><span data-stu-id="a5aa3-103">OcTerminate function</span></span>

<span data-ttu-id="a5aa3-104">Schließt den OC-Manager.</span><span class="sxs-lookup"><span data-stu-id="a5aa3-104">Closes the OC manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5aa3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5aa3-105">Syntax</span></span>


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a><span data-ttu-id="a5aa3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5aa3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5aa3-107">*Ocmanagercontext* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a5aa3-107">*OcManagerContext* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5aa3-108">Enthält bei Eingabe den von [**ocinitialize**](ocinitialize.md)zurückgegebenen OC Manager-Kontext Zeiger.</span><span class="sxs-lookup"><span data-stu-id="a5aa3-108">On input, contains the OC manager context pointer returned by [**OcInitialize**](ocinitialize.md).</span></span> <span data-ttu-id="a5aa3-109">Bei der Ausgabe empfängt **null**.</span><span class="sxs-lookup"><span data-stu-id="a5aa3-109">On output, receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5aa3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5aa3-110">Return value</span></span>

<span data-ttu-id="a5aa3-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a5aa3-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5aa3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5aa3-112">Remarks</span></span>

<span data-ttu-id="a5aa3-113">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a5aa3-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5aa3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5aa3-114">Requirements</span></span>



| <span data-ttu-id="a5aa3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5aa3-115">Requirement</span></span> | <span data-ttu-id="a5aa3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a5aa3-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5aa3-117">DLL</span><span class="sxs-lookup"><span data-stu-id="a5aa3-117">DLL</span></span><br/> | <dl> <span data-ttu-id="a5aa3-118"><dt>OcManage.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5aa3-118"><dt>OcManage.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5aa3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5aa3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5aa3-120">**Ocinitialize**</span><span class="sxs-lookup"><span data-stu-id="a5aa3-120">**OcInitialize**</span></span>](ocinitialize.md)
</dt> </dl>

 

 
