---
description: Proxy Funktion für die Commit-Methode.
ms.assetid: f7f1be43-fe44-47eb-a5ba-3446c0db22a6
title: IWICBitmapEncoder_Commit_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c0cd3cfbe5e1c80d82cd90303d26f2da33cf467d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041699"
---
# <a name="iwicbitmapencoder_commit_proxy-function"></a><span data-ttu-id="64bb6-103">Iwicbitmapcoder \_ Commit- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="64bb6-103">IWICBitmapEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="64bb6-104">Proxy Funktion für die [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) -Methode.</span><span class="sxs-lookup"><span data-stu-id="64bb6-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="64bb6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64bb6-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Commit_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="64bb6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="64bb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64bb6-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64bb6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64bb6-108">Typ: \**[**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="64bb6-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="64bb6-109">Zeiger auf dieses [_ *iwicbitmapcoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="64bb6-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64bb6-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64bb6-110">Return value</span></span>

<span data-ttu-id="64bb6-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="64bb6-111">Type: **HRESULT**</span></span>

<span data-ttu-id="64bb6-112">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="64bb6-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="64bb6-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="64bb6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="64bb6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64bb6-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="64bb6-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="64bb6-115">Requirements</span></span>



| <span data-ttu-id="64bb6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64bb6-116">Requirement</span></span> | <span data-ttu-id="64bb6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="64bb6-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64bb6-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64bb6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="64bb6-119">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64bb6-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="64bb6-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64bb6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="64bb6-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64bb6-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="64bb6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="64bb6-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64bb6-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64bb6-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




