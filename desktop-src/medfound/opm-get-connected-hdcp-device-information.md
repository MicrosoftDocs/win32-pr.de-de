---
description: 'Weitere Informationen finden Sie hier: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561a348588b1244a6763eb447affa2b330e9c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527884"
---
# <a name="opm_get_connected_hdcp_device_information"></a><span data-ttu-id="c2566-103">OPM \_ get \_ Connected \_ HDCP- \_ Geräte \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="c2566-103">OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION</span></span>

<span data-ttu-id="c2566-104">Ruft Informationen zu einem HDCP-Gerät (High-Bandwidth Digital Content Protection) ab, das an die Videoausgabe angehängt ist.</span><span class="sxs-lookup"><span data-stu-id="c2566-104">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="c2566-105">Die folgenden Informationen werden zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="c2566-105">The following information is returned:</span></span>

-   <span data-ttu-id="c2566-106">Der HDCP Key Selection Vector (KSV) des Geräts.</span><span class="sxs-lookup"><span data-stu-id="c2566-106">The device's HDCP key selection vector (KSV).</span></span>
-   <span data-ttu-id="c2566-107">Gibt an, ob das Gerät ein HDCP-Repeater ist.</span><span class="sxs-lookup"><span data-stu-id="c2566-107">Whether the device is an HDCP repeater.</span></span>



| <span data-ttu-id="c2566-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2566-108">Requirement</span></span> | <span data-ttu-id="c2566-109">Wert</span><span class="sxs-lookup"><span data-stu-id="c2566-109">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2566-110">Anforderungs-GUID</span><span class="sxs-lookup"><span data-stu-id="c2566-110">Request GUID</span></span> | <span data-ttu-id="c2566-111">OPM \_ get \_ Connected \_ HDCP- \_ Geräte \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="c2566-111">OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION</span></span>                                                          |
| <span data-ttu-id="c2566-112">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="c2566-112">Input data</span></span>   | <span data-ttu-id="c2566-113">Keine</span><span class="sxs-lookup"><span data-stu-id="c2566-113">None</span></span>                                                                                                    |
| <span data-ttu-id="c2566-114">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="c2566-114">Return data</span></span>  | <span data-ttu-id="c2566-115">Eine [**mit OPM \_ verbundene \_ HDCP- \_ Geräte \_ Informations**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) Struktur</span><span class="sxs-lookup"><span data-stu-id="c2566-115">An [**OPM\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c2566-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2566-116">Remarks</span></span>

<span data-ttu-id="c2566-117">Diese Abfrage kann nur mit dem *COPP-Emulations Modus* verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2566-117">This query can be used only with *COPP emulation mode*.</span></span> <span data-ttu-id="c2566-118">Wenn die [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Schnittstelle eine OPM-Semantik (Output Protection Manager) verwendet, wird diese Status Anforderung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2566-118">If the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface uses Output Protection Manager (OPM) semantics, this status request is not supported.</span></span>

<span data-ttu-id="c2566-119">Der KSV ist ein Bezeichner, der dem Gerätehersteller zur Verfügung gestellt wird und im HDCP-Authentifizierungs-und-Setup Prozess verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2566-119">The KSV is an identifier provided to the device manufacturer, and is used in the HDCP authentication and setup process.</span></span> <span data-ttu-id="c2566-120">Im COPP-Emulations Modus verwendet die Anwendung den KSV, um zu bestimmen, ob das HDCP-Gerät gesperrt wird.</span><span class="sxs-lookup"><span data-stu-id="c2566-120">In COPP emulation mode, the application uses the KSV to determine whether the HDCP device is revoked.</span></span> <span data-ttu-id="c2566-121">Wenn dies der Fall ist, sollte die Anwendung geschützte Inhalte nicht wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="c2566-121">If it is, the application should not play protected content.</span></span> <span data-ttu-id="c2566-122">Außerdem sollte die Anwendung geschützte Inhalte nicht wiedergeben, wenn es sich bei dem Gerät um einen HDCP-Repeater handelt, da COPP HDCP-Repeaters nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2566-122">Also, the application should not play protected content if the device is an HDCP repeater, because COPP does not support HDCP repeaters.</span></span>

<span data-ttu-id="c2566-123">Diese Abfrage wird bei Verwendung der OPM-Semantik nicht benötigt, da OPM die Geräte Sperrung und HDCP-Repeater unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2566-123">This query is not needed when OPM semantics are used, because OPM supports device revocation and HDCP repeaters.</span></span>

<span data-ttu-id="c2566-124">Diese Abfrage entspricht der DXVA- \_ Abfrage "coppqueryhdcpkeydata", die im Certified Output Protection Protocol (COPP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2566-124">This query is equivalent to the DXVA\_COPPQueryHDCPKeyData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2566-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2566-125">Requirements</span></span>



| <span data-ttu-id="c2566-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2566-126">Requirement</span></span> | <span data-ttu-id="c2566-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c2566-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c2566-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2566-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c2566-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2566-129">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c2566-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2566-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c2566-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2566-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c2566-132">Header</span><span class="sxs-lookup"><span data-stu-id="c2566-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2566-133"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2566-133"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2566-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2566-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2566-135">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="c2566-135">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="c2566-136">OPM-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2566-136">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




