---
title: Rückruf Funktionen für Client Anwendungen
description: Zwei Arten von Rückruf Signaturen.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371edd162c4cbd1332764c7b3e9e70bf114270e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388610"
---
# <a name="client-application-callback-functions"></a><span data-ttu-id="4f2db-103">Rückruf Funktionen für Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="4f2db-103">Client Application Callback Functions</span></span>

<span data-ttu-id="4f2db-104">Der Windows-Biometrieframework unterstützt zwei Arten von Rückruf Signaturen.</span><span class="sxs-lookup"><span data-stu-id="4f2db-104">The Windows Biometric Framework supports two types of callback signatures.</span></span> <span data-ttu-id="4f2db-105">Ab Windows 8 wird der folgende Rückruf unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f2db-105">Beginning with Windows 8, the following callback is supported.</span></span> <span data-ttu-id="4f2db-106">Es wird empfohlen, dass Sie diesen Rückruf für alle neuen Anwendungen implementieren.</span><span class="sxs-lookup"><span data-stu-id="4f2db-106">We recommend that you implement this callback for all new applications.</span></span> <span data-ttu-id="4f2db-107">Dieser Rückruf kann jedoch in Windows 7 nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f2db-107">This callback cannot, however, be used in Windows 7.</span></span>



| <span data-ttu-id="4f2db-108">Rückruf</span><span class="sxs-lookup"><span data-stu-id="4f2db-108">Callback</span></span>                                                                                     | <span data-ttu-id="4f2db-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f2db-109">Description</span></span>                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f2db-110">**pwinbio \_ Async- \_ Abschluss \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="4f2db-110">**PWINBIO\_ASYNC\_COMPLETION\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | <span data-ttu-id="4f2db-111">Benachrichtigt die Client Anwendung, dass ein asynchroner Vorgang, der mithilfe von [**winbioasyncopensession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) oder [**winbioasyncopenframework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) gestartet wurde, abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="4f2db-111">Notifies the client application that an asynchronous operation started by using [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) or [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) has completed.</span></span><br/> |



 

<span data-ttu-id="4f2db-112">Die folgenden Rückruf Funktionen wurden in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4f2db-112">The following callback functions were introduced in Windows 7.</span></span> <span data-ttu-id="4f2db-113">Es wird empfohlen, Sie nicht für neue Anwendungen zu implementieren, die auf Windows 8 und spätere Betriebssysteme abzielen.</span><span class="sxs-lookup"><span data-stu-id="4f2db-113">We recommend that you do not implement them for new applications that target Windows 8 and later operating systems.</span></span>



| <span data-ttu-id="4f2db-114">Rückruf</span><span class="sxs-lookup"><span data-stu-id="4f2db-114">Callback</span></span>                                                                                 | <span data-ttu-id="4f2db-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f2db-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f2db-116">**pwinbio \_ Capture- \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="4f2db-116">**PWINBIO\_CAPTURE\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | <span data-ttu-id="4f2db-117">Gibt Ergebnisse aus der asynchronen [**winbiocapturesamplewithcallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="4f2db-117">Returns results from the asynchronous [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) function.</span></span><br/> |
| [<span data-ttu-id="4f2db-118">**pwinbio-Registrierungs \_ \_ \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="4f2db-118">**PWINBIO\_ENROLL\_CAPTURE\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | <span data-ttu-id="4f2db-119">Gibt Ergebnisse aus der asynchronen [**winbioregistricapturewithcallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="4f2db-119">Returns results from the asynchronous [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) function.</span></span><br/> |
| [<span data-ttu-id="4f2db-120">**pwinbio- \_ Ereignis \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="4f2db-120">**PWINBIO\_EVENT\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | <span data-ttu-id="4f2db-121">Gibt Ergebnisse aus der asynchronen [**winbioregistereventmonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="4f2db-121">Returns results from the asynchronous [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function.</span></span><br/>           |
| [<span data-ttu-id="4f2db-122">**pwinbio \_ - \_ identifizrückruf**</span><span class="sxs-lookup"><span data-stu-id="4f2db-122">**PWINBIO\_IDENTIFY\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | <span data-ttu-id="4f2db-123">Gibt Ergebnisse aus der asynchronen [**winbioidentifywithcallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="4f2db-123">Returns results from the asynchronous [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) function.</span></span><br/>           |
| [<span data-ttu-id="4f2db-124">**pwinbio-Abruf \_ \_ Sensor \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="4f2db-124">**PWINBIO\_LOCATE\_SENSOR\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | <span data-ttu-id="4f2db-125">Gibt Ergebnisse aus der asynchronen [**winbiolotoresensorwithcallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="4f2db-125">Returns results from the asynchronous [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) function.</span></span><br/>   |
| [<span data-ttu-id="4f2db-126">**pwinbio \_ - \_ prüfrückruf**</span><span class="sxs-lookup"><span data-stu-id="4f2db-126">**PWINBIO\_VERIFY\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | <span data-ttu-id="4f2db-127">Gibt Ergebnisse aus der asynchronen [**winbioverifywithcallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="4f2db-127">Returns results from the asynchronous [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) function.</span></span><br/>               |



 

## <a name="related-topics"></a><span data-ttu-id="4f2db-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4f2db-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f2db-129">Client Anwendungs Referenz</span><span class="sxs-lookup"><span data-stu-id="4f2db-129">Client Application Reference</span></span>](client-application-reference.md)
</dt> </dl>

 

 





