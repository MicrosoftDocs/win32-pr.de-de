---
description: Durchsucht die Baumstruktur eines Elements anhand des Namens als Suchschlüssel.
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: 'IWiaItem2:: finditembyname-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.FindItemByName
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 821be7e4abd8d1396befa886093aa197bcdea7f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348791"
---
# <a name="iwiaitem2finditembyname-method"></a><span data-ttu-id="095ef-103">IWiaItem2:: finditembyname-Methode</span><span class="sxs-lookup"><span data-stu-id="095ef-103">IWiaItem2::FindItemByName method</span></span>

<span data-ttu-id="095ef-104">Durchsucht die Baumstruktur eines Elements anhand des Namens als Suchschlüssel.</span><span class="sxs-lookup"><span data-stu-id="095ef-104">Searches an item's tree of subitems using the name as the search key.</span></span>

## <a name="syntax"></a><span data-ttu-id="095ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="095ef-105">Syntax</span></span>


```C++
HRESULT FindItemByName(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrFullItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="095ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="095ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="095ef-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="095ef-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="095ef-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="095ef-108">Type: **LONG**</span></span>

<span data-ttu-id="095ef-109">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="095ef-109">Currently unused.</span></span> <span data-ttu-id="095ef-110">Sollte auf Null festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="095ef-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="095ef-111">*bstraufullitemname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="095ef-111">*bstrFullItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="095ef-112">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="095ef-112">Type: **BSTR**</span></span>

<span data-ttu-id="095ef-113">Gibt den Namen des zu suchenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="095ef-113">Specifies the name fo the item to search for.</span></span>

</dd> <dt>

<span data-ttu-id="095ef-114">*ppIWiaItem2* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="095ef-114">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="095ef-115">Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="095ef-115">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="095ef-116">Empfängt die Adresse eines Zeigers auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des gefundenen Elements.</span><span class="sxs-lookup"><span data-stu-id="095ef-116">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item found.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="095ef-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="095ef-117">Return value</span></span>

<span data-ttu-id="095ef-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="095ef-118">Type: **HRESULT**</span></span>

<span data-ttu-id="095ef-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="095ef-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="095ef-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="095ef-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="095ef-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="095ef-121">Remarks</span></span>

<span data-ttu-id="095ef-122">Mit dieser Methode wird die Struktur der untergeordneten Elemente des aktuellen Elements mithilfe des Namens als Suchschlüssel durchsucht.</span><span class="sxs-lookup"><span data-stu-id="095ef-122">This method searches the current item's tree of sub-items using the name as the search key.</span></span> <span data-ttu-id="095ef-123">Wenn **IWiaItem2:: finditembyname** das von *bstraufullitemname* angegebene Element findet, speichert es die Adresse eines Zeigers auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des Elements im *ppIWiaItem2* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="095ef-123">If **IWiaItem2::FindItemByName** finds the item specified by *bstrFullItemName*, it stores the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item in the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="095ef-124">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppIWiaItem2* -Parameter empfangen.</span><span class="sxs-lookup"><span data-stu-id="095ef-124">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="095ef-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="095ef-125">Requirements</span></span>



| <span data-ttu-id="095ef-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="095ef-126">Requirement</span></span> | <span data-ttu-id="095ef-127">Wert</span><span class="sxs-lookup"><span data-stu-id="095ef-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="095ef-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="095ef-128">Minimum supported client</span></span><br/> | <span data-ttu-id="095ef-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="095ef-129">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="095ef-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="095ef-130">Minimum supported server</span></span><br/> | <span data-ttu-id="095ef-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="095ef-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="095ef-132">Header</span><span class="sxs-lookup"><span data-stu-id="095ef-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="095ef-133"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="095ef-133"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="095ef-134">IDL</span><span class="sxs-lookup"><span data-stu-id="095ef-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="095ef-135"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="095ef-135"><dt>Wia.idl</dt></span></span> </dl> |



 

 
