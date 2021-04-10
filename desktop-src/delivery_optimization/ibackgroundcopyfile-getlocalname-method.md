---
title: Ibackgroundcopyfile getLocalName-Methode (deliveryoptimization. h)
description: Ruft den lokalen Namen der Datei ab.
ms.assetid: 9AA57EB7-5C29-4E5E-972B-DD34B130E6E4
keywords:
- GetLocalName-Methode
- GetLocalName-Methode, ibackgroundcopyfile-Schnittstelle
- Ibackgroundcopyfile-Schnittstelle, getLocalName-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetLocalName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1c3a957e64701242d9c698a014ec2ab4028cd85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040523"
---
# <a name="ibackgroundcopyfilegetlocalname-method"></a><span data-ttu-id="9f487-106">Ibackgroundcopyfile:: getLocalName-Methode</span><span class="sxs-lookup"><span data-stu-id="9f487-106">IBackgroundCopyFile::GetLocalName method</span></span>

<span data-ttu-id="9f487-107">Ruft den lokalen Namen der Datei ab.</span><span class="sxs-lookup"><span data-stu-id="9f487-107">Retrieves the local name of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f487-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f487-108">Syntax</span></span>


```C++
HRESULT GetLocalName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="9f487-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f487-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f487-110">*ppName* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9f487-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f487-111">Eine auf NULL endenden Zeichenfolge, die den Namen der Datei auf dem Client enthält.</span><span class="sxs-lookup"><span data-stu-id="9f487-111">Null-terminated string that contains the name of the file on the client.</span></span> <span data-ttu-id="9f487-112">Der Name ist voll qualifiziert.</span><span class="sxs-lookup"><span data-stu-id="9f487-112">The name is fully qualified.</span></span> <span data-ttu-id="9f487-113">Wenn Sie die Funktion " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen, wird " *ppName* " freigegeben.</span><span class="sxs-lookup"><span data-stu-id="9f487-113">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f487-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f487-114">Return value</span></span>

<span data-ttu-id="9f487-115">Diese Methode gibt **S_OK** bei Erfolg oder einen der standardmäßigen com **HRESULT** -Werte bei einem Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9f487-115">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f487-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f487-116">Requirements</span></span>



| <span data-ttu-id="9f487-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f487-117">Requirement</span></span> | <span data-ttu-id="9f487-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9f487-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f487-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f487-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9f487-120">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f487-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9f487-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f487-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9f487-122">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f487-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9f487-123">Header</span><span class="sxs-lookup"><span data-stu-id="9f487-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f487-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f487-124"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f487-125">IDL</span><span class="sxs-lookup"><span data-stu-id="9f487-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f487-126"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f487-126"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9f487-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9f487-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f487-128"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f487-128"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9f487-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9f487-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f487-130"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f487-130"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9f487-131">IID</span><span class="sxs-lookup"><span data-stu-id="9f487-131">IID</span></span><br/>                      | <span data-ttu-id="9f487-132">IID_IBackgroundCopyFile ist als 01b7bd23-B88-4a77-8490-5891d3e4653a definiert.</span><span class="sxs-lookup"><span data-stu-id="9f487-132">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="9f487-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f487-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f487-134">**Ibackgroundcopyfile**</span><span class="sxs-lookup"><span data-stu-id="9f487-134">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="9f487-135">**Ibackgroundcopyfile:: getremutename**</span><span class="sxs-lookup"><span data-stu-id="9f487-135">**IBackgroundCopyFile::GetRemoteName**</span></span>](ibackgroundcopyfile-getremotename-method.md)
</dt> </dl>

 

