---
title: Arbeiten mit Sperr Listen
description: Arbeiten mit Sperr Listen
ms.assetid: 4463abb5-f48f-484f-b837-512313572c0a
keywords:
- Windows Media-Format-SDK, Sperr Listen
- Advanced Systems Format (ASF), Sperr Listen
- ASF (Advanced Systems Format), Sperr Listen
- Sperr Listen
- Digital Rights Management (DRM), Sperr Listen
- DRM (Digital Rights Management), Sperr Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f4eca82dd82c9225406a85034ff2a6df227fce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516580"
---
# <a name="working-with-revocation-lists"></a><span data-ttu-id="0d2fb-109">Arbeiten mit Sperr Listen</span><span class="sxs-lookup"><span data-stu-id="0d2fb-109">Working with Revocation Lists</span></span>

<span data-ttu-id="0d2fb-110">Um auf Sicherheitsverletzungen zu reagieren und sicherzustellen, dass Player-Anwendungen, die bekanntermaßen beschädigt oder kompromittiert sind, keine geschützten Dateien wiedergeben oder verwenden können, enthält jede ausgegebene Lizenz eine Sperr Liste.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-110">To respond to security breaches and to ensure that player applications known to be broken or compromised cannot play or use protected files, each license that is issued contains a revocation list.</span></span> <span data-ttu-id="0d2fb-111">Eine Sperr Liste enthält die Anwendungs Zertifikate aller Player-Anwendungen, die bekanntermaßen beschädigt oder beschädigt sind.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-111">A revocation list contains the application certificates of all those player applications known to be broken or corrupted.</span></span> <span data-ttu-id="0d2fb-112">Beim Empfang einer neuen Lizenz wird von der DRM-Komponente der Player Anwendung eine Sperr Liste geprüft.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-112">When a new license is received, the DRM component of the player application checks for a revocation list.</span></span> <span data-ttu-id="0d2fb-113">Wenn eine neue gefunden wird, die aktueller als die derzeit auf dem Computer ist, wird die neuere Liste gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-113">If one is found that is newer than the one currently on the computer, the newer list is stored.</span></span> <span data-ttu-id="0d2fb-114">Wenn der Consumer das nächste Mal eine geschützte ASF-Datei abspielt, vergleicht die DRM-Komponente die Player Anwendung mit der Sperr Liste.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-114">The next time the consumer plays a protected ASF file, the DRM component compares the player application to the revocation list.</span></span> <span data-ttu-id="0d2fb-115">Wenn die Player Anwendung widerrufen wird, sendet die DRM-Komponente eine Fehlermeldung an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-115">If the player application is revoked, the DRM component sends an error message to the application.</span></span>

<span data-ttu-id="0d2fb-116">Spieler Anwendungen können in den folgenden Szenarien eine Sperr Fehlermeldung erhalten:</span><span class="sxs-lookup"><span data-stu-id="0d2fb-116">Player applications can receive a revocation error message in the following scenarios:</span></span>

-   <span data-ttu-id="0d2fb-117">Die Fehlermeldung wird empfangen, nachdem die Anwendung die [**iwmdrmreader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) -Methode für eine geschützte Datei aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-117">The error message is received after the application calls the [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) method for a protected file.</span></span> <span data-ttu-id="0d2fb-118">Der-Befehl schlägt fehl, wenn der **HRESULT** -Code NS \_ E \_ DRM \_ appcert \_ widerrufen wurde, der für die **OnStatus** -Rückruffunktion mit dem WMT-Abruf \_ Lizenzstatus bereitgestellt wird \_ .</span><span class="sxs-lookup"><span data-stu-id="0d2fb-118">The call fails with the **HRESULT** code NS\_E\_DRM\_APPCERT\_REVOKED, which is supplied to the **OnStatus** callback function with WMT\_ACQUIRE\_LICENSE status.</span></span> <span data-ttu-id="0d2fb-119">Wenn dieser **HRESULT** -Code ignoriert wird, treten Fehler weiterhin auf.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-119">If this **HRESULT** code is ignored, errors will continue to occur.</span></span>
-   <span data-ttu-id="0d2fb-120">Die Fehlermeldung wird empfangen, wenn die Anwendung den DRM-fähigen Reader erstellt und die [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) -Methode für eine geschützte Datei aufruft.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-120">The error message is received when the application creates the DRM-enabled reader and calls the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method for a protected file.</span></span> <span data-ttu-id="0d2fb-121">Der-Befehl schlägt fehl, wenn der **HRESULT** -Code NS \_ E \_ DRM \_ appcert \_ widerrufen wurde, der für die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode mit dem geöffneten WMT-Status bereitgestellt wird \_ .</span><span class="sxs-lookup"><span data-stu-id="0d2fb-121">The call fails with the **HRESULT** code NS\_E\_DRM\_APPCERT\_REVOKED, which is supplied to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method with WMT\_OPENED status.</span></span> <span data-ttu-id="0d2fb-122">Wenn eine Player Anwendung diese Fehlermeldung empfängt, sollte Sie von der Anwendung benachrichtigt und eine Möglichkeit zum Wiederherstellen der Funktionalität für Ihren Player bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-122">When a player application receives this error message, the application should notify end users and provide a way for them to restore functionality to their player.</span></span> <span data-ttu-id="0d2fb-123">Die Anwendung kann z. b. eine URL öffnen, in der Endbenutzer ein Upgrade für die kompromittierte Anwendung herunterladen können.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-123">For example, the application can open a URL where end users can download an upgrade for the compromised application.</span></span>

<span data-ttu-id="0d2fb-124">**Hinweis** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-124">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d2fb-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d2fb-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d2fb-126">**Features digitaler Rights Management**</span><span class="sxs-lookup"><span data-stu-id="0d2fb-126">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="0d2fb-127">**Behandeln von Lizenz Erwerbs Ereignissen**</span><span class="sxs-lookup"><span data-stu-id="0d2fb-127">**Handling License Acquisition Events**</span></span>](handling-license-acquisition-events.md)
</dt> </dl>

 

 




