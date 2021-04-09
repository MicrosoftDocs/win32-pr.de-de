---
description: 'Die IWiaItem2:: enumregistereventinfo-Methode erstellt einen Enumerator, mit dem Sie Informationen zu Ereignissen abrufen können, für die eine Anwendung registriert ist.'
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: 'IWiaItem2:: enumregistereventinfo-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumRegisterEventInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b5899b629267f74724129aeae3f66801953d8cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129428"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a><span data-ttu-id="5df8c-103">IWiaItem2:: enumregistereventinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="5df8c-103">IWiaItem2::EnumRegisterEventInfo method</span></span>

<span data-ttu-id="5df8c-104">Die **IWiaItem2:: enumregistereventinfo** -Methode erstellt einen Enumerator, mit dem Sie Informationen zu Ereignissen abrufen können, für die eine Anwendung registriert ist.</span><span class="sxs-lookup"><span data-stu-id="5df8c-104">The **IWiaItem2::EnumRegisterEventInfo** method creates an enumerator that you can use to obtain information about events for which an application is registered.</span></span>

## <a name="syntax"></a><span data-ttu-id="5df8c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5df8c-105">Syntax</span></span>


```C++
HRESULT EnumRegisterEventInfo(
  [in]        LONG              lFlags,
  [in]  const GUID              *pEventGUID,
  [out]       IEnumWIA_DEV_CAPS **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="5df8c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5df8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5df8c-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5df8c-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5df8c-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="5df8c-108">Type: **LONG**</span></span>

<span data-ttu-id="5df8c-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5df8c-109">Not used.</span></span> <span data-ttu-id="5df8c-110">Auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="5df8c-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="5df8c-111">" *Peer-GUID* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="5df8c-111">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5df8c-112">Geben Sie Folgendes ein: \* Konstante *GUID \** _</span><span class="sxs-lookup"><span data-stu-id="5df8c-112">Type: \**const GUID\** _</span></span>

<span data-ttu-id="5df8c-113">Ein Zeiger auf einen Bezeichner, der das Hardware Ereignis angibt, für das Sie Registrierungsinformationen abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="5df8c-113">Pointer to an identifier that specifies the hardware event for which you want to obtain registration information.</span></span>

</dd> <dt>

<span data-ttu-id="5df8c-114">_ppIEnum \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5df8c-114">_ppIEnum\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5df8c-115">Typ: **[ **ienumwia \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span><span class="sxs-lookup"><span data-stu-id="5df8c-115">Type: **[**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span></span>

<span data-ttu-id="5df8c-116">Die Adresse eines Zeigers auf die [**ienumwia \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5df8c-116">The address of a pointer to the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5df8c-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5df8c-117">Return value</span></span>

<span data-ttu-id="5df8c-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5df8c-118">Type: **HRESULT**</span></span>

<span data-ttu-id="5df8c-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5df8c-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5df8c-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5df8c-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5df8c-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5df8c-121">Remarks</span></span>

<span data-ttu-id="5df8c-122">Eine Anwendung ruft diese Methode auf, um ein Enumeratorobjekt für die Ereignis Informationen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5df8c-122">An application calls this method to create an enumerator object for the event information.</span></span> <span data-ttu-id="5df8c-123">**IWiaItem2:: enumregistereventinfo** speichert die Adresse der [**ienumwia \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) -Schnittstelle des Enumeratorobjekts im *ppienum* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="5df8c-123">**IWiaItem2::EnumRegisterEventInfo** stores the address of the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface of the enumerator object in the *ppIEnum* parameter.</span></span> <span data-ttu-id="5df8c-124">Das Programm verwendet dann den Schnittstellen Zeiger, um die Eigenschaften des Ereignisses aufzulisten, für das es registriert ist.</span><span class="sxs-lookup"><span data-stu-id="5df8c-124">The program then uses the interface pointer to enumerate the properties of the event for which it is registered.</span></span>

<span data-ttu-id="5df8c-125">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppienum* -Parameter empfangen.</span><span class="sxs-lookup"><span data-stu-id="5df8c-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers that they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5df8c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5df8c-126">Requirements</span></span>



| <span data-ttu-id="5df8c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5df8c-127">Requirement</span></span> | <span data-ttu-id="5df8c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="5df8c-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5df8c-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5df8c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5df8c-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5df8c-130">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5df8c-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5df8c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5df8c-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5df8c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5df8c-133">Header</span><span class="sxs-lookup"><span data-stu-id="5df8c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5df8c-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5df8c-134"><dt>Wia.h</dt></span></span> </dl> |



 

 
