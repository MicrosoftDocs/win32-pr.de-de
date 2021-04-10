---
description: Überspringt die angegebene Anzahl von Elementen während einer Enumeration verfügbarer IWiaItem2-Objekte.
ms.assetid: 7a5e9e1c-1e6e-4de0-9499-bf89e35c19aa
title: 'IEnumWiaItem2:: Skip-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Skip
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7618aad923136a9a32d8b7fb935050fefe07bff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959092"
---
# <a name="ienumwiaitem2skip-method"></a><span data-ttu-id="5bdf3-103">IEnumWiaItem2:: Skip-Methode</span><span class="sxs-lookup"><span data-stu-id="5bdf3-103">IEnumWiaItem2::Skip method</span></span>

<span data-ttu-id="5bdf3-104">Überspringt die angegebene Anzahl von Elementen während einer Enumeration verfügbarer [**IWiaItem2**](-wia-iwiaitem2.md) -Objekte.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-104">Skips the specified number of items during an enumeration of available [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bdf3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bdf3-105">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG cElt
);
```



## <a name="parameters"></a><span data-ttu-id="5bdf3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bdf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bdf3-107">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bdf3-107">*cElt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bdf3-108">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="5bdf3-108">Type: **ULONG**</span></span>

<span data-ttu-id="5bdf3-109">Gibt die Anzahl der zu über springenden Elemente an.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-109">Specifies the number of items to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bdf3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5bdf3-110">Return value</span></span>

<span data-ttu-id="5bdf3-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5bdf3-111">Type: **HRESULT**</span></span>

<span data-ttu-id="5bdf3-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5bdf3-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bdf3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bdf3-114">Requirements</span></span>



| <span data-ttu-id="5bdf3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bdf3-115">Requirement</span></span> | <span data-ttu-id="5bdf3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5bdf3-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5bdf3-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5bdf3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5bdf3-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bdf3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5bdf3-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5bdf3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5bdf3-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bdf3-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5bdf3-121">Header</span><span class="sxs-lookup"><span data-stu-id="5bdf3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bdf3-122"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bdf3-122"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="5bdf3-123">IDL</span><span class="sxs-lookup"><span data-stu-id="5bdf3-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5bdf3-124"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5bdf3-124"><dt>Wia.idl</dt></span></span> </dl> |



 

 




