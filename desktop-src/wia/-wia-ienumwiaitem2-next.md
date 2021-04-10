---
description: Füllt ein Array von Zeigern auf IWiaItem2-Schnittstellen auf.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: 'IEnumWiaItem2:: Next-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Next
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e8800ead0c8f0abaddd0f055f31962d4d55d14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214835"
---
# <a name="ienumwiaitem2next-method"></a><span data-ttu-id="4a6de-103">IEnumWiaItem2:: Next-Methode</span><span class="sxs-lookup"><span data-stu-id="4a6de-103">IEnumWiaItem2::Next method</span></span>

<span data-ttu-id="4a6de-104">Füllt ein Array von Zeigern auf [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstellen auf.</span><span class="sxs-lookup"><span data-stu-id="4a6de-104">Fills an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a6de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a6de-105">Syntax</span></span>


```C++
HRESULT Next(
  [in]      ULONG     cElt,
  [out]     IWiaItem2 **ppIWiaItem2,
  [in, out] ULONG     *pcEltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="4a6de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a6de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a6de-107">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a6de-107">*cElt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6de-108">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="4a6de-108">Type: **ULONG**</span></span>

<span data-ttu-id="4a6de-109">Gibt die Anzahl der Array Elemente in dem Array an, das durch den *ppIWiaItem2* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4a6de-109">Specifies the number of array elements in the array indicated by the *ppIWiaItem2* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4a6de-110">*ppIWiaItem2* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4a6de-110">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6de-111">Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="4a6de-111">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="4a6de-112">Empfängt die Adresse eines Arrays von [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstellen Zeigern.</span><span class="sxs-lookup"><span data-stu-id="4a6de-112">Receives the address of an array of [**IWiaItem2**](-wia-iwiaitem2.md) interface pointers.</span></span> <span data-ttu-id="4a6de-113">**IEnumWiaItem2:: Next** füllt dieses Array mit Schnittstellen Zeigern.</span><span class="sxs-lookup"><span data-stu-id="4a6de-113">**IEnumWiaItem2::Next** fills this array with interface pointers.</span></span>

</dd> <dt>

<span data-ttu-id="4a6de-114">*pceltfetch* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4a6de-114">*pcEltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6de-115">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="4a6de-115">Type: \**ULONG\** _</span></span>

<span data-ttu-id="4a6de-116">Bei der Ausgabe empfängt dieser Parameter die Anzahl der Schnittstellen Zeiger, die tatsächlich in dem Array gespeichert werden, das durch den _ppIWiaItem2 \*-Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4a6de-116">On output, this parameter receives the number of interface pointers actually stored in the array indicated by the _ppIWiaItem2\* parameter.</span></span> <span data-ttu-id="4a6de-117">Wenn die Enumeration fertig ist, enthält dieser Parameter 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4a6de-117">When the enumeration is complete, this parameter contains zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a6de-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a6de-118">Return value</span></span>

<span data-ttu-id="4a6de-119">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4a6de-119">Type: **HRESULT**</span></span>

<span data-ttu-id="4a6de-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="4a6de-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a6de-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4a6de-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a6de-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a6de-122">Remarks</span></span>

<span data-ttu-id="4a6de-123">Das Windows Image Acquisition (WIA) 2,0-Laufzeitsystem stellt WIA 2,0-Hardware Geräte als hierarchische Struktur von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="4a6de-123">The Windows Image Acquisition (WIA) 2.0 run-time system represents WIA 2.0 hardware devices as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="4a6de-124">Anwendungen verwenden die **IEnumWiaItem2:: Next** -Methode zum Abrufen eines **IWiaItem2** -Schnittstellen Zeigers für jedes Element im aktuellen Ordner der **IWiaItem2** -Objektstruktur eines Hardware Geräts.</span><span class="sxs-lookup"><span data-stu-id="4a6de-124">Applications use the **IEnumWiaItem2::Next** method to obtain an **IWiaItem2** interface pointer for each item in the current folder of a hardware device's **IWiaItem2** object tree.</span></span>

<span data-ttu-id="4a6de-125">Um die Liste der Zeiger zu erhalten, übergibt die Anwendung ein Array von [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstellen Zeigern, die Sie zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4a6de-125">To obtain the list of pointers, the application passes an array of [**IWiaItem2**](-wia-iwiaitem2.md) interface pointers that it allocates.</span></span> <span data-ttu-id="4a6de-126">Außerdem wird die Anzahl der Array Elemente im *celt*-Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="4a6de-126">It also passes the number of array elements in the parameter *cElt*.</span></span> <span data-ttu-id="4a6de-127">Die **IEnumWiaItem2:: Next** -Methode füllt das Array mit Zeigern auf **IWiaItem2** -Schnittstellen auf.</span><span class="sxs-lookup"><span data-stu-id="4a6de-127">The **IEnumWiaItem2::Next** method fills the array with pointers to **IWiaItem2** interfaces.</span></span>

<span data-ttu-id="4a6de-128">Bis der enumerationsprozess abgeschlossen ist, gibt die **IEnumWiaItem2:: Next** -Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="4a6de-128">Until the enumeration process completes, the **IEnumWiaItem2::Next** method returns S\_OK.</span></span> <span data-ttu-id="4a6de-129">Jedes Mal, wenn dies der Fall ist, wird der Wert, auf den *pceltfetch* zeigt, auf die Anzahl der in das Array eingefügten Elemente festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a6de-129">Each time it does, it sets the value pointed to by *pcEltFetched* to the number of items it inserted into the array.</span></span> <span data-ttu-id="4a6de-130">Wenn **IEnumWiaItem2:: Next** den Prozess der Enumeration von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten abschließt, wird S false zurückgegeben, \_ und der Speicher Speicherort, auf den *pceltfetch* verweist, wird auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a6de-130">When **IEnumWiaItem2::Next** finishes the process of enumerating [**IWiaItem2**](-wia-iwiaitem2.md) objects, it returns S\_FALSE and sets the memory location pointed to by *pcEltFetched* to zero.</span></span>

<span data-ttu-id="4a6de-131">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppIWiaItem2* -Parameter empfangen.</span><span class="sxs-lookup"><span data-stu-id="4a6de-131">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a6de-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a6de-132">Requirements</span></span>



| <span data-ttu-id="4a6de-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a6de-133">Requirement</span></span> | <span data-ttu-id="4a6de-134">Wert</span><span class="sxs-lookup"><span data-stu-id="4a6de-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a6de-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a6de-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4a6de-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a6de-136">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4a6de-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a6de-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4a6de-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a6de-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4a6de-139">Header</span><span class="sxs-lookup"><span data-stu-id="4a6de-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a6de-140"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a6de-140"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a6de-141">IDL</span><span class="sxs-lookup"><span data-stu-id="4a6de-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4a6de-142"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4a6de-142"><dt>Wia.idl</dt></span></span> </dl> |



 

 
