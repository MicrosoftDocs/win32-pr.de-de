---
description: Ruft Typinformationen eines Elements ab.
ms.assetid: 9670f184-e8ba-4596-af6d-2967320dfd95
title: 'IWiaItem2:: GetItemType-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemType
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3bf177ddcc117cdfe21a1b9322a0e457cf899c0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751784"
---
# <a name="iwiaitem2getitemtype-method"></a><span data-ttu-id="c4a3b-103">IWiaItem2:: GetItemType-Methode</span><span class="sxs-lookup"><span data-stu-id="c4a3b-103">IWiaItem2::GetItemType method</span></span>

<span data-ttu-id="c4a3b-104">Ruft Typinformationen eines Elements ab.</span><span class="sxs-lookup"><span data-stu-id="c4a3b-104">Gets an item's type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4a3b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4a3b-105">Syntax</span></span>


```C++
HRESULT GetItemType(
  [out] LONG *pItemType
);
```



## <a name="parameters"></a><span data-ttu-id="c4a3b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4a3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4a3b-107">*pitemtype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c4a3b-107">*pItemType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4a3b-108">Type: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="c4a3b-108">Type: \**LONG\** _</span></span>

<span data-ttu-id="c4a3b-109">Empfängt einen Zeiger auf ein _ \*Long\*\*, das eine Kombination von typfflags enthält.</span><span class="sxs-lookup"><span data-stu-id="c4a3b-109">Receives a pointer to a _ *LONG*\* that contains a combination of type flags.</span></span> <span data-ttu-id="c4a3b-110">Siehe [**WIA-Elementtyp-Flags**](-wia-wia-item-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c4a3b-110">See [**WIA Item Type Flags**](-wia-wia-item-type-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4a3b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4a3b-111">Return value</span></span>

<span data-ttu-id="c4a3b-112">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c4a3b-112">Type: **HRESULT**</span></span>

<span data-ttu-id="c4a3b-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c4a3b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c4a3b-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4a3b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4a3b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4a3b-115">Remarks</span></span>

<span data-ttu-id="c4a3b-116">Jedes [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt in der hierarchischen Struktur von Objekten, das einem Windows-Abbild Erfassungs-Hardware Gerät (WIA) 2,0 zugeordnet ist, verfügt über einen bestimmten Datentyp.</span><span class="sxs-lookup"><span data-stu-id="c4a3b-116">Every [**IWiaItem2**](-wia-iwiaitem2.md) object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) 2.0 hardware device has a specific data type.</span></span> <span data-ttu-id="c4a3b-117">Element Objekte stellen Ordner und Dateien dar.</span><span class="sxs-lookup"><span data-stu-id="c4a3b-117">Item objects represent folders and files.</span></span> <span data-ttu-id="c4a3b-118">Ordner enthalten Datei Objekte.</span><span class="sxs-lookup"><span data-stu-id="c4a3b-118">Folders contain file objects.</span></span> <span data-ttu-id="c4a3b-119">Datei Objekte enthalten Daten, die vom Gerät abgerufen werden, z. b. Bilder und Sounds.</span><span class="sxs-lookup"><span data-stu-id="c4a3b-119">File objects contain data acquired by the device such as images and sounds.</span></span> <span data-ttu-id="c4a3b-120">Diese Methode ermöglicht Anwendungen, den Typ jedes Elements in einer hierarchischen Struktur von Element Objekten in einem Gerät zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c4a3b-120">This method enables applications to identify the type of any item in a hierarchical tree of item objects in a device.</span></span>

<span data-ttu-id="c4a3b-121">Ein Element kann über mehr als einen Typ verfügen.</span><span class="sxs-lookup"><span data-stu-id="c4a3b-121">An item may have more than one type.</span></span> <span data-ttu-id="c4a3b-122">Beispielsweise verfügt ein Element, das eine Audiodatei darstellt, über die Typattribute [**wiaitemtypeaudiowiaitemtypefile**](-wia-wia-item-type-flags.md) \| .</span><span class="sxs-lookup"><span data-stu-id="c4a3b-122">For example, an item that represents an audio file will have the type attributes [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4a3b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4a3b-123">Requirements</span></span>



| <span data-ttu-id="c4a3b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4a3b-124">Requirement</span></span> | <span data-ttu-id="c4a3b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c4a3b-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a3b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4a3b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c4a3b-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4a3b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c4a3b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4a3b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c4a3b-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4a3b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c4a3b-130">Header</span><span class="sxs-lookup"><span data-stu-id="c4a3b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4a3b-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4a3b-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4a3b-132">IDL</span><span class="sxs-lookup"><span data-stu-id="c4a3b-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4a3b-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4a3b-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 




