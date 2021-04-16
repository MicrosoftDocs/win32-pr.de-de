---
description: Wenn eine SOAP-fähige Anwendung von einem Server im Proxy Modus exportiert wurde, können Clients, die Sie importieren, automatisch auf die Methoden der enthaltenen Komponenten zugreifen, Remote als Webdienste, die vom Server im Client aktivierten Objekt Modus (Cao) angeboten werden. Dies ermöglicht die einfache Bereitstellung der Funktionalität einer COM+-Anwendung in einem Netzwerk als XML-Webdienst.
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: Importieren einer SOAP-Enabled Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9faca91a726caea765d4b2ca227ddba0ff3a2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524200"
---
# <a name="importing-a-soap-enabled-application"></a><span data-ttu-id="bb7fa-104">Importieren einer SOAP-Enabled Anwendung</span><span class="sxs-lookup"><span data-stu-id="bb7fa-104">Importing a SOAP-Enabled Application</span></span>

<span data-ttu-id="bb7fa-105">Wenn eine SOAP-fähige Anwendung von einem Server im Proxy Modus [exportiert](exporting-a-soap-enabled-application.md) wurde, können Clients, die Sie importieren, automatisch auf die Methoden der enthaltenen Komponenten zugreifen, Remote als Webdienste, die vom Server im Client aktivierten Objekt Modus (Cao) angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="bb7fa-105">When a SOAP-enabled application has been [exported](exporting-a-soap-enabled-application.md) from a server in proxy mode, clients that import it can automatically access the methods of the components it contains, remotely, as web services offered by the server in client-activated object (CAO) mode.</span></span> <span data-ttu-id="bb7fa-106">Dies ermöglicht die einfache Bereitstellung der Funktionalität einer COM+-Anwendung in einem Netzwerk als XML-Webdienst.</span><span class="sxs-lookup"><span data-stu-id="bb7fa-106">This allows you to very easily deploy the functionality of a COM+ application across a network as an XML web service.</span></span>

<span data-ttu-id="bb7fa-107">Wenn die Komponenten einer Anwendung, die auf diese Weise importiert werden, auf dem Client verwendet werden, werden Sie nicht auf dem Client ausgeführt, sondern der Zugriff erfolgt über einen Remote Zugriff mithilfe des XML-Webdiensts, der von dem Server bereitgestellt wird, von dem die Anwendung exportiert wurde.</span><span class="sxs-lookup"><span data-stu-id="bb7fa-107">When the components of an application imported in this way are used on the client, they do not run on the client but instead are accessed remotely by using the XML web service provided by the server from which the application was exported.</span></span> <span data-ttu-id="bb7fa-108">Ausführliche Informationen zur Verwendung der Komponenten einer Anwendung, die auf diese Weise importiert werden, finden Sie unter [zugreifen auf XML-Webdienste im Modus "Cao](accessing-xml-web-services-in-cao-mode.md)".</span><span class="sxs-lookup"><span data-stu-id="bb7fa-108">For details on using the components of an application imported in this way, see [Accessing XML Web Services in CAO Mode](accessing-xml-web-services-in-cao-mode.md).</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="bb7fa-109">Verwaltungs Tool für Komponenten Dienste</span><span class="sxs-lookup"><span data-stu-id="bb7fa-109">Component Services Administrative Tool</span></span>

<span data-ttu-id="bb7fa-110">Führen Sie die folgenden Schritte aus, um eine SOAP-fähige Anwendung in einen Client zu importieren:</span><span class="sxs-lookup"><span data-stu-id="bb7fa-110">To import a SOAP-enabled application into a client, use the following steps:</span></span>

1.  <span data-ttu-id="bb7fa-111">Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste unter **Komponenten Dienste** den Ordner, der dem Client Computer zugeordnet ist, auf dem Sie die Anwendung installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="bb7fa-111">In the console tree of the Component Services administrative tool, under **Component Services**, open the folder associated with the client computer on which you want to install the application.</span></span>

2.  <span data-ttu-id="bb7fa-112">Klicken Sie mit der rechten Maustaste auf den **com+-Anwendungs** Ordner des Clients, und wählen Sie dann **neu** aus.</span><span class="sxs-lookup"><span data-stu-id="bb7fa-112">Right-click the client's **COM+ Applications** folder, and then choose **New**.</span></span> <span data-ttu-id="bb7fa-113">Der **COM+-Anwendungsinstallations-Assistent** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bb7fa-113">The **COM+ Application Install Wizard** appears.</span></span>

3.  <span data-ttu-id="bb7fa-114">Klicken Sie im **com+**-Anwendungsinstallations-Assistenten auf **vorgefertigte Anwendung (en) installieren**.</span><span class="sxs-lookup"><span data-stu-id="bb7fa-114">In the **COM+ Application Install Wizard**, click **Install pre-built application(s)**.</span></span>

4.  <span data-ttu-id="bb7fa-115">Suchen Sie im Netzwerk nach dem Netzwerkpfad der MSI-Datei auf dem Server, auf dem Sie die Anwendung installieren möchten, oder geben Sie ihn an.</span><span class="sxs-lookup"><span data-stu-id="bb7fa-115">Browse the network to locate or specify the network path of the MSI file on the server from which you want to install the application.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="bb7fa-116">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bb7fa-116">Visual Basic</span></span>

<span data-ttu-id="bb7fa-117">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="bb7fa-117">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="bb7fa-118">C/C++</span><span class="sxs-lookup"><span data-stu-id="bb7fa-118">C/C++</span></span>

<span data-ttu-id="bb7fa-119">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="bb7fa-119">Does not apply.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb7fa-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb7fa-120">Remarks</span></span>

<span data-ttu-id="bb7fa-121">COM-Komponenten werden durch eine GUID identifiziert, die sich ändert, wenn die Komponenten neu kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="bb7fa-121">COM components are identified by a GUID, which changes if the components are recompiled.</span></span> <span data-ttu-id="bb7fa-122">Wenn eine konfigurierte COM-Komponente, die als XML-Webdienst verfügbar gemacht wird, neu kompiliert wird, werden die Client Anwendungen, die Sie verwenden, unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="bb7fa-122">If a configured COM component that is exposed as an XML web service is recompiled, client applications that use it will break.</span></span> <span data-ttu-id="bb7fa-123">Wenn also eine Komponente, die als XML-Webdienst verfügbar gemacht wird, neu kompiliert wird, sollten die Clients die Anwendungen erneut importieren, die die Komponente verwenden.</span><span class="sxs-lookup"><span data-stu-id="bb7fa-123">Therefore, when a component that is exposed as an XML web service is recompiled, clients should re-import the applications that use the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb7fa-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb7fa-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb7fa-125">Übersicht über den COM+ SOAP-Dienst</span><span class="sxs-lookup"><span data-stu-id="bb7fa-125">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="bb7fa-126">Erstellen von XML-Webdiensten</span><span class="sxs-lookup"><span data-stu-id="bb7fa-126">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="bb7fa-127">Exportieren einer SOAP-Enabled Anwendung</span><span class="sxs-lookup"><span data-stu-id="bb7fa-127">Exporting a SOAP-Enabled Application</span></span>](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



