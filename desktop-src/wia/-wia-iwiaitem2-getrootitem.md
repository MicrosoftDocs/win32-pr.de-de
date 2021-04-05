---
description: Ruft das Stamm Element einer Struktur von Item-Objekten ab, die zum Darstellen eines Windows-Abbild Erwerbs (WIA) 2,0-Hardware Geräts verwendet werden.
ms.assetid: bc31ad4a-0851-4510-a038-83646ffd5c98
title: 'IWiaItem2:: GetRootItem-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetRootItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c8d4f004cc9c7cabaf4898f5e8c838a0399dc106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751777"
---
# <a name="iwiaitem2getrootitem-method"></a><span data-ttu-id="14829-103">IWiaItem2:: GetRootItem-Methode</span><span class="sxs-lookup"><span data-stu-id="14829-103">IWiaItem2::GetRootItem method</span></span>

<span data-ttu-id="14829-104">Ruft das Stamm Element einer Struktur von Item-Objekten ab, die zum Darstellen eines Windows-Abbild Erwerbs (WIA) 2,0-Hardware Geräts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14829-104">Gets the root item of a tree of item objects used to represent a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="14829-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14829-105">Syntax</span></span>


```C++
HRESULT GetRootItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="14829-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14829-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14829-107">*ppIWiaItem2* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="14829-107">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14829-108">Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="14829-108">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="14829-109">Empfängt die Adresse eines Zeigers auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des Stamm Elements.</span><span class="sxs-lookup"><span data-stu-id="14829-109">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14829-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14829-110">Return value</span></span>

<span data-ttu-id="14829-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="14829-111">Type: **HRESULT**</span></span>

<span data-ttu-id="14829-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="14829-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="14829-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="14829-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="14829-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14829-114">Remarks</span></span>

<span data-ttu-id="14829-115">Wenn ein beliebiges [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt in der Objektstruktur eines WIA 2,0-Hardware Geräts vorhanden ist, ruft die Anwendung durch Aufrufen dieser Funktion einen Zeiger auf das Stamm Element ab.</span><span class="sxs-lookup"><span data-stu-id="14829-115">Given any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device, the application retrieves a pointer to the root item by calling this function.</span></span>

<span data-ttu-id="14829-116">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppIWiaItem2* -Parameter empfangen.</span><span class="sxs-lookup"><span data-stu-id="14829-116">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="14829-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14829-117">Requirements</span></span>



| <span data-ttu-id="14829-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14829-118">Requirement</span></span> | <span data-ttu-id="14829-119">Wert</span><span class="sxs-lookup"><span data-stu-id="14829-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="14829-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14829-120">Minimum supported client</span></span><br/> | <span data-ttu-id="14829-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14829-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="14829-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14829-122">Minimum supported server</span></span><br/> | <span data-ttu-id="14829-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14829-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="14829-124">Header</span><span class="sxs-lookup"><span data-stu-id="14829-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="14829-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="14829-125"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="14829-126">IDL</span><span class="sxs-lookup"><span data-stu-id="14829-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14829-127"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14829-127"><dt>Wia.idl</dt></span></span> </dl> |



 

 
