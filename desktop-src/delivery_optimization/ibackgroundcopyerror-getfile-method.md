---
title: Ibackgroundcopyerror GetFile-Methode (deliveryoptimization. h)
description: Ruft einen Schnittstellen Zeiger auf das File-Objekt ab, das dem Fehler zugeordnet ist.
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- GetFile-Methode
- GetFile-Methode, ibackgroundcopyerror-Schnittstelle
- Ibackgroundcopyerror-Schnittstelle, GetFile-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b84396797378c77a6f774b4c63a3966b0d601b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337735"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a><span data-ttu-id="17d56-106">Ibackgroundcopyerror:: GetFile-Methode</span><span class="sxs-lookup"><span data-stu-id="17d56-106">IBackgroundCopyError::GetFile method</span></span>

<span data-ttu-id="17d56-107">Ruft einen Schnittstellen Zeiger auf das File-Objekt ab, das dem Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="17d56-107">Retrieves an interface pointer to the file object associated with the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d56-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="17d56-108">Syntax</span></span>


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="17d56-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="17d56-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17d56-110">*ppfile* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="17d56-110">*ppFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17d56-111">Ein [**ibackgroundcopyfile**](ibackgroundcopyfile.md) -Schnittstellen Zeiger, dessen Methoden Sie verwenden, um die dem Fehler zugeordneten lokalen und Remote Dateinamen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="17d56-111">An [**IBackgroundCopyFile**](ibackgroundcopyfile.md) interface pointer whose methods you use to determine the local and remote file names associated with the error.</span></span> <span data-ttu-id="17d56-112">Der *ppfile* -Parameter wird auf **null** festgelegt, wenn der Fehler nicht der lokalen Datei oder Remote Datei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="17d56-112">The *ppFile* parameter is set to **NULL** if the error is not associated with the local or remote file.</span></span> <span data-ttu-id="17d56-113">Wenn Sie den Vorgang abgeschlossen haben, geben Sie *ppfile* frei</span><span class="sxs-lookup"><span data-stu-id="17d56-113">When done, release *ppFile*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17d56-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17d56-114">Return value</span></span>

<span data-ttu-id="17d56-115">Diese Methode gibt die folgenden **HRESULT** -Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="17d56-115">This method returns the following **HRESULT** values.</span></span>



| <span data-ttu-id="17d56-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="17d56-116">Return code</span></span>                                                                                                | <span data-ttu-id="17d56-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17d56-117">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="17d56-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="17d56-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>                   | <span data-ttu-id="17d56-119">Ein Schnittstellen Zeiger auf das Datei Objekt wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="17d56-119">Successfully retrieved an interface pointer to the file object.</span></span><br/>                                     |
| <dl> <span data-ttu-id="17d56-120"><dt>**DO_E_FILE_NOT_AVAILABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="17d56-120"><dt>**DO_E_FILE_NOT_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="17d56-121">Der Fehler ist keiner lokalen oder Remote Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="17d56-121">The error is not associated with a local or remote file.</span></span> <span data-ttu-id="17d56-122">Der *ppfile* -Parameter ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="17d56-122">The *ppFile* parameter is set to **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="17d56-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17d56-123">Requirements</span></span>



| <span data-ttu-id="17d56-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17d56-124">Requirement</span></span> | <span data-ttu-id="17d56-125">Wert</span><span class="sxs-lookup"><span data-stu-id="17d56-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17d56-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17d56-126">Minimum supported client</span></span><br/> | <span data-ttu-id="17d56-127">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17d56-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="17d56-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17d56-128">Minimum supported server</span></span><br/> | <span data-ttu-id="17d56-129">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17d56-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="17d56-130">Header</span><span class="sxs-lookup"><span data-stu-id="17d56-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="17d56-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="17d56-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="17d56-132">IDL</span><span class="sxs-lookup"><span data-stu-id="17d56-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17d56-133"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17d56-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="17d56-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="17d56-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="17d56-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17d56-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="17d56-136">DLL</span><span class="sxs-lookup"><span data-stu-id="17d56-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17d56-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17d56-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="17d56-138">IID</span><span class="sxs-lookup"><span data-stu-id="17d56-138">IID</span></span><br/>                      | <span data-ttu-id="17d56-139">IID_IBackgroundCopyError ist als 19c613a0-fcb8-4f 28-81ae-897c3d078-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="17d56-139">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="17d56-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17d56-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17d56-141">**Ibackgroundcopyerror**</span><span class="sxs-lookup"><span data-stu-id="17d56-141">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="17d56-142">**Ibackgroundcopyerror:: getError**</span><span class="sxs-lookup"><span data-stu-id="17d56-142">**IBackgroundCopyError::GetError**</span></span>](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





