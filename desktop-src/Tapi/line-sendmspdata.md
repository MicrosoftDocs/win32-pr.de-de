---
description: Die TSPI-Zeilen- \_ sendmspdata-Nachricht wird gesendet, wenn der Telefoniedienstanbieter (TSP) Informationen an den Media Service Provider (MSP) übergeben möchte.
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: LINE_SENDMSPDATA Meldung (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce46664be0bc7f312af8b45cc5e06e13a7d91488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357617"
---
# <a name="line_sendmspdata-message"></a><span data-ttu-id="89aaf-103">Zeile \_ sendmspdata-Nachricht</span><span class="sxs-lookup"><span data-stu-id="89aaf-103">LINE\_SENDMSPDATA message</span></span>

<span data-ttu-id="89aaf-104">Die TSPI- **Zeilen- \_ sendmspdata** -Nachricht wird gesendet, wenn der Telefoniedienstanbieter (TSP) Informationen an den Media Service Provider (MSP) übergeben möchte.</span><span class="sxs-lookup"><span data-stu-id="89aaf-104">The TSPI **LINE\_SENDMSPDATA** message is sent when the telephony service provider (TSP) wants to pass information to the media service provider (MSP).</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="89aaf-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="89aaf-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89aaf-106">*htline*</span><span class="sxs-lookup"><span data-stu-id="89aaf-106">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="89aaf-107">Der TAPI-Handle für die Zeile.</span><span class="sxs-lookup"><span data-stu-id="89aaf-107">The TAPI handle for the line.</span></span>

</dd> <dt>

<span data-ttu-id="89aaf-108">*"htcall"*</span><span class="sxs-lookup"><span data-stu-id="89aaf-108">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="89aaf-109">Der TAPI-Handle für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="89aaf-109">The TAPI handle for the call.</span></span>

</dd> <dt>

<span data-ttu-id="89aaf-110">*dwmsg*</span><span class="sxs-lookup"><span data-stu-id="89aaf-110">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="89aaf-111">Die Wert Zeile \_ sendmspdata.</span><span class="sxs-lookup"><span data-stu-id="89aaf-111">The value LINE\_SENDMSPDATA.</span></span>

</dd> <dt>

<span data-ttu-id="89aaf-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="89aaf-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="89aaf-113">Identifiziert den MSP, der die Nachricht empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="89aaf-113">Identifies the MSP that should receive the message.</span></span> <span data-ttu-id="89aaf-114">Wenn der Wert 0 ist, wird die Nachricht an alle MSPs gesendet.</span><span class="sxs-lookup"><span data-stu-id="89aaf-114">If 0, the message will be sent to all MSPs.</span></span> <span data-ttu-id="89aaf-115">Dabei handelt es sich um das Handle, das an die Funktion [**TSPI \_ linecreatemspinstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="89aaf-115">This is the handle that is passed to the [**TSPI\_LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) function.</span></span>

</dd> <dt>

<span data-ttu-id="89aaf-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="89aaf-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="89aaf-117">Der Puffer, der an das MSP übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="89aaf-117">The buffer to pass to the MSP.</span></span> <span data-ttu-id="89aaf-118">Der Puffer wird nicht von TAPI interpretiert.</span><span class="sxs-lookup"><span data-stu-id="89aaf-118">The buffer is not interpreted by TAPI.</span></span>

</dd> <dt>

<span data-ttu-id="89aaf-119">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="89aaf-119">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="89aaf-120">Die Größe (in Bytes) des Puffers in *dwParam2*.</span><span class="sxs-lookup"><span data-stu-id="89aaf-120">The size, in bytes, of the buffer in *dwParam2*.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89aaf-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89aaf-121">Remarks</span></span>

<span data-ttu-id="89aaf-122">Der Dienstanbieter muss eine TAPI-Version 3,0 oder höher aushandeln, damit diese Nachricht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="89aaf-122">The service provider must negotiate a TAPI version 3.0 or later for this message to operate.</span></span>

## <a name="requirements"></a><span data-ttu-id="89aaf-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89aaf-123">Requirements</span></span>



| <span data-ttu-id="89aaf-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89aaf-124">Requirement</span></span> | <span data-ttu-id="89aaf-125">Wert</span><span class="sxs-lookup"><span data-stu-id="89aaf-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="89aaf-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="89aaf-126">TAPI version</span></span><br/> | <span data-ttu-id="89aaf-127">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="89aaf-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="89aaf-128">Header</span><span class="sxs-lookup"><span data-stu-id="89aaf-128">Header</span></span><br/>       | <dl> <span data-ttu-id="89aaf-129"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="89aaf-129"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89aaf-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89aaf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89aaf-131">Informationen zum Media Service Provider (MSP)</span><span class="sxs-lookup"><span data-stu-id="89aaf-131">About The Media Service Provider (MSP)</span></span>](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[<span data-ttu-id="89aaf-132">**TSPI \_ linemspidentify**</span><span class="sxs-lookup"><span data-stu-id="89aaf-132">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[<span data-ttu-id="89aaf-133">**TSPI \_ linecreatemspinstance**</span><span class="sxs-lookup"><span data-stu-id="89aaf-133">**TSPI\_LineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[<span data-ttu-id="89aaf-134">**TSPI \_ lineclosemspinstance**</span><span class="sxs-lookup"><span data-stu-id="89aaf-134">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[<span data-ttu-id="89aaf-135">**TSPI \_ linerecievemspdata**</span><span class="sxs-lookup"><span data-stu-id="89aaf-135">**TSPI\_lineRecieveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[<span data-ttu-id="89aaf-136">**Linedevcaps**</span><span class="sxs-lookup"><span data-stu-id="89aaf-136">**LINEDEVCAPS**</span></span>](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

