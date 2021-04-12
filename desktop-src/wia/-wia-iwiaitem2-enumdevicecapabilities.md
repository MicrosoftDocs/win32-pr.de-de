---
description: Erstellt einen Enumerator, der verwendet wird, um die Befehle und Ereignisse zu ermitteln, die ein Windows-Abbild Erfassungsgerät (WIA) 2,0 unterstützt.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: 'IWiaItem2:: enumdevicecapabili-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumDeviceCapabilities
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3e771aa636b42d9cd7e4024a1684ebe3edf02eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526468"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a><span data-ttu-id="26130-103">IWiaItem2:: enumdevicecapabili-Methode</span><span class="sxs-lookup"><span data-stu-id="26130-103">IWiaItem2::EnumDeviceCapabilities method</span></span>

<span data-ttu-id="26130-104">Erstellt einen Enumerator, der verwendet wird, um die Befehle und Ereignisse zu ermitteln, die ein Windows-Abbild Erfassungsgerät (WIA) 2,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="26130-104">Creates an enumerator that is used to ascertain the commands and events a Windows Image Acquisition (WIA) 2.0 device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="26130-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="26130-105">Syntax</span></span>


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a><span data-ttu-id="26130-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="26130-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26130-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26130-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26130-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="26130-108">Type: **LONG**</span></span>

<span data-ttu-id="26130-109">Gibt ein Flag an, das den Typ der aufzuzählenden Funktionen auswählt.</span><span class="sxs-lookup"><span data-stu-id="26130-109">Specifies a flag that selects the type of capabilities to enumerate.</span></span> <span data-ttu-id="26130-110">Es handelt sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="26130-110">It is one of the following values.</span></span>

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span data-ttu-id="26130-111"><span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**WIA- \_ Geräte \_ Befehle**</span><span class="sxs-lookup"><span data-stu-id="26130-111"><span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**WIA\_DEVICE\_COMMANDS**</span></span>


</dt> <dd>

<span data-ttu-id="26130-112">Listet Geräte Befehle auf.</span><span class="sxs-lookup"><span data-stu-id="26130-112">Enumerate device commands.</span></span>

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span data-ttu-id="26130-113"><span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**WIA- \_ Geräte \_ Ereignisse**</span><span class="sxs-lookup"><span data-stu-id="26130-113"><span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**WIA\_DEVICE\_EVENTS**</span></span>


</dt> <dd>

<span data-ttu-id="26130-114">Listet Geräte Ereignisse auf.</span><span class="sxs-lookup"><span data-stu-id="26130-114">Enumerate device events.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="26130-115">*ppienumwia \_ DEV \_* - \[ out\]</span><span class="sxs-lookup"><span data-stu-id="26130-115">*ppIEnumWIA\_DEV\_CAPS* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26130-116">Typ: **[ **ienumwia \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span><span class="sxs-lookup"><span data-stu-id="26130-116">Type: **[**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span></span>

<span data-ttu-id="26130-117">Empfängt einen Zeiger auf die [**ienumwia \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) -Schnittstelle, die von dieser Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="26130-117">Receives a pointer to the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface created by this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26130-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26130-118">Return value</span></span>

<span data-ttu-id="26130-119">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="26130-119">Type: **HRESULT**</span></span>

<span data-ttu-id="26130-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="26130-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26130-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="26130-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="26130-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26130-122">Remarks</span></span>

<span data-ttu-id="26130-123">Diese Methode wird verwendet, um ein Enumeratorobjekt zum Abrufen der Befehle und Ereignisse zu erstellen, die von einem WIA 2,0-Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="26130-123">This method is used to create an enumerator object to obtain the set of commands and events that a WIA 2.0 device supports.</span></span> <span data-ttu-id="26130-124">Der *lFlags* -Parameter wird verwendet, um anzugeben, welche Arten von Gerätefunktionen aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="26130-124">The *lFlags* parameter is used to specify which kinds of device capabilities to enumerate.</span></span> <span data-ttu-id="26130-125">Die **IWiaItem2:: enumdevicecapabili-** Methode speichert die Adresse der Schnittstelle des Enumeratorobjekts im *ppienumwia \_ dev \_ Caps* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="26130-125">The **IWiaItem2::EnumDeviceCapabilities** method stores the address of the interface of the enumerator object in the *ppIEnumWIA\_DEV\_CAPS* parameter.</span></span>

<span data-ttu-id="26130-126">Diese Methode kann nur für das Stamm Element von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten einer Gerätestruktur aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="26130-126">This method can only be called on the root item of [**IWiaItem2**](-wia-iwiaitem2.md) objects of a device tree.</span></span>

<span data-ttu-id="26130-127">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppienumwia \_ dev \_ Caps* -Parameter erhalten.</span><span class="sxs-lookup"><span data-stu-id="26130-127">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnumWIA\_DEV\_CAPS* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="26130-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26130-128">Requirements</span></span>



| <span data-ttu-id="26130-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26130-129">Requirement</span></span> | <span data-ttu-id="26130-130">Wert</span><span class="sxs-lookup"><span data-stu-id="26130-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26130-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26130-131">Minimum supported client</span></span><br/> | <span data-ttu-id="26130-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26130-132">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="26130-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26130-133">Minimum supported server</span></span><br/> | <span data-ttu-id="26130-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26130-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="26130-135">Header</span><span class="sxs-lookup"><span data-stu-id="26130-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="26130-136"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="26130-136"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="26130-137">IDL</span><span class="sxs-lookup"><span data-stu-id="26130-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26130-138"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="26130-138"><dt>Wia.idl</dt></span></span> </dl> |



 

 
