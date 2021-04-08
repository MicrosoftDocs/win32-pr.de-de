---
title: Inapcomponentinfo-GetIcon-Methode (napcommon. h)
description: Wird vom NAP-System verwendet, um das Symbol eines Integritäts Clients zu erhalten.
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- GetIcon-Methode NAP
- GetIcon-Methode NAP, inapcomponentinfo-Schnittstelle
- Inapcomponentinfo-Schnittstelle NAP, GetIcon-Methode
topic_type:
- apiref
api_name:
- INapComponentInfo.GetIcon
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 795ad85f8497262f88fa55d8efb2da7466b8c3a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957083"
---
# <a name="inapcomponentinfogeticon-method"></a><span data-ttu-id="c824d-106">Inapcomponentinfo:: GetIcon-Methode</span><span class="sxs-lookup"><span data-stu-id="c824d-106">INapComponentInfo::GetIcon method</span></span>

> [!Note]  
> <span data-ttu-id="c824d-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c824d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c824d-108">Die **inapcomponentinfo:: GetIcon** -Rückruf Methode wird vom NAP-System verwendet, um das Symbol eines Integritäts Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c824d-108">The **INapComponentInfo::GetIcon** callback method is used by the NAP System to get the icon of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="c824d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c824d-109">Syntax</span></span>


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a><span data-ttu-id="c824d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c824d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c824d-111">*dllfilepath* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c824d-111">*dllFilePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c824d-112">Ein Zeiger auf einen Zeiger auf eine [**zählzeichenfolge**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , die verwendet wird, um den Dateipfad der dll zurückzugeben, die das Symbol enthält.</span><span class="sxs-lookup"><span data-stu-id="c824d-112">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) used to return the file path of the DLL that contains the icon.</span></span>

</dd> <dt>

<span data-ttu-id="c824d-113">*IconResourceID* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c824d-113">*iconResourceId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c824d-114">Ein Zeiger auf den Wert, der verwendet wird, um die Ressourcen-ID des zu verwendenden Symbols zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="c824d-114">A pointer to value used to return the resource ID of the icon to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c824d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c824d-115">Return value</span></span>

<span data-ttu-id="c824d-116">Gibt einen dieser Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="c824d-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="c824d-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c824d-117">Return code</span></span>                                                                                     | <span data-ttu-id="c824d-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c824d-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c824d-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c824d-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="c824d-120">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c824d-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="c824d-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="c824d-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="c824d-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="c824d-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c824d-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="c824d-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="c824d-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c824d-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c824d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c824d-125">Remarks</span></span>

<span data-ttu-id="c824d-126">Symbole sollten entsprechend der Sprach-ID des aufrufenden Threads lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c824d-126">Icons should be localized according to the calling thread's language-id.</span></span>

## <a name="requirements"></a><span data-ttu-id="c824d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c824d-127">Requirements</span></span>



| <span data-ttu-id="c824d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c824d-128">Requirement</span></span> | <span data-ttu-id="c824d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c824d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c824d-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c824d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c824d-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c824d-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c824d-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c824d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c824d-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c824d-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c824d-134">Header</span><span class="sxs-lookup"><span data-stu-id="c824d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c824d-135"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c824d-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="c824d-136">IDL</span><span class="sxs-lookup"><span data-stu-id="c824d-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c824d-137"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c824d-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c824d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c824d-138">See also</span></span>

<dl> <span data-ttu-id="c824d-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c824d-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="c824d-140">**Inapcomponentinfo**</span><span class="sxs-lookup"><span data-stu-id="c824d-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





