---
title: Getobjectdataonclearchannel-Methode
description: Die getobjectdataonclearchannel-Methode überträgt einen Block von Objektdaten auf einem unverschlüsselten Kanal zurück an den Windows Media-Device Manager.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Getobjectdataonclearchannel-Methode, Windows Media Device Manager
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25b72df0dd27289153a97221fefbcb58f3a5ad13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364409"
---
# <a name="getobjectdataonclearchannel-method"></a><span data-ttu-id="d8134-104">Getobjectdataonclearchannel-Methode</span><span class="sxs-lookup"><span data-stu-id="d8134-104">GetObjectDataOnClearChannel method</span></span>

<span data-ttu-id="d8134-105">Die **getobjectdataonclearchannel** -Methode überträgt einen Block von Objektdaten auf einem unverschlüsselten Kanal zurück an den Windows Media-Device Manager.</span><span class="sxs-lookup"><span data-stu-id="d8134-105">The **GetObjectDataOnClearChannel** method transfers a block of object data on a clear channel back to Windows Media Device Manager.</span></span>

<span data-ttu-id="d8134-106">Diese Methode ist mit [**iscpsecureexchange:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) identisch, mit dem Unterschied, dass die von dieser Methode zurückgegebenen Daten nicht verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="d8134-106">This method is identical to [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) except that the data returned by this method is not encrypted.</span></span> <span data-ttu-id="d8134-107">Folglich ist diese Methode effizienter.</span><span class="sxs-lookup"><span data-stu-id="d8134-107">Consequently this method is more efficient.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8134-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8134-108">Syntax</span></span>


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a><span data-ttu-id="d8134-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8134-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8134-110">*pdevice*</span><span class="sxs-lookup"><span data-stu-id="d8134-110">*pDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="d8134-111">Zeiger auf das Geräte Objekt.</span><span class="sxs-lookup"><span data-stu-id="d8134-111">Pointer to the device object.</span></span>

</dd> <dt>

<span data-ttu-id="d8134-112">*pData*</span><span class="sxs-lookup"><span data-stu-id="d8134-112">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="d8134-113">Zeiger auf einen Puffer zum Empfangen von Daten.</span><span class="sxs-lookup"><span data-stu-id="d8134-113">Pointer to a buffer to receive data.</span></span>

</dd> <dt>

<span data-ttu-id="d8134-114">*pdwSize*</span><span class="sxs-lookup"><span data-stu-id="d8134-114">*pdwSize*</span></span> 
</dt> <dd>

<span data-ttu-id="d8134-115">Zeiger auf ein **DWORD** , das die Übertragungs Größe enthält.</span><span class="sxs-lookup"><span data-stu-id="d8134-115">Pointer to a **DWORD** containing the transfer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8134-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8134-116">Return value</span></span>

<span data-ttu-id="d8134-117">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="d8134-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="d8134-118">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d8134-118">If the method fails, it returns an **HRESULT** error code.</span></span>



| <span data-ttu-id="d8134-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d8134-119">Return code</span></span>                                                                                                | <span data-ttu-id="d8134-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8134-120">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d8134-121"><dt>**Fehler beim Überprüfen von WMDM \_ E \_ Mac. \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8134-121"><dt>**WMDM\_E\_MAC\_CHECK\_FAILED**</dt></span></span> </dl> | <span data-ttu-id="d8134-122">Der Nachrichten Authentifizierungscode ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d8134-122">The message authentication code is not valid.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d8134-123"><dt>**WMDM \_ E- \_ norights**</dt></span><span class="sxs-lookup"><span data-stu-id="d8134-123"><dt>**WMDM\_E\_NORIGHTS**</dt></span></span> </dl>           | <span data-ttu-id="d8134-124">Der Aufrufer verfügt nicht über die erforderlichen Rechte, um den angeforderten Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d8134-124">The caller does not have the rights required to perform the requested operation.</span></span><br/> |
| <dl> <span data-ttu-id="d8134-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="d8134-125"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="d8134-126">Die Methode ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="d8134-126">The method failed.</span></span> <span data-ttu-id="d8134-127">Beenden Sie die Interaktion mit dem Inhaltsanbieter.</span><span class="sxs-lookup"><span data-stu-id="d8134-127">Terminate interaction with the content provider.</span></span><br/>              |
| <dl> <span data-ttu-id="d8134-128"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="d8134-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="d8134-129">Ein Parameter ist ein ungültiger oder **null** -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="d8134-129">A parameter is an invalid or **NULL** pointer.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d8134-130"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="d8134-130"><dt>**E\_FAIL**</dt></span></span> </dl>                     | <span data-ttu-id="d8134-131">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d8134-131">An unspecified error occurred.</span></span><br/>                                                   |



 

## <a name="remarks"></a><span data-ttu-id="d8134-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8134-132">Remarks</span></span>

<span data-ttu-id="d8134-133">Zum Übertragen von Daten ruft Windows Media Device Manager die [transfercontainerdataonclearchannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) -Methode auf, um die Containerdaten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8134-133">To transfer data, Windows Media Device Manager calls the [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) method to obtain the container data.</span></span> <span data-ttu-id="d8134-134">**Getobjectdataonclearchannel** wird aufgerufen, um Blöcke von Objektdaten vom Inhaltsanbieter an Windows Media Device Manager zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="d8134-134">**GetObjectDataOnClearChannel** is then called to transfer blocks of object data from the content provider to Windows Media Device Manager.</span></span> <span data-ttu-id="d8134-135">Wenn S \_ OK zurückgegeben wird und *pdwSize* auf NULL festgelegt ist, fordert Windows Media Device Manager keine weiteren Daten an.</span><span class="sxs-lookup"><span data-stu-id="d8134-135">If S\_OK is returned with *pdwSize* set to zero, Windows Media Device Manager will request no further data.</span></span>

<span data-ttu-id="d8134-136">Diese Methode ist mit [**iscpsecureexchange:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) identisch, mit dem Unterschied, dass die von dieser Methode zurückgegebenen Daten nicht verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="d8134-136">This method is identical to [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) except that the data returned by this method is not encrypted.</span></span> <span data-ttu-id="d8134-137">Folglich ist diese Methode effizienter.</span><span class="sxs-lookup"><span data-stu-id="d8134-137">Consequently this method is more efficient.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8134-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8134-138">Requirements</span></span>



| <span data-ttu-id="d8134-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8134-139">Requirement</span></span> | <span data-ttu-id="d8134-140">Wert</span><span class="sxs-lookup"><span data-stu-id="d8134-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8134-141">Header</span><span class="sxs-lookup"><span data-stu-id="d8134-141">Header</span></span><br/>  | <dl> <span data-ttu-id="d8134-142"><dt>Wmscp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d8134-142"><dt>WMSCP.idl</dt></span></span> </dl>    |
| <span data-ttu-id="d8134-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d8134-143">Library</span></span><br/> | <dl> <span data-ttu-id="d8134-144"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8134-144"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8134-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8134-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8134-146">**Iscpsecureexchange:: ObjectData**</span><span class="sxs-lookup"><span data-stu-id="d8134-146">**ISCPSecureExchange::ObjectData**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[<span data-ttu-id="d8134-147">**ISCPSecureExchange3-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d8134-147">**ISCPSecureExchange3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





