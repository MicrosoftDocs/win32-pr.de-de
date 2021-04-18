---
description: Ermöglicht dem Bild Verarbeitungs Filter das Zurückschreiben von Eigenschaften an den Treiber (und das Gerät).
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: 'Iwiaimagefilter:: applyproperties-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.ApplyProperties
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3c20527ee587b975adea34e7c480349836620015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347375"
---
# <a name="iwiaimagefilterapplyproperties-method"></a><span data-ttu-id="6ee4c-103">Iwiaimagefilter:: applyproperties-Methode</span><span class="sxs-lookup"><span data-stu-id="6ee4c-103">IWiaImageFilter::ApplyProperties method</span></span>

<span data-ttu-id="6ee4c-104">Ermöglicht dem Bild Verarbeitungs Filter das Zurückschreiben von Eigenschaften an den Treiber (und das Gerät).</span><span class="sxs-lookup"><span data-stu-id="6ee4c-104">Enables the image processing filter to write properties back to the driver (and device).</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee4c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ee4c-105">Syntax</span></span>


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a><span data-ttu-id="6ee4c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ee4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ee4c-107">*pwiapropertystorage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ee4c-107">*pWiaPropertyStorage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee4c-108">Typ: \**[**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) \** _</span><span class="sxs-lookup"><span data-stu-id="6ee4c-108">Type: \**[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)\** _</span></span>

<span data-ttu-id="6ee4c-109">Gibt einen Zeiger auf den [_ *iwiapropertystorage* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) für die anzuwendenden Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-109">Specifies a pointer to the [_ *IWiaPropertyStorage*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) for the properties to be applied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ee4c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ee4c-110">Return value</span></span>

<span data-ttu-id="6ee4c-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6ee4c-111">Type: **HRESULT**</span></span>

<span data-ttu-id="6ee4c-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6ee4c-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ee4c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ee4c-114">Remarks</span></span>

<span data-ttu-id="6ee4c-115">Nennen Sie diese Methode nicht direkt aus der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-115">Do not call this method directly from your application.</span></span> <span data-ttu-id="6ee4c-116">Sie wird von der Windows-Abbild Beschaffung (WIA) 2,0 aufgerufen, nachdem der Bild Verarbeitungs Filter die Rohdaten verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-116">It is called by Windows Image Acquisition (WIA) 2.0 after the image processing filter has processed the raw data.</span></span>

<span data-ttu-id="6ee4c-117">*pwiapropertystorage* ist die Schnittstelle [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) , in der der Bild Verarbeitungs Filtereigenschaften schreiben soll.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-117">*pWiaPropertyStorage* is the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface into which the image processing filter should write properties.</span></span> <span data-ttu-id="6ee4c-118">Ein Bild Verarbeitungs Filter sollte nur die Methode [IPropertyStorage:: schreitemultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) zum Schreiben von Eigenschaften verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-118">An image processing filter should use only the [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) method to write properties.</span></span>

<span data-ttu-id="6ee4c-119">Diese Methode ermöglicht dem Bild Verarbeitungs Filter das Zurückschreiben von Eigenschaften an den Treiber (und das Gerät).</span><span class="sxs-lookup"><span data-stu-id="6ee4c-119">This method allows the image processing filter to write properties back to the driver (and device).</span></span> <span data-ttu-id="6ee4c-120">Dies kann für Filter notwendig sein, die Funktionen wie die automatische Verfügbarkeit während der Überprüfung von Filmen implementieren.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-120">This may be necessary for filters that implement features such as auto-exposure during film scanning.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ee4c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ee4c-121">Requirements</span></span>



| <span data-ttu-id="6ee4c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ee4c-122">Requirement</span></span> | <span data-ttu-id="6ee4c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6ee4c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee4c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ee4c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee4c-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ee4c-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6ee4c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ee4c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee4c-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ee4c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6ee4c-128">Header</span><span class="sxs-lookup"><span data-stu-id="6ee4c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ee4c-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ee4c-129"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ee4c-130">IDL</span><span class="sxs-lookup"><span data-stu-id="6ee4c-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ee4c-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ee4c-131"><dt>Wia.idl</dt></span></span> </dl> |



 

 
