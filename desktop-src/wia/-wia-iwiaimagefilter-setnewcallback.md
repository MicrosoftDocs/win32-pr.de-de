---
description: Legt einen neuen Anwendungs Rückruf für den Bild Verarbeitungs Filter fest, der für Weiterleitungs Aufrufe verwendet werden soll.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: 'Iwiaimagefilter:: setnewcallback-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.SetNewCallback
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 16325d854f7b17c62e6fb8254819078de64977f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752832"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a><span data-ttu-id="3dd61-103">Iwiaimagefilter:: setnewcallback-Methode</span><span class="sxs-lookup"><span data-stu-id="3dd61-103">IWiaImageFilter::SetNewCallback method</span></span>

<span data-ttu-id="3dd61-104">Legt einen neuen Anwendungs Rückruf für den Bild Verarbeitungs Filter fest, der für Weiterleitungs Aufrufe verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3dd61-104">Sets a new application callback for the image processing filter to use for forwarding calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dd61-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3dd61-105">Syntax</span></span>


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="3dd61-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dd61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dd61-107">*pwiatransfercallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3dd61-107">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd61-108">Typ: **[ **iwiatransfercallback**](-wia-iwiatransfercallback.md)**</span><span class="sxs-lookup"><span data-stu-id="3dd61-108">Type: **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)**</span></span>

<span data-ttu-id="3dd61-109">Gibt einen Zeiger auf die [**iwiatransfercallback**](-wia-iwiatransfercallback.md) -Schnittstelle der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="3dd61-109">Specifies a pointer to the application's [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dd61-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3dd61-110">Return value</span></span>

<span data-ttu-id="3dd61-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3dd61-111">Type: **HRESULT**</span></span>

<span data-ttu-id="3dd61-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3dd61-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3dd61-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3dd61-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dd61-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3dd61-114">Remarks</span></span>

<span data-ttu-id="3dd61-115">Nennen Sie diese Methode nicht direkt aus der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3dd61-115">Do not call this method directly from your application.</span></span>

<span data-ttu-id="3dd61-116">Der Bild Verarbeitungs Filter ist erforderlich, um die zuvor gespeicherte Anwendungs Rückruf Schnittstelle vor dem Festlegen des neuen Rückrufs freizugeben.</span><span class="sxs-lookup"><span data-stu-id="3dd61-116">The image processing filter is required to release the previously stored application callback interface before setting the new callback.</span></span>

<span data-ttu-id="3dd61-117">Wenn *pwiatransfercallback* **null** ist, sollte der Bild Verarbeitungs Filter einfach den alten Anwendungs Rückruf freigeben und S OK zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="3dd61-117">If *pWiaTransferCallback* is **NULL**, the image processing filter should simply release the old application callback and return S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dd61-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3dd61-118">Requirements</span></span>



| <span data-ttu-id="3dd61-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3dd61-119">Requirement</span></span> | <span data-ttu-id="3dd61-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3dd61-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3dd61-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3dd61-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3dd61-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dd61-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3dd61-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3dd61-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3dd61-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dd61-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3dd61-125">Header</span><span class="sxs-lookup"><span data-stu-id="3dd61-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dd61-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dd61-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="3dd61-127">IDL</span><span class="sxs-lookup"><span data-stu-id="3dd61-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3dd61-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3dd61-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 




