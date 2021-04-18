---
description: Gibt eine Zeichenfolge zurück, die den Statuscode beschreibt.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: 'Iwiaerrorhandler:: GetStatus Description-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.GetStatusDescription
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: da23e413ee238f43ae577a51b18a542dc1b0768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368140"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a><span data-ttu-id="efb15-103">Iwiaerrorhandler:: GetStatus Description-Methode</span><span class="sxs-lookup"><span data-stu-id="efb15-103">IWiaErrorHandler::GetStatusDescription method</span></span>

<span data-ttu-id="efb15-104">Gibt eine Zeichenfolge zurück, die den Statuscode beschreibt.</span><span class="sxs-lookup"><span data-stu-id="efb15-104">Returns a string that describes the status code.</span></span>

## <a name="syntax"></a><span data-ttu-id="efb15-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="efb15-105">Syntax</span></span>


```C++
HRESULT GetStatusDescription(
  [in]  IUnknown *punkItem,
  [in]  HRESULT  hrStatus,
  [in]  LONG     cbResLength,
  [in]  BYTE     *pbData,
  [out] BSTR     *pbstrDescription
);
```



## <a name="parameters"></a><span data-ttu-id="efb15-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="efb15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efb15-107">*punkitem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efb15-107">*punkItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efb15-108">Typ: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="efb15-108">Type: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="efb15-109">Zeiger auf das [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) des übertragenen Elements.</span><span class="sxs-lookup"><span data-stu-id="efb15-109">Pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) of the item being transferred.</span></span> <span data-ttu-id="efb15-110">Dieses Objekt implementiert mindestens [_ *IWiaItem2* \*](-wia-iwiaitem2.md) und [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="efb15-110">This object minimally implements [_ *IWiaItem2*\*](-wia-iwiaitem2.md) and [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span>

</dd> <dt>

<span data-ttu-id="efb15-111">*hrStatus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efb15-111">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efb15-112">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="efb15-112">Type: **HRESULT**</span></span>

<span data-ttu-id="efb15-113">**HRESULT** , das der von [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)empfangene Statuscode ist.</span><span class="sxs-lookup"><span data-stu-id="efb15-113">**HRESULT** that is the status code received by [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="efb15-114">*cbreslength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efb15-114">*cbResLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efb15-115">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="efb15-115">Type: **LONG**</span></span>

<span data-ttu-id="efb15-116">**Long** , d. h. die Größe der Daten, auf die von *pbData* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="efb15-116">**LONG** that is the size of the data referred to by *pbData*.</span></span>

</dd> <dt>

<span data-ttu-id="efb15-117">*pbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efb15-117">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efb15-118">Typ: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="efb15-118">Type: \**BYTE\** _</span></span>

<span data-ttu-id="efb15-119">Zeiger auf den Datenpuffer, wie von [_ *banbeddatacallback* \*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)empfangen.</span><span class="sxs-lookup"><span data-stu-id="efb15-119">Pointer to the data buffer as received by [_ *BandedDataCallback*\*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="efb15-120">*pbstraudescription* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="efb15-120">*pbstrDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efb15-121">Geben Sie Folgendes ein: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="efb15-121">Type: \**BSTR\** _</span></span>

<span data-ttu-id="efb15-122">_ \*BSTR\*\*, das eine Beschreibung des Status oder Fehlers erhält, der während der Datenübertragung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="efb15-122">_ *BSTR*\* that receives a description of the status or error encountered during the data transfer.</span></span> <span data-ttu-id="efb15-123">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="efb15-123">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="efb15-124">Der Aufrufer muss die Zeichenfolge mit [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)freigeben, und der implemenor muss die Zeichenfolge mithilfe von " [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring)" zuordnen.</span><span class="sxs-lookup"><span data-stu-id="efb15-124">The caller must free the string using [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring), and the implementor must allocate the string using [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efb15-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="efb15-125">Return value</span></span>

<span data-ttu-id="efb15-126">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="efb15-126">Type: **HRESULT**</span></span>

<span data-ttu-id="efb15-127">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="efb15-127">Returns one of the following values.</span></span>



| <span data-ttu-id="efb15-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="efb15-128">Return code</span></span>                                                                             | <span data-ttu-id="efb15-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="efb15-129">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="efb15-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="efb15-130"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="efb15-131">*pbstraudescription* enthält einen gültigen **BSTR** -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="efb15-131">*pbstrDescription* contains a valid **BSTR** pointer.</span></span> <br/>  |
| <dl> <span data-ttu-id="efb15-132"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="efb15-132"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="efb15-133">*hrStatus* ist unbekannt, und es ist keine Beschreibung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="efb15-133">*hrStatus* is unknown and no description is available.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="efb15-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="efb15-134">Requirements</span></span>



| <span data-ttu-id="efb15-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="efb15-135">Requirement</span></span> | <span data-ttu-id="efb15-136">Wert</span><span class="sxs-lookup"><span data-stu-id="efb15-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="efb15-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="efb15-137">Minimum supported client</span></span><br/> | <span data-ttu-id="efb15-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efb15-138">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="efb15-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="efb15-139">Minimum supported server</span></span><br/> | <span data-ttu-id="efb15-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efb15-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="efb15-141">Header</span><span class="sxs-lookup"><span data-stu-id="efb15-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="efb15-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="efb15-142"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="efb15-143">IDL</span><span class="sxs-lookup"><span data-stu-id="efb15-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="efb15-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="efb15-144"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="efb15-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="efb15-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="efb15-146"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efb15-146"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
