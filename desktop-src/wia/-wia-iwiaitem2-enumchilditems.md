---
description: Erstellt ein Enumeratorobjekt und übergibt einen Zeiger auf seine IEnumWiaItem2-Schnittstelle für Ordner mit Elementen in der IWiaItem2-Struktur eines Windows-Abbild Erwerbs (WIA) 2,0-Geräts.
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: 'IWiaItem2:: enumchilditems-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumChildItems
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2de76d9bf43d10e08e5a85cd2a32d6b377680d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485067"
---
# <a name="iwiaitem2enumchilditems-method"></a><span data-ttu-id="77f2c-103">IWiaItem2:: enumchilditems-Methode</span><span class="sxs-lookup"><span data-stu-id="77f2c-103">IWiaItem2::EnumChildItems method</span></span>

<span data-ttu-id="77f2c-104">Erstellt ein Enumeratorobjekt und übergibt einen Zeiger auf seine [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) -Schnittstelle für Ordner mit Elementen in der [**IWiaItem2**](-wia-iwiaitem2.md) -Struktur eines Windows-Abbild Erwerbs (WIA) 2,0-Geräts.</span><span class="sxs-lookup"><span data-stu-id="77f2c-104">Creates an enumerator object and passes back a pointer to its [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface for folders with items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree of a Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="77f2c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="77f2c-105">Syntax</span></span>


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="77f2c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="77f2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77f2c-107">*pcategoryguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77f2c-107">*pCategoryGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77f2c-108">Geben Sie Folgendes ein: \* Konstante *GUID \** _</span><span class="sxs-lookup"><span data-stu-id="77f2c-108">Type: \**const GUID\** _</span></span>

<span data-ttu-id="77f2c-109">Gibt einen Zeiger auf eine Kategorie an, für die untergeordnete Knoten aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="77f2c-109">Specifies a pointer to a category for which child nodes are enumerated.</span></span> <span data-ttu-id="77f2c-110">Wenn _ \* NULL \* \*, werden alle untergeordneten Knoten aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="77f2c-110">If _\*NULL\*\*, then all child nodes are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="77f2c-111">*ppIEnumWiaItem2* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="77f2c-111">*ppIEnumWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77f2c-112">Typ: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="77f2c-112">Type: **[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span></span>

<span data-ttu-id="77f2c-113">Empfängt die Adresse eines Zeigers auf die [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) -Schnittstelle, die von dieser Methode erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="77f2c-113">Receives the address of a pointer to the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface that this method creates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77f2c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77f2c-114">Return value</span></span>

<span data-ttu-id="77f2c-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="77f2c-115">Type: **HRESULT**</span></span>

<span data-ttu-id="77f2c-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="77f2c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="77f2c-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="77f2c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="77f2c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77f2c-118">Remarks</span></span>

<span data-ttu-id="77f2c-119">Das WIA 2,0-Laufzeitsystem stellt jedes WIA 2,0-Hardware Gerät als hierarchische Struktur von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="77f2c-119">The WIA 2.0 run-time system represents each WIA 2.0 hardware device as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="77f2c-120">Mit der **IWiaItem2:: enumchilditems** -Methode können Anwendungen untergeordnete Elemente im aktuellen Element aufzählen.</span><span class="sxs-lookup"><span data-stu-id="77f2c-120">The **IWiaItem2::EnumChildItems** method enables applications to enumerate child items in the current item.</span></span> <span data-ttu-id="77f2c-121">Sie kann jedoch nur auf Elemente angewendet werden, bei denen es sich um Ordner handelt.</span><span class="sxs-lookup"><span data-stu-id="77f2c-121">However, it can only be applied to items that are folders.</span></span>

<span data-ttu-id="77f2c-122">Wenn der Ordner nicht leer ist, enthält er eine Teilstruktur von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="77f2c-122">If the folder is not empty, it contains a subtree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="77f2c-123">Mit der **IWiaItem2:: enumchilditems** -Methode werden alle im Ordner enthaltenen Elemente aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="77f2c-123">The **IWiaItem2::EnumChildItems** method enumerates all of the items contained in the folder.</span></span> <span data-ttu-id="77f2c-124">Es speichert einen Zeiger auf einen Enumerator im *ppIEnumWiaItem2* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="77f2c-124">It stores a pointer to an enumerator in the *ppIEnumWiaItem2* parameter.</span></span> <span data-ttu-id="77f2c-125">Anwendungen verwenden den enumeratorzeiger, um die Enumeration der untergeordneten Elemente eines Objekts auszuführen.</span><span class="sxs-lookup"><span data-stu-id="77f2c-125">Applications use the enumerator pointer to perform the enumeration of an object's child items.</span></span>

<span data-ttu-id="77f2c-126">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppIEnumWiaItem2* -Parameter empfangen.</span><span class="sxs-lookup"><span data-stu-id="77f2c-126">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnumWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="77f2c-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77f2c-127">Requirements</span></span>



| <span data-ttu-id="77f2c-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77f2c-128">Requirement</span></span> | <span data-ttu-id="77f2c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="77f2c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77f2c-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77f2c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="77f2c-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77f2c-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="77f2c-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77f2c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="77f2c-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77f2c-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="77f2c-134">Header</span><span class="sxs-lookup"><span data-stu-id="77f2c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="77f2c-135"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="77f2c-135"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="77f2c-136">IDL</span><span class="sxs-lookup"><span data-stu-id="77f2c-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="77f2c-137"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="77f2c-137"><dt>Wia.idl</dt></span></span> </dl> |



 

 
