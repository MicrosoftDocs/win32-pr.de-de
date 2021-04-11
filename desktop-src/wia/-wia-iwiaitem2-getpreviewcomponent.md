---
description: Ruft die Windows-Abbild Erwerbs-Vorschau Komponente (WIA) 2,0 ab.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: 'IWiaItem2:: getpreviewcomponent-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e0881f68044c30731322c89d6cc2f19ce7277a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129421"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a><span data-ttu-id="00182-103">IWiaItem2:: getpreviewcomponent-Methode</span><span class="sxs-lookup"><span data-stu-id="00182-103">IWiaItem2::GetPreviewComponent method</span></span>

<span data-ttu-id="00182-104">Ruft die Windows-Abbild Erwerbs-Vorschau Komponente (WIA) 2,0 ab.</span><span class="sxs-lookup"><span data-stu-id="00182-104">Gets the Windows Image Acquisition (WIA) 2.0 preview component.</span></span>

## <a name="syntax"></a><span data-ttu-id="00182-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="00182-105">Syntax</span></span>


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a><span data-ttu-id="00182-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="00182-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00182-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00182-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00182-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="00182-108">Type: **LONG**</span></span>

<span data-ttu-id="00182-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="00182-109">Not used.</span></span> <span data-ttu-id="00182-110">Auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="00182-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="00182-111">*ppwiapreview* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="00182-111">*ppWiaPreview* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00182-112">Typ: **[ **iwiapreview**](-wia-iwiapreview.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="00182-112">Type: **[**IWiaPreview**](-wia-iwiapreview.md)\*\***</span></span>

<span data-ttu-id="00182-113">Gibt die Adresse eines Zeigers auf die [**iwiapreview**](-wia-iwiapreview.md) -Schnittstelle der vorschaukomponente zurück.</span><span class="sxs-lookup"><span data-stu-id="00182-113">Returns the address of a pointer to the [**IWiaPreview**](-wia-iwiapreview.md) interface of the preview component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00182-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00182-114">Return value</span></span>

<span data-ttu-id="00182-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="00182-115">Type: **HRESULT**</span></span>

<span data-ttu-id="00182-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="00182-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="00182-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00182-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="00182-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00182-118">Remarks</span></span>

<span data-ttu-id="00182-119">Verwenden Sie diese Funktion, um einen Zeiger auf die Adresse der WIA 2,0-Vorschau Komponente für ein beliebiges [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt in der Objektstruktur eines WIA 2,0-Hardware Geräts zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="00182-119">Use this function to return a pointer to the address of the WIA 2.0 preview component for any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device.</span></span>

<span data-ttu-id="00182-120">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den Parameter *ppwiapreview* empfangen.</span><span class="sxs-lookup"><span data-stu-id="00182-120">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers that they receive through the *ppWiaPreview* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="00182-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00182-121">Requirements</span></span>



| <span data-ttu-id="00182-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00182-122">Requirement</span></span> | <span data-ttu-id="00182-123">Wert</span><span class="sxs-lookup"><span data-stu-id="00182-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00182-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00182-124">Minimum supported client</span></span><br/> | <span data-ttu-id="00182-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00182-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="00182-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00182-126">Minimum supported server</span></span><br/> | <span data-ttu-id="00182-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00182-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="00182-128">Header</span><span class="sxs-lookup"><span data-stu-id="00182-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="00182-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="00182-129"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="00182-130">IDL</span><span class="sxs-lookup"><span data-stu-id="00182-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="00182-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="00182-131"><dt>Wia.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00182-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00182-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00182-133">**IWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="00182-133">**IWiaItem2**</span></span>](-wia-iwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="00182-134">**Iwiapreview**</span><span class="sxs-lookup"><span data-stu-id="00182-134">**IWiaPreview**</span></span>](-wia-iwiapreview.md)
</dt> </dl>

 

 
