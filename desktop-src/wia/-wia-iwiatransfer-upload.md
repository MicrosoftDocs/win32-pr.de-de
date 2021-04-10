---
description: Initiiert einen Daten Upload eines einzelnen Elements vom Aufrufer.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'Iwiatransfer:: Upload-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Upload
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6aae6ca8f86d07ec052fdd59d24b0da2b96599d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214652"
---
# <a name="iwiatransferupload-method"></a><span data-ttu-id="82bb2-103">Iwiatransfer:: Upload-Methode</span><span class="sxs-lookup"><span data-stu-id="82bb2-103">IWiaTransfer::Upload method</span></span>

<span data-ttu-id="82bb2-104">Initiiert einen Daten Upload eines einzelnen Elements vom Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="82bb2-104">Initiates a data upload of a single item from the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="82bb2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="82bb2-105">Syntax</span></span>


```C++
HRESULT Upload(
  [in] LONG                 lFlags,
  [in] IStream              *pSource,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="82bb2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="82bb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82bb2-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82bb2-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82bb2-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="82bb2-108">Type: **LONG**</span></span>

<span data-ttu-id="82bb2-109">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="82bb2-109">Currently unused.</span></span> <span data-ttu-id="82bb2-110">Sollte auf Null festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="82bb2-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="82bb2-111">*psource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82bb2-111">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82bb2-112">Typ: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="82bb2-112">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="82bb2-113">Gibt einen Zeiger auf die [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Daten an.</span><span class="sxs-lookup"><span data-stu-id="82bb2-113">Specifies a pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) data.</span></span>

</dd> <dt>

<span data-ttu-id="82bb2-114">_pIWiaTransferCallback \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82bb2-114">_pIWiaTransferCallback\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82bb2-115">Typ: \**[**iwiatransfercallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="82bb2-115">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="82bb2-116">Gibt einen Zeiger auf die [_ *iwiatransfercallback* \*](-wia-iwiatransfercallback.md) -Schnittstelle des Aufrufers an.</span><span class="sxs-lookup"><span data-stu-id="82bb2-116">Specifies a pointer to the caller's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82bb2-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82bb2-117">Return value</span></span>

<span data-ttu-id="82bb2-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="82bb2-118">Type: **HRESULT**</span></span>

<span data-ttu-id="82bb2-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="82bb2-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="82bb2-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="82bb2-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="82bb2-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82bb2-121">Requirements</span></span>



| <span data-ttu-id="82bb2-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82bb2-122">Requirement</span></span> | <span data-ttu-id="82bb2-123">Wert</span><span class="sxs-lookup"><span data-stu-id="82bb2-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82bb2-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82bb2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="82bb2-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82bb2-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="82bb2-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82bb2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="82bb2-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82bb2-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="82bb2-128">Header</span><span class="sxs-lookup"><span data-stu-id="82bb2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="82bb2-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="82bb2-129"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="82bb2-130">IDL</span><span class="sxs-lookup"><span data-stu-id="82bb2-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="82bb2-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="82bb2-131"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="82bb2-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="82bb2-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="82bb2-133"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82bb2-133"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
