---
description: Gibt die von der ieaxiservice-Schnittstelle verwendeten Ressourcen frei.
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: 'Ieaxiservice:: Cleanup-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Cleanup
api_type:
- COM
api_location: ''
ms.openlocfilehash: b29784ae360ec78b9f7e01d2045617615333a5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217164"
---
# <a name="ieaxiservicecleanup-method"></a><span data-ttu-id="e8315-103">Ieaxiservice:: Cleanup-Methode</span><span class="sxs-lookup"><span data-stu-id="e8315-103">IeAxiService::Cleanup method</span></span>

<span data-ttu-id="e8315-104">Die **cleanupmethode** gibt Ressourcen frei, die von der [**ieaxiservice**](ieaxiservice.md) -Schnittstelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8315-104">The **Cleanup** method frees resources used by the [**IeAxiService**](ieaxiservice.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8315-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8315-105">Syntax</span></span>


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a><span data-ttu-id="e8315-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8315-106">Parameters</span></span>

<span data-ttu-id="e8315-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e8315-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8315-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8315-108">Return value</span></span>

<span data-ttu-id="e8315-109">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="e8315-109">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="e8315-110">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="e8315-110">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="e8315-111">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="e8315-111">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8315-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8315-112">Requirements</span></span>



| <span data-ttu-id="e8315-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8315-113">Requirement</span></span> | <span data-ttu-id="e8315-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e8315-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8315-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8315-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e8315-116">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8315-116">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e8315-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8315-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e8315-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e8315-118">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="e8315-119">IID</span><span class="sxs-lookup"><span data-stu-id="e8315-119">IID</span></span><br/>                      | <span data-ttu-id="e8315-120">IID \_ ieaxiservice ist definiert als E9E92380-9ecd-4982-A0EB-6815a56ccb27</span><span class="sxs-lookup"><span data-stu-id="e8315-120">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="e8315-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8315-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8315-122">**Ieaxiservice**</span><span class="sxs-lookup"><span data-stu-id="e8315-122">**IeAxiService**</span></span>](ieaxiservice.md)
</dt> </dl>

 

