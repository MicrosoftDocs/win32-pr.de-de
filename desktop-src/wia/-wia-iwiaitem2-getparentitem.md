---
description: Ruft das übergeordnete Element in der-Struktur ab, das ein Windows-Abbild Erfassungs-Hardware Gerät (WIA) 2,0 darstellt.
ms.assetid: c6fdaf1d-9875-4852-893c-813894d89f6c
title: 'IWiaItem2:: getparameentitem-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetParentItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 055625b98807103c3b79109216f6081d00564b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343668"
---
# <a name="iwiaitem2getparentitem-method"></a><span data-ttu-id="9adad-103">IWiaItem2:: getparameentitem-Methode</span><span class="sxs-lookup"><span data-stu-id="9adad-103">IWiaItem2::GetParentItem method</span></span>

<span data-ttu-id="9adad-104">Ruft das übergeordnete Element in der-Struktur ab, das ein Windows-Abbild Erfassungs-Hardware Gerät (WIA) 2,0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="9adad-104">Gets the parent item in the tree that represents a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9adad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9adad-105">Syntax</span></span>


```C++
HRESULT GetParentItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="9adad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9adad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9adad-107">*ppIWiaItem2* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9adad-107">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9adad-108">Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9adad-108">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="9adad-109">Empfängt die Adresse eines Zeigers auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des übergeordneten Elements des Elements in der Struktur von Item-Objekten.</span><span class="sxs-lookup"><span data-stu-id="9adad-109">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the parent of the item in the tree of item objects.</span></span> <span data-ttu-id="9adad-110">Wenn diese Methode für den Stamm der Struktur aufgerufen wird, ist die zurückgegebene Adresse **null**.</span><span class="sxs-lookup"><span data-stu-id="9adad-110">If this method is called on the root of the tree, then the returned address is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9adad-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9adad-111">Return value</span></span>

<span data-ttu-id="9adad-112">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9adad-112">Type: **HRESULT**</span></span>

<span data-ttu-id="9adad-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9adad-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9adad-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9adad-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9adad-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9adad-115">Remarks</span></span>

<span data-ttu-id="9adad-116">Wenn ein beliebiges [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt in der Objektstruktur eines WIA 2,0-Hardware Geräts vorhanden ist, ruft die Anwendung einen Zeiger auf das übergeordnete Element ab, indem diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9adad-116">Given any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device, the application retrieves a pointer to the parent item by calling this function.</span></span>

<span data-ttu-id="9adad-117">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppIWiaItem2* -Parameter empfangen, wenn diese Zeiger nicht **null** sind.</span><span class="sxs-lookup"><span data-stu-id="9adad-117">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter if these pointers are not **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9adad-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9adad-118">Requirements</span></span>



| <span data-ttu-id="9adad-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9adad-119">Requirement</span></span> | <span data-ttu-id="9adad-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9adad-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9adad-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9adad-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9adad-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9adad-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9adad-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9adad-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9adad-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9adad-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9adad-125">Header</span><span class="sxs-lookup"><span data-stu-id="9adad-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9adad-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9adad-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="9adad-127">IDL</span><span class="sxs-lookup"><span data-stu-id="9adad-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9adad-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9adad-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 
