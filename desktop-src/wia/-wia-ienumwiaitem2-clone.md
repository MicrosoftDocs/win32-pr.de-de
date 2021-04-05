---
description: Erstellt eine zusätzliche Instanz der IEnumWiaItem2-Schnittstelle und sendet einen Zeiger darauf zurück.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: 'IEnumWiaItem2:: Clone-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Clone
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3279e7db3efe66e940adbcb9677204e5df7867f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752872"
---
# <a name="ienumwiaitem2clone-method"></a><span data-ttu-id="f41cd-103">IEnumWiaItem2:: Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="f41cd-103">IEnumWiaItem2::Clone method</span></span>

<span data-ttu-id="f41cd-104">Erstellt eine zusätzliche Instanz der [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) -Schnittstelle und sendet einen Zeiger darauf zurück.</span><span class="sxs-lookup"><span data-stu-id="f41cd-104">Creates an additional instance of the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface and sends back a pointer to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="f41cd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f41cd-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="f41cd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f41cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f41cd-107">*ppiumum* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f41cd-107">*ppIEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f41cd-108">Typ: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f41cd-108">Type: **[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span></span>

<span data-ttu-id="f41cd-109">Empfängt die Adresse der [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) -Schnittstellen Instanz, die von **IEnumWiaItem2:: Clone** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f41cd-109">Receives the address of the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface instance that **IEnumWiaItem2::Clone** creates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f41cd-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f41cd-110">Return value</span></span>

<span data-ttu-id="f41cd-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f41cd-111">Type: **HRESULT**</span></span>

<span data-ttu-id="f41cd-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f41cd-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f41cd-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f41cd-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f41cd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f41cd-114">Remarks</span></span>

<span data-ttu-id="f41cd-115">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppienum* -Parameter empfangen.</span><span class="sxs-lookup"><span data-stu-id="f41cd-115">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f41cd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f41cd-116">Requirements</span></span>



| <span data-ttu-id="f41cd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f41cd-117">Requirement</span></span> | <span data-ttu-id="f41cd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f41cd-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f41cd-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f41cd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f41cd-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f41cd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f41cd-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f41cd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f41cd-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f41cd-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f41cd-123">Header</span><span class="sxs-lookup"><span data-stu-id="f41cd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f41cd-124"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f41cd-124"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="f41cd-125">IDL</span><span class="sxs-lookup"><span data-stu-id="f41cd-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f41cd-126"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f41cd-126"><dt>Wia.idl</dt></span></span> </dl> |



 

 
