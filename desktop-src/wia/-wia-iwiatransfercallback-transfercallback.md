---
description: Gibt den Fortschritt und andere Benachrichtigungen während einer Übertragung an.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: 'Iwiatransfercallback:: transfercallback-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.TransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: f1e2f939a7a3d768fc744c0603563b0a088e08f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354496"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a><span data-ttu-id="34e1a-103">Iwiatransfercallback:: transfercallback-Methode</span><span class="sxs-lookup"><span data-stu-id="34e1a-103">IWiaTransferCallback::TransferCallback method</span></span>

<span data-ttu-id="34e1a-104">Gibt den Fortschritt und andere Benachrichtigungen während einer Übertragung an.</span><span class="sxs-lookup"><span data-stu-id="34e1a-104">Provides progress and other notifications during a transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e1a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34e1a-105">Syntax</span></span>


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a><span data-ttu-id="34e1a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="34e1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34e1a-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34e1a-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e1a-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="34e1a-108">Type: **LONG**</span></span>

<span data-ttu-id="34e1a-109">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34e1a-109">Currently unused.</span></span> <span data-ttu-id="34e1a-110">Sollte auf Null festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="34e1a-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="34e1a-111">*pwiatransferpara* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34e1a-111">*pWiaTransferParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e1a-112">Typ: \**[**wiatransferparameams**](-wia-wiatransferparams.md) \** _</span><span class="sxs-lookup"><span data-stu-id="34e1a-112">Type: \**[**WiaTransferParams**](-wia-wiatransferparams.md)\** _</span></span>

<span data-ttu-id="34e1a-113">Gibt einen Zeiger auf eine [_ *wiatransferparameams* \*](-wia-wiatransferparams.md) -Struktur an.</span><span class="sxs-lookup"><span data-stu-id="34e1a-113">Specifies a pointer to a [_ *WiaTransferParams*\*](-wia-wiatransferparams.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34e1a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34e1a-114">Return value</span></span>

<span data-ttu-id="34e1a-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="34e1a-115">Type: **HRESULT**</span></span>

<span data-ttu-id="34e1a-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="34e1a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="34e1a-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="34e1a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="34e1a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34e1a-118">Remarks</span></span>

<span data-ttu-id="34e1a-119">Wenn diese Methode von einem Bild Verarbeitungs Filter implementiert wird, ruft der Windows-Abbild Erwerb (WIA) 2,0 Mini Treiber Sie während der Abbild Erfassung auf, um Statusmeldungen an die Anwendung zurückzusenden.</span><span class="sxs-lookup"><span data-stu-id="34e1a-119">When this method is implemented by an image processing filter, the Windows Image Acquisition (WIA) 2.0 minidriver calls it during image acquisition to send progress messages back to the application.</span></span>

<span data-ttu-id="34e1a-120">**Iwiatransfercallback:: transfercallback** eines Filters muss an die **iwiatransfercallback:: transfercallback** -Methode des Anwendungs Rückrufs delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="34e1a-120">A filter's **IWiaTransferCallback::TransferCallback** must delegate to the application callback's **IWiaTransferCallback::TransferCallback** method.</span></span> <span data-ttu-id="34e1a-121">Normalerweise filtert der Filterdaten Strom die an ihn über gebenden Daten und schreibt die gefilterten Daten direkt in den von der Anwendung bereitgestellten Stream.</span><span class="sxs-lookup"><span data-stu-id="34e1a-121">Usually, the filter stream filters the data passed to it and writes the filtered data directly to the application provided stream.</span></span> <span data-ttu-id="34e1a-122">Wenn der Bild Verarbeitungs Filterdaten zwischen Aufrufen der [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) -Methode speichert, muss er auch die Werte *lprozentucomplete* und *ulbytesschreibbcurrentstream* in der [**wiatransferparameams**](-wia-wiatransferparams.md) -Struktur ändern.</span><span class="sxs-lookup"><span data-stu-id="34e1a-122">When image processing filter stores data between calls to its [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) method, it must also modify the *lPercentComplete* and *ulBytesWrittenToCurrentStream* values in the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="34e1a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34e1a-123">Requirements</span></span>



| <span data-ttu-id="34e1a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34e1a-124">Requirement</span></span> | <span data-ttu-id="34e1a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="34e1a-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34e1a-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34e1a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="34e1a-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34e1a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="34e1a-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34e1a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="34e1a-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34e1a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="34e1a-130">Header</span><span class="sxs-lookup"><span data-stu-id="34e1a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="34e1a-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="34e1a-131"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="34e1a-132">IDL</span><span class="sxs-lookup"><span data-stu-id="34e1a-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="34e1a-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="34e1a-133"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="34e1a-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34e1a-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="34e1a-135"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34e1a-135"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
