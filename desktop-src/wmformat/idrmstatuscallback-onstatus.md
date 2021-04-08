---
title: Idrmstatuscallback OnStatus-Methode
description: Die OnStatus-Methode empfängt Statusmeldungen von asynchronen DRM-Prozessen.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- OnStatus-Methode Windows Media-Format
- OnStatus-Methode Windows Media-Format, idrmstatuscallback-Schnittstelle
- Idrmstatuscallback-Schnittstelle Windows Media-Format, OnStatus-Methode
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 754d59d74fb0365f423243e92565ac17b46628a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037848"
---
# <a name="idrmstatuscallbackonstatus-method"></a><span data-ttu-id="bb90b-106">Idrmstatuscallback:: OnStatus-Methode</span><span class="sxs-lookup"><span data-stu-id="bb90b-106">IDRMStatusCallback::OnStatus method</span></span>

<span data-ttu-id="bb90b-107">Die **OnStatus** -Methode empfängt Statusmeldungen von asynchronen DRM-Prozessen.</span><span class="sxs-lookup"><span data-stu-id="bb90b-107">The **OnStatus** method receives status messages from asynchronous DRM processes.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb90b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb90b-108">Syntax</span></span>


```C++
HRESULT OnStatus(
  [in] MSDRM_STATUS      Status,
  [in] HRESULT           hr,
  [in] DRM_ATTR_DATATYPE dwType,
  [in] BYTE              *pValue,
  [in] void              *pvContext
);
```



## <a name="parameters"></a><span data-ttu-id="bb90b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb90b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb90b-110">*Status* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb90b-110">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb90b-111">Statuscode.</span><span class="sxs-lookup"><span data-stu-id="bb90b-111">Status code.</span></span> <span data-ttu-id="bb90b-112">Nachrichten Codes werden im Enumerationstyp " **msdrm- \_ Status** " definiert.</span><span class="sxs-lookup"><span data-stu-id="bb90b-112">Message codes are defined in the **MSDRM\_STATUS** enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="bb90b-113">*Personalabteilung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb90b-113">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb90b-114">Rückgabecode, der die Statusmeldung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bb90b-114">Return code that supports the status message.</span></span>

</dd> <dt>

<span data-ttu-id="bb90b-115">*dwType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb90b-115">*dwType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb90b-116">Der Typ der Daten, auf die von *pValue* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="bb90b-116">Type of the data pointed to by *pValue*.</span></span> <span data-ttu-id="bb90b-117">Legen Sie auf einen der Werte der " [**DRM \_ attr \_ DataType**](drm-attr-datatype.md) "-Enumeration fest.</span><span class="sxs-lookup"><span data-stu-id="bb90b-117">Set to one of the values of the [**DRM\_ATTR\_DATATYPE**](drm-attr-datatype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="bb90b-118">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb90b-118">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb90b-119">Zeiger auf Daten, die mit der Statusmeldung verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="bb90b-119">Pointer to data related to the status message.</span></span> <span data-ttu-id="bb90b-120">Der Typ der Daten wird durch den Wert des *dwType* -Parameters bestimmt.</span><span class="sxs-lookup"><span data-stu-id="bb90b-120">The type of data is determined by the value of the *dwType* parameter.</span></span> <span data-ttu-id="bb90b-121">Weitere Informationen finden Sie in der " [**DRM \_ attr \_ DataType**](drm-attr-datatype.md) "-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="bb90b-121">For more information, see the [**DRM\_ATTR\_DATATYPE**](drm-attr-datatype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="bb90b-122">*pvcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb90b-122">*pvContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb90b-123">Optionaler Parameter, der verwendet werden kann, um das Objekt zu identifizieren, das die Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="bb90b-123">Optional parameter that can be used to identify the object that sent the message.</span></span> <span data-ttu-id="bb90b-124">Wenn Sie *pvcontext* festlegen, wenn Sie diesen Rückruf registrieren, können Sie denselben Rückruf verwenden, um mehrere asynchrone Prozesse zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="bb90b-124">By setting *pvContext* when you register this callback, you can use the same callback to handle multiple asynchronous processes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb90b-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb90b-125">Return value</span></span>

<span data-ttu-id="bb90b-126">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="bb90b-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bb90b-127">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="bb90b-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bb90b-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bb90b-128">Return code</span></span>                                                                          | <span data-ttu-id="bb90b-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb90b-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bb90b-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb90b-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bb90b-131">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb90b-131">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bb90b-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb90b-132">Remarks</span></span>

<span data-ttu-id="bb90b-133">Keine.</span><span class="sxs-lookup"><span data-stu-id="bb90b-133">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb90b-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bb90b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb90b-135">**DRM- \_ attr- \_ Datentyp**</span><span class="sxs-lookup"><span data-stu-id="bb90b-135">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)
</dt> <dt>

[<span data-ttu-id="bb90b-136">**Idrmstatus Callback-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="bb90b-136">**IDRMStatusCallback Interface**</span></span>](idrmstatuscallback.md)
</dt> </dl>

 

 





