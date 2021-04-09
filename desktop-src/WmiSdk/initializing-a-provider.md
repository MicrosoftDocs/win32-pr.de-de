---
description: Eine der ersten Aufgaben, die Sie für einen-Anbieter programmieren müssen, ist der Initialisierungs Prozess, der alle Aufgaben abdeckt, die der Anbieter ausführen muss, sodass er Informationen von WMI senden und empfangen, ein verwaltetes Objekt Steuern und andere Aufgaben ausführen kann.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Initialisieren eines Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14a724d72d5e5c58eff30f2fa61da64d77a493f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868751"
---
# <a name="initializing-a-provider"></a><span data-ttu-id="cde1c-103">Initialisieren eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="cde1c-103">Initializing a Provider</span></span>

<span data-ttu-id="cde1c-104">Eine der ersten Aufgaben, die Sie für einen-Anbieter programmieren müssen, ist der Initialisierungs Prozess, der alle Aufgaben abdeckt, die der Anbieter ausführen muss, sodass er Informationen von WMI senden und empfangen, ein verwaltetes Objekt Steuern und andere Aufgaben ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="cde1c-104">One of the first tasks you must code for a provider is the initialization process, which covers any tasks your provider must perform that allows it to send and receive information from WMI, control a managed object, and perform other tasks.</span></span> <span data-ttu-id="cde1c-105">Jeder Anbietertyp verfügt über einen anderen Satz von Aufgaben, den er ausführen muss und über einen begleitenden Satz eindeutiger Schnittstellen verfügt.</span><span class="sxs-lookup"><span data-stu-id="cde1c-105">Each type of provider has a different set of tasks that it must perform and has an accompanying set of unique interfaces.</span></span>

<span data-ttu-id="cde1c-106">Allerdings initialisieren alle Anbieter über die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle und informieren WMI über die [**iwbemproviderinitsink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) -Schnittstelle über Ihren Initialisierungs Status.</span><span class="sxs-lookup"><span data-stu-id="cde1c-106">However, all providers initialize through the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, and inform WMI of their initialization status through the [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) interface.</span></span>

<span data-ttu-id="cde1c-107">Im folgenden Verfahren wird beschrieben, wie ein Anbieter initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="cde1c-107">The following procedure describes how to initialize a provider.</span></span>

<span data-ttu-id="cde1c-108">**So initialisieren Sie einen Anbieter**</span><span class="sxs-lookup"><span data-stu-id="cde1c-108">**To initialize a provider**</span></span>

1.  <span data-ttu-id="cde1c-109">Implementieren Sie [**iwbemproviderinit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) für Ihren Anbieter.</span><span class="sxs-lookup"><span data-stu-id="cde1c-109">Implement [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) for your provider.</span></span>

    <span data-ttu-id="cde1c-110">Wenn WMI ermittelt, dass ein Client die Dienste eines Anbieters erfordert, lädt WMI den Anbieter durch Aufrufen der Methode [**iwbemproviderinit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) .</span><span class="sxs-lookup"><span data-stu-id="cde1c-110">When WMI determines that a client requires the services of a provider, WMI loads the provider by calling the [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) method.</span></span>

