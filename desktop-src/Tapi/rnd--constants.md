---
description: Die folgenden Konstanten können als Fehler zurückgegeben werden.
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: RND_ Konstanten (rnderr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a89b6747fb9fef775bbf40fac472081567ff1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356447"
---
# <a name="rnd_-constants"></a><span data-ttu-id="baff9-103">Rnd- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="baff9-103">RND\_ Constants</span></span>

<span data-ttu-id="baff9-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="baff9-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="baff9-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="baff9-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="baff9-106">Die folgenden Konstanten können als Fehler zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="baff9-106">The following constants may be returned as errors.</span></span>

<dl> <dt>

<span data-ttu-id="baff9-107"><span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**Rnd \_ ungültige \_ Zeit**</span><span class="sxs-lookup"><span data-stu-id="baff9-107"><span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**RND\_INVALID\_TIME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="baff9-108">0xe0000200</span><span class="sxs-lookup"><span data-stu-id="baff9-108">0xe0000200</span></span>
</dt> <dt>



<span data-ttu-id="baff9-109">Der eingegebene Zeitwert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="baff9-109">The time value entered is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baff9-110"><span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**Rnd- \_ NULL- \_ Server \_ Name**</span><span class="sxs-lookup"><span data-stu-id="baff9-110"><span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**RND\_NULL\_SERVER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="baff9-111">0xe0000201</span><span class="sxs-lookup"><span data-stu-id="baff9-111">0xe0000201</span></span>
</dt> <dt>



<span data-ttu-id="baff9-112">Der Servername ist **null**, wahrscheinlich weil [**itconferenceblob:: init**](itconferenceblob-init.md) nicht ausgeführt wurde oder nicht erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="baff9-112">The server name is **NULL**, probably because [**ITConferenceBlob::Init**](itconferenceblob-init.md) has not been run or did not succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baff9-113"><span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**Rnd ist \_ bereits \_ verbunden.**</span><span class="sxs-lookup"><span data-stu-id="baff9-113"><span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="baff9-114">0xe0000202</span><span class="sxs-lookup"><span data-stu-id="baff9-114">0xe0000202</span></span>
</dt> <dt>



<span data-ttu-id="baff9-115">Die [**itdirectory:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) -Methode wurde aufgerufen, aber es ist bereits eine Verbindung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="baff9-115">The [**ITDirectory::Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) method was called, but a connection already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="baff9-116"><span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**Rnd ist \_ nicht \_ verbunden.**</span><span class="sxs-lookup"><span data-stu-id="baff9-116"><span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="baff9-117">0xe0000203</span><span class="sxs-lookup"><span data-stu-id="baff9-117">0xe0000203</span></span>
</dt> <dt>



<span data-ttu-id="baff9-118">Die [**itdirectory:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) -Methode wurde nicht aufgerufen oder ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="baff9-118">The [**ITDirectory::Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) method has not been called, or failed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="baff9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="baff9-119">Requirements</span></span>



| <span data-ttu-id="baff9-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="baff9-120">Requirement</span></span> | <span data-ttu-id="baff9-121">Wert</span><span class="sxs-lookup"><span data-stu-id="baff9-121">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="baff9-122">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="baff9-122">TAPI version</span></span><br/> | <span data-ttu-id="baff9-123">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="baff9-123">Requires TAPI 3.0 or later</span></span><br/>                                               |
| <span data-ttu-id="baff9-124">Header</span><span class="sxs-lookup"><span data-stu-id="baff9-124">Header</span></span><br/>       | <dl> <span data-ttu-id="baff9-125"><dt>Rnderr. h</dt></span><span class="sxs-lookup"><span data-stu-id="baff9-125"><dt>Rnderr.h</dt></span></span> </dl> |



 

 




