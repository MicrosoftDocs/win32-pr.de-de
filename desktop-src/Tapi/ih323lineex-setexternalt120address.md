---
description: Die SetExternalT120Address-Methode wird von einer Anwendung aufgerufen, um eine externe T. 120-Adresse für den Datenaustausch zu konfigurieren.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: 'IH323LineEx:: SetExternalT120Address-Methode (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09756aaf77ba36497b3059f7e93829d7d6a57b42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357593"
---
# <a name="ih323lineexsetexternalt120address-method"></a><span data-ttu-id="9d0b2-103">IH323LineEx:: SetExternalT120Address-Methode</span><span class="sxs-lookup"><span data-stu-id="9d0b2-103">IH323LineEx::SetExternalT120Address method</span></span>

<span data-ttu-id="9d0b2-104">\[**SetExternalT120Address** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-104">\[**SetExternalT120Address** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9d0b2-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9d0b2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9d0b2-106">Die **SetExternalT120Address** -Methode wird von einer Anwendung aufgerufen, um eine externe T. 120-Adresse für den Datenaustausch zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-106">The **SetExternalT120Address** method is called by an application to configure an external T.120 address for data exchange.</span></span> <span data-ttu-id="9d0b2-107">Die Funktion "t. 120" wird während der H. 245-Aushandlung angekündigt, und die Adresse wird in der Bestätigung des Open Logic-Kanals verwendet, sodass der andere Endpunkt T. 120-Sitzungen einrichten kann, in denen der Dienst diese Adresse überwacht.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-107">T.120 capability will be advertised during the H.245 negotiation, and the address will be used in the open logic channel acknowledgement so that the other endpoint can set up T.120 sessions with the service listening on that address.</span></span> <span data-ttu-id="9d0b2-108">Wenn diese Funktion nicht aufgerufen wird, kündigt der Dienstanbieter H. 323 keine T. 120-Funktion an.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-108">If this function is not called, the H.323 service provider will not advertise T.120 capability.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d0b2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d0b2-109">Syntax</span></span>


```C++
HRESULT SetExternalT120Address(
  [in] BOOL  fEnable,
  [in] DWORD dwIP,
  [in] WORD  wPort
);
```



## <a name="parameters"></a><span data-ttu-id="9d0b2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d0b2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d0b2-111">*fenckbar* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d0b2-111">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d0b2-112">**True** , um T. 120-Funktion zu aktivieren; **False** , um die T. 120-Funktion zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-112">**TRUE** to enable T.120 capability; **FALSE** to disable T.120 capability.</span></span>

</dd> <dt>

<span data-ttu-id="9d0b2-113">*dwip* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d0b2-113">*dwIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d0b2-114">**DWORD** mit der IP-Adresse in der Host-Byte Reihenfolge des externen T. 120-Diensts.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-114">**DWORD** containing the IP address in host byte order of the external T.120 service.</span></span>

</dd> <dt>

<span data-ttu-id="9d0b2-115">*wport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d0b2-115">*wPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d0b2-116">**Word** , das den Port des externen T. 120-dienstangs enthält.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-116">**WORD** containing the port of the external T.120 service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d0b2-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d0b2-117">Return value</span></span>

<span data-ttu-id="9d0b2-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-118">This method can return one of these values.</span></span>



| <span data-ttu-id="9d0b2-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9d0b2-119">Return code</span></span>                                                                          | <span data-ttu-id="9d0b2-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d0b2-120">Description</span></span>                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="9d0b2-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9d0b2-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9d0b2-122">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-122">Method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9d0b2-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d0b2-123">Requirements</span></span>



| <span data-ttu-id="9d0b2-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d0b2-124">Requirement</span></span> | <span data-ttu-id="9d0b2-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9d0b2-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d0b2-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="9d0b2-126">TAPI version</span></span><br/> | <span data-ttu-id="9d0b2-127">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="9d0b2-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9d0b2-128">Header</span><span class="sxs-lookup"><span data-stu-id="9d0b2-128">Header</span></span><br/>       | <dl> <span data-ttu-id="9d0b2-129"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d0b2-129"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="9d0b2-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d0b2-130">Library</span></span><br/>      | <dl> <span data-ttu-id="9d0b2-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d0b2-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9d0b2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9d0b2-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="9d0b2-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d0b2-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