2.  <span data-ttu-id="cde1c-111">Implementieren Sie alle Schnittstellen, die für Ihren Anbietertyp eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="cde1c-111">Implement any interfaces unique to your type of provider.</span></span>
3.  <span data-ttu-id="cde1c-112">Informieren Sie WMI, dass Ihr Anbieter die Initialisierung abgeschlossen hat, indem Sie [**iwbemproviderinitsink:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cde1c-112">Inform WMI that your provider is finished with initialization by calling [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).</span></span>

    <span data-ttu-id="cde1c-113">Alle Implementierungen von [**iwbemproviderinit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) müssen [**iwbemproviderinitsink:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) aufrufen, um den Initialisierungs Status an WMI zu melden.</span><span class="sxs-lookup"><span data-stu-id="cde1c-113">All implementations of [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) must call [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to report initialization status to WMI.</span></span> <span data-ttu-id="cde1c-114">Mit der **SetStatus** -Methode kann WMI ermitteln, ob ein Anbieter für den Empfang von Anforderungen bereit ist, und die Art der Anforderungen, die der Anbieter empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="cde1c-114">The **SetStatus** method allows WMI to determine if a provider is ready to receive requests and the type of requests that the provider is ready to receive.</span></span>

<span data-ttu-id="cde1c-115">Im folgenden Verfahren wird beschrieben, wie eine erfolgreiche Initialisierung gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="cde1c-115">The following procedure describes how to report a successful initialization.</span></span>

<span data-ttu-id="cde1c-116">**So melden Sie eine erfolgreiche Initialisierung**</span><span class="sxs-lookup"><span data-stu-id="cde1c-116">**To report a successful initialization**</span></span>

-   <span data-ttu-id="cde1c-117">Legen Sie den *istatus* -Parameter von [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) auf **WBEM \_ S \_ Initialized** fest.</span><span class="sxs-lookup"><span data-stu-id="cde1c-117">Set the *IStatus* parameter of [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to **WBEM\_S\_INITIALIZED**.</span></span>

    <span data-ttu-id="cde1c-118">Durch das Zurückgeben von **WBEM S, das \_ \_ Initialisiert** wurde, gibt ein Anbieter eine Bereitschaft zum Verarbeiten von Anforderungen von Anwendungen, WMI und anderen Anbietern an.</span><span class="sxs-lookup"><span data-stu-id="cde1c-118">By returning **WBEM\_S\_INITIALIZED**, a provider indicates a readiness to handle requests from applications, WMI, and other providers.</span></span> <span data-ttu-id="cde1c-119">Nach \_ \_ dem Initialisieren von WBEM S ruft WMI die [**iwbemproviderinit:: QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Methode für den Anbieter auf.</span><span class="sxs-lookup"><span data-stu-id="cde1c-119">After receiving WBEM\_S\_INITIALIZED, WMI makes a call to the [**IWbemProviderInit::QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) method on the provider.</span></span> <span data-ttu-id="cde1c-120">Diese Abfrage ruft einen Zeiger auf die primäre Schnittstelle des Anbieters ab.</span><span class="sxs-lookup"><span data-stu-id="cde1c-120">This query retrieves a pointer to the primary interface of the provider.</span></span>

<span data-ttu-id="cde1c-121">Im folgenden Verfahren wird beschrieben, wie ein Fehler während der Initialisierung gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="cde1c-121">The following procedure describes how to report an error during initialization.</span></span>

<span data-ttu-id="cde1c-122">**So melden Sie einen Fehler während der Initialisierung**</span><span class="sxs-lookup"><span data-stu-id="cde1c-122">**To report an error during initialization**</span></span>

-   <span data-ttu-id="cde1c-123">Fehler beim Festlegen des *istatus* -Parameters von [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) auf **WBEM \_ E \_**.</span><span class="sxs-lookup"><span data-stu-id="cde1c-123">Set the *IStatus* parameter of [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to **WBEM\_E\_FAILED**.</span></span> <span data-ttu-id="cde1c-124">WMI-Ansichts Anbieter, die **WBEM \_ E \_** zurückgeben, sind nicht funktionsfähig.</span><span class="sxs-lookup"><span data-stu-id="cde1c-124">WMI views providers that return **WBEM\_E\_FAILED** as not functional.</span></span>

    <span data-ttu-id="cde1c-125">WMI gibt den [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Zeiger entweder dann frei, nachdem WMI einen Zeiger auf die primäre Schnittstelle des Anbieters abgerufen hat oder wenn die Initialisierung fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="cde1c-125">WMI releases the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pointer either after WMI has obtained a pointer to the primary interface of the provider or after initialization has failed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cde1c-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cde1c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cde1c-127">Entwickeln eines WMI-Anbieters</span><span class="sxs-lookup"><span data-stu-id="cde1c-127">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="cde1c-128">Festlegen von namepace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="cde1c-128">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="cde1c-129">Sichern Ihres Anbieters</span><span class="sxs-lookup"><span data-stu-id="cde1c-129">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 



