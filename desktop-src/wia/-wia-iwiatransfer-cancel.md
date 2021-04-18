---
description: Bricht den aktuellen Übertragungsvorgang ab.
ms.assetid: 42c6b2c3-7b6a-45d2-a7ce-844e95fe277b
title: 'Iwiatransfer:: Cancel-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Cancel
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 4764e922498a3c33278555cae37d09c1822959dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526459"
---
# <a name="iwiatransfercancel-method"></a><span data-ttu-id="19436-103">Iwiatransfer:: Cancel-Methode</span><span class="sxs-lookup"><span data-stu-id="19436-103">IWiaTransfer::Cancel method</span></span>

<span data-ttu-id="19436-104">Bricht den aktuellen Übertragungsvorgang ab.</span><span class="sxs-lookup"><span data-stu-id="19436-104">Cancels the current transfer operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="19436-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19436-105">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="19436-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="19436-106">Parameters</span></span>

<span data-ttu-id="19436-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="19436-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="19436-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19436-108">Return value</span></span>

<span data-ttu-id="19436-109">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="19436-109">Type: **HRESULT**</span></span>

<span data-ttu-id="19436-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="19436-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19436-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="19436-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="19436-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19436-112">Requirements</span></span>



| <span data-ttu-id="19436-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19436-113">Requirement</span></span> | <span data-ttu-id="19436-114">Wert</span><span class="sxs-lookup"><span data-stu-id="19436-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19436-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19436-115">Minimum supported client</span></span><br/> | <span data-ttu-id="19436-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19436-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="19436-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19436-117">Minimum supported server</span></span><br/> | <span data-ttu-id="19436-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19436-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="19436-119">Header</span><span class="sxs-lookup"><span data-stu-id="19436-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="19436-120"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="19436-120"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="19436-121">IDL</span><span class="sxs-lookup"><span data-stu-id="19436-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19436-122"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="19436-122"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="19436-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="19436-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="19436-124"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19436-124"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




