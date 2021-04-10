---
description: Wenn Sie com+ zum Erstellen eines XML-Webdiensts verwenden, kann dieser Dienst von jedem autorisierten Client verwendet werden, einschließlich derjenigen, die nicht com+ oder sogar Microsoft Windows verwenden.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Exportieren einer SOAP-Enabled Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c92029f431fc06964f233c5746c283821d11c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861372"
---
# <a name="exporting-a-soap-enabled-application"></a><span data-ttu-id="e86a7-103">Exportieren einer SOAP-Enabled Anwendung</span><span class="sxs-lookup"><span data-stu-id="e86a7-103">Exporting a SOAP-Enabled Application</span></span>

<span data-ttu-id="e86a7-104">Wenn Sie com+ zum Erstellen eines XML-Webdiensts verwenden, kann dieser Dienst von jedem autorisierten Client verwendet werden, einschließlich derjenigen, die nicht com+ oder sogar Microsoft Windows verwenden.</span><span class="sxs-lookup"><span data-stu-id="e86a7-104">When you use COM+ to create an XML web service, that service can be used by any authorized client, including those not using COM+ or even Microsoft Windows.</span></span> <span data-ttu-id="e86a7-105">Die Verwendung eines com+-Webdiensts im-Client aktivierten Objekt Modus (Cao) aus einer com+-Client Anwendung ist jedoch besonders einfach.</span><span class="sxs-lookup"><span data-stu-id="e86a7-105">However, using a COM+ web service in client-activated object (CAO) mode from a COM+ client application is especially easy.</span></span> <span data-ttu-id="e86a7-106">Exportieren Sie einfach die SOAP-aktivierte Anwendung im Proxy Modus, und [importieren](importing-a-soap-enabled-application.md) Sie Sie dann in den Client, für den Sie auf den entsprechenden XML-Webdienst zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="e86a7-106">Just export the SOAP-enabled application in proxy mode, and then [import](importing-a-soap-enabled-application.md) it into the client for which you want to access the corresponding XML web service.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="e86a7-107">Verwaltungs Tool für Komponenten Dienste</span><span class="sxs-lookup"><span data-stu-id="e86a7-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="e86a7-108">Führen Sie die folgenden Schritte aus, um eine SOAP-fähige Anwendung von einem Server zu exportieren:</span><span class="sxs-lookup"><span data-stu-id="e86a7-108">To export a SOAP-enabled application from a server, use the following steps:</span></span>

1.  <span data-ttu-id="e86a7-109">Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste unter **Komponenten Dienste** den Ordner **com+-Anwendungen** , der dem Computer zugeordnet ist, den Sie verwalten möchten.</span><span class="sxs-lookup"><span data-stu-id="e86a7-109">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you want to manage.</span></span>

2.  <span data-ttu-id="e86a7-110">Klicken Sie mit der rechten Maustaste auf die Komponente, die Sie als XML-Webdienst verfügbar machen möchten, und wählen Sie **exportieren** aus.</span><span class="sxs-lookup"><span data-stu-id="e86a7-110">Right-click the component you want to expose as an XML web service, and choose **Export**.</span></span> <span data-ttu-id="e86a7-111">Der **com+-Anwendungs Export-Assistent** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e86a7-111">The **COM+ Application Export Wizard** appears.</span></span>

3.  <span data-ttu-id="e86a7-112">Geben Sie im Textfeld mit **der Bezeichnung den vollständigen Pfad und Dateinamen für die zu erstellende Anwendungsdatei** ein. Geben Sie den vollständigen Pfad und Dateinamen für die MSI-Datei ein, die die exportierte Anwendung enthalten soll, oder klicken Sie auf **Durchsuchen** , um den vollständigen Pfad und Dateinamen</span><span class="sxs-lookup"><span data-stu-id="e86a7-112">In the text box labeled **Enter the full path and filename for the application file to be created**, enter the full path and filename for the MSI file that will contain the exported application, or click **Browse** to select the full path and filename using a dialog box.</span></span>

4.  <span data-ttu-id="e86a7-113">Wählen Sie unter **Exportieren als** den **Anwendungs Proxy – auf anderen Computern installieren aus, um den Zugriff auf diesen Computer zu aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="e86a7-113">Under **Export As**, select the **Application Proxy – Install on other machines to enable access to this machine** radio button.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="e86a7-114">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e86a7-114">Visual Basic</span></span>

<span data-ttu-id="e86a7-115">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="e86a7-115">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="e86a7-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="e86a7-116">C/C++</span></span>

<span data-ttu-id="e86a7-117">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="e86a7-117">Does not apply.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e86a7-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e86a7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e86a7-119">Übersicht über den COM+ SOAP-Dienst</span><span class="sxs-lookup"><span data-stu-id="e86a7-119">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="e86a7-120">Erstellen von XML-Webdiensten</span><span class="sxs-lookup"><span data-stu-id="e86a7-120">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="e86a7-121">Importieren einer SOAP-Enabled Anwendung</span><span class="sxs-lookup"><span data-stu-id="e86a7-121">Importing a SOAP-Enabled Application</span></span>](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



