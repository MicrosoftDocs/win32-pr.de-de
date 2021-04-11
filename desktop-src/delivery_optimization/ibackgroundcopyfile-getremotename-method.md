---
title: Ibackgroundcopyfile getremutename-Methode (deliveryoptimization. h)
description: Ruft den Remote Namen der Datei ab.
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- Getremutename-Methode
- Getremutename-Methode, ibackgroundcopyfile-Schnittstelle
- Ibackgroundcopyfile-Schnittstelle, getremutename-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9984ed9971fdfb91279dabc5810490b62804b7e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040521"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a><span data-ttu-id="b9e11-106">Ibackgroundcopyfile:: getremutename-Methode</span><span class="sxs-lookup"><span data-stu-id="b9e11-106">IBackgroundCopyFile::GetRemoteName method</span></span>

<span data-ttu-id="b9e11-107">Ruft den Remote Namen der Datei ab.</span><span class="sxs-lookup"><span data-stu-id="b9e11-107">Retrieves the remote name of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e11-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9e11-108">Syntax</span></span>


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="b9e11-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9e11-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9e11-110">*ppName* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9e11-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e11-111">Eine auf NULL endenden Zeichenfolge, die den Remote Namen der zu übertragenden Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="b9e11-111">Null-terminated string that contains the remote name of the file to transfer.</span></span> <span data-ttu-id="b9e11-112">Der Name ist voll qualifiziert.</span><span class="sxs-lookup"><span data-stu-id="b9e11-112">The name is fully qualified.</span></span> <span data-ttu-id="b9e11-113">Wenn Sie die Funktion " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen, wird " *ppName* " freigegeben.</span><span class="sxs-lookup"><span data-stu-id="b9e11-113">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9e11-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9e11-114">Return value</span></span>

<span data-ttu-id="b9e11-115">Diese Methode gibt **S_OK** bei Erfolg oder einen der standardmäßigen com **HRESULT** -Werte bei einem Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b9e11-115">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9e11-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9e11-116">Remarks</span></span>

<span data-ttu-id="b9e11-117">Um den Remote Dateinamen zu ändern, nennen Sie die [**IBackgroundCopyFile2::**](ibackgroundcopyfile2-setremotename-method.md) Setup-Methode.</span><span class="sxs-lookup"><span data-stu-id="b9e11-117">To change the remote file name, call the [**IBackgroundCopyFile2::SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9e11-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9e11-118">Requirements</span></span>



| <span data-ttu-id="b9e11-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9e11-119">Requirement</span></span> | <span data-ttu-id="b9e11-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b9e11-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e11-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9e11-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b9e11-122">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9e11-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b9e11-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9e11-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b9e11-124">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9e11-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b9e11-125">Header</span><span class="sxs-lookup"><span data-stu-id="b9e11-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9e11-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9e11-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9e11-127">IDL</span><span class="sxs-lookup"><span data-stu-id="b9e11-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9e11-128"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9e11-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b9e11-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b9e11-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9e11-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9e11-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b9e11-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b9e11-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9e11-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9e11-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b9e11-133">IID</span><span class="sxs-lookup"><span data-stu-id="b9e11-133">IID</span></span><br/>                      | <span data-ttu-id="b9e11-134">IID_IBackgroundCopyFile ist als 01b7bd23-B88-4a77-8490-5891d3e4653a definiert.</span><span class="sxs-lookup"><span data-stu-id="b9e11-134">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="b9e11-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9e11-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e11-136">**Ibackgroundcopyfile**</span><span class="sxs-lookup"><span data-stu-id="b9e11-136">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="b9e11-137">**Ibackgroundcopyfile:: getLocalName**</span><span class="sxs-lookup"><span data-stu-id="b9e11-137">**IBackgroundCopyFile::GetLocalName**</span></span>](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

