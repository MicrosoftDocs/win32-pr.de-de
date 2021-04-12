---
description: Initiiert einen Daten Download für den Aufrufer.
ms.assetid: e639fabb-2c13-4009-affa-1c2b06c0d4c8
title: Iwiatransfer::D ownload-Methode (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Download
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 2863915b850588d4db018693d9081ed2907d644a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526456"
---
# <a name="iwiatransferdownload-method"></a><span data-ttu-id="8ad6c-103">Iwiatransfer::D ownload-Methode</span><span class="sxs-lookup"><span data-stu-id="8ad6c-103">IWiaTransfer::Download method</span></span>

<span data-ttu-id="8ad6c-104">Initiiert einen Daten Download für den Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="8ad6c-104">Initiates a data download to the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ad6c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ad6c-105">Syntax</span></span>


```C++
HRESULT Download(
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="8ad6c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ad6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ad6c-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ad6c-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ad6c-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="8ad6c-108">Type: **LONG**</span></span>

<span data-ttu-id="8ad6c-109">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ad6c-109">Currently unused.</span></span> <span data-ttu-id="8ad6c-110">Sollte auf Null festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ad6c-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="8ad6c-111">*piwiatransfercallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ad6c-111">*pIWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ad6c-112">Typ: \**[**iwiatransfercallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="8ad6c-112">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="8ad6c-113">Gibt einen Zeiger auf die [_ *iwiatransfercallback* \*](-wia-iwiatransfercallback.md) -Schnittstelle des Aufrufers an.</span><span class="sxs-lookup"><span data-stu-id="8ad6c-113">Specifies a pointer to the caller's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ad6c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ad6c-114">Return value</span></span>

<span data-ttu-id="8ad6c-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8ad6c-115">Type: **HRESULT**</span></span>

<span data-ttu-id="8ad6c-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8ad6c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ad6c-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ad6c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ad6c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ad6c-118">Remarks</span></span>

<span data-ttu-id="8ad6c-119">Wenn ein Ordner heruntergeladen wird, werden alle untergeordneten Elemente dieses Ordners ebenfalls übertragen.</span><span class="sxs-lookup"><span data-stu-id="8ad6c-119">If a folder is downloaded, then all the child items of that folder are also transferred.</span></span> <span data-ttu-id="8ad6c-120">Jedes Element wird in einem separaten Stream übertragen.</span><span class="sxs-lookup"><span data-stu-id="8ad6c-120">Each item is transferred in a separate stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ad6c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ad6c-121">Requirements</span></span>



| <span data-ttu-id="8ad6c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ad6c-122">Requirement</span></span> | <span data-ttu-id="8ad6c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="8ad6c-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ad6c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ad6c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8ad6c-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ad6c-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8ad6c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ad6c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8ad6c-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ad6c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8ad6c-128">Header</span><span class="sxs-lookup"><span data-stu-id="8ad6c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ad6c-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ad6c-129"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="8ad6c-130">IDL</span><span class="sxs-lookup"><span data-stu-id="8ad6c-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8ad6c-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ad6c-131"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="8ad6c-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ad6c-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="8ad6c-133"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ad6c-133"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




