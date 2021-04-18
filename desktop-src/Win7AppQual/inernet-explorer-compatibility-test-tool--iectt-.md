---
description: .
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: Internet Explorer-Kompatibilitätstest-Tool (Internet Explorer Compatibility Test Tool, IECTT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25e39263f448c7e11db1be32463b3801e4a8761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347643"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a><span data-ttu-id="8d906-103">Internet Explorer-Kompatibilitätstest-Tool (Internet Explorer Compatibility Test Tool, IECTT)</span><span class="sxs-lookup"><span data-stu-id="8d906-103">Internet Explorer Compatibility Test Tool (IECTT)</span></span>

<span data-ttu-id="8d906-104">Das Internet Explorer Compatibility Test Tool (iectt) ist eine Komponente des [Microsoft Anwendungskompatibilitäts-Toolkits](/windows-hardware/get-started/adk-install).</span><span class="sxs-lookup"><span data-stu-id="8d906-104">The Internet Explorer Compatibility Test Tool (IECTT) is a component of the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span></span> <span data-ttu-id="8d906-105">Mithilfe dieses Tools können Sie Probleme in Ihren Webanwendungen diagnostizieren, indem Sie Probleme in Echtzeit anzeigen und optional die Ergebnisse in eine ACT-Datenbank hochladen.</span><span class="sxs-lookup"><span data-stu-id="8d906-105">This tool can help you diagnose issues in your web applications by displaying issues in real time and optionally uploading the results to an ACT database.</span></span> <span data-ttu-id="8d906-106">Die Ergebnisse enthalten Details zu möglichen Kompatibilitätsproblemen und Links, um weitere Informationen zu jedem Kompatibilitätsproblem zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8d906-106">The results include details about possible compatibility issues and links for more information about each compatibility issue.</span></span> <span data-ttu-id="8d906-107">Iectt ermöglicht es Ihnen außerdem, Probleme auszuschließen und verfügbare Attribute zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8d906-107">IECTT also enables you to exclude issues and modify available attributes.</span></span>

## <a name="to-open-iectt"></a><span data-ttu-id="8d906-108">So öffnen Sie iectt</span><span class="sxs-lookup"><span data-stu-id="8d906-108">To open IECTT</span></span>

1.  <span data-ttu-id="8d906-109">Installieren Sie das [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span><span class="sxs-lookup"><span data-stu-id="8d906-109">Install the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span></span>
2.  <span data-ttu-id="8d906-110">Klicken Sie auf **Start**, zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft Application Compatibility Toolkit 5,6**, zeigen Sie auf **Entwickler-und Tester-Tools**, und klicken Sie dann auf **Internet Explorer Compatibility Test Tool**.</span><span class="sxs-lookup"><span data-stu-id="8d906-110">Click **Start**, point to **Programs**, point to **Microsoft Application Compatibility Toolkit 5.6**, point to **Developer and Tester Tools**, and then click **Internet Explorer Compatibility Test Tool**.</span></span>

<span data-ttu-id="8d906-111">In den folgenden Abschnitten werden gängige iectt-Szenarios beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8d906-111">The following sections describe common IECTT scenarios.</span></span>

## <a name="view-issues-in-real-time"></a><span data-ttu-id="8d906-112">Anzeigen von Problemen in Echtzeit</span><span class="sxs-lookup"><span data-stu-id="8d906-112">View Issues in Real Time</span></span>

<span data-ttu-id="8d906-113">Sie können Ihre webbasierten Probleme in Echtzeit suchen und anzeigen, während Sie Ihre Websites und Webanwendungen mit Windows Internet Explorer 7 und Windows Internet Explorer 8 testen.</span><span class="sxs-lookup"><span data-stu-id="8d906-113">You can locate and view your web-based issues in real time, while you are testing your websites and web applications against Windows Internet Explorer 7 and Windows Internet Explorer 8.</span></span> <span data-ttu-id="8d906-114">Nachdem Sie die Tests durchgeführt haben, können Sie die Ergebnisse im Bildschirm **Live Daten** von iectt anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8d906-114">After you complete your testing, you can view your results in the **Live Data** screen of the IECTT.</span></span>

## <a name="upload-issues-to-your-act-database"></a><span data-ttu-id="8d906-115">Hochladen von Problemen in Ihre Act-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8d906-115">Upload Issues to Your ACT Database</span></span>

<span data-ttu-id="8d906-116">Sie können Ihre webbasierten Probleme in die ACT-Datenbank hochladen, die die Informationen verarbeitet und es Ihnen ermöglicht, die Ergebnisse auf dem **Analyse** Bildschirm des Anwendungskompatibilitäts-Managers anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8d906-116">You can upload your web-based issues to the ACT database, which processes the information and enables you to view your results on the **Analyze** screen of the Application Compatibility Manager.</span></span>

## <a name="collect-your-compatibility-data"></a><span data-ttu-id="8d906-117">Sammeln von Kompatibilitäts Daten</span><span class="sxs-lookup"><span data-stu-id="8d906-117">Collect Your Compatibility Data</span></span>

<span data-ttu-id="8d906-118">Sie können Ihre Website-und Webanwendungs bezogenen Kompatibilitäts Daten erfassen, indem Sie das iectt-Tool entweder mit Internet Explorer 7 oder Internet Explorer 7 verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d906-118">You can collect your website and web application-related compatibility data by using the IECTT tool with either Internet Explorer 7 or Internet Explorer 7.</span></span>

<span data-ttu-id="8d906-119">**So erfassen Sie Kompatibilitäts Daten**</span><span class="sxs-lookup"><span data-stu-id="8d906-119">**To collect your compatibility data**</span></span>

1.  <span data-ttu-id="8d906-120">Schließen Sie alle aktiven Windows Internet Explorer-Fenster.</span><span class="sxs-lookup"><span data-stu-id="8d906-120">Close all of your active Windows Internet Explorer windows.</span></span>
2.  <span data-ttu-id="8d906-121">Klicken Sie in iectt auf der Symbolleiste des **Kompatibilitäts Testtools für Internet Explorer** auf **aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="8d906-121">In IECTT, on the **Internet Explorer Compatibility Test Tool** toolbar, click **Enable**.</span></span>
3.  <span data-ttu-id="8d906-122">Öffnen Sie ein Fenster von Internet Explorer 7 oder Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="8d906-122">Open an Internet Explorer 7 or Internet Explorer 8 window.</span></span>

    <span data-ttu-id="8d906-123">Eine Meldung wird angezeigt, die besagt, dass die Kompatibilitäts Bewertungs Protokollierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8d906-123">A message appears and states that compatibility evaluation logging is turned on.</span></span>

4.  <span data-ttu-id="8d906-124">Besuchen Sie die Websites oder Webanwendungen, die für die Verwendung durch Ihre Organisation erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8d906-124">Visit the websites or web applications that are required for use by your organization.</span></span> <span data-ttu-id="8d906-125">Beim Besuch der einzelnen Standorte zeigt das iectt-Tool in Echtzeit Ihre potenziellen Kompatibilitätsprobleme an.</span><span class="sxs-lookup"><span data-stu-id="8d906-125">As you visit each site, the IECTT tool displays, in real-time, your potential compatibility issues.</span></span>
5.  <span data-ttu-id="8d906-126">Klicken Sie in der Symbolleiste des **Kompatibilitäts Testtools für Internet Explorer** auf **Deaktivieren** , wenn Sie dies abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="8d906-126">On the **Internet Explorer Compatibility Test Tool** toolbar, click **Disable** when you are done.</span></span>

    <span data-ttu-id="8d906-127">Der Kompatibilitäts Protokollierungs Prozess wird beendet und beendet.</span><span class="sxs-lookup"><span data-stu-id="8d906-127">The compatibility logging process finishes and stops.</span></span>

## <a name="filter-your-issue-results"></a><span data-ttu-id="8d906-128">Filtern Ihrer Problem Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="8d906-128">Filter Your Issue Results</span></span>

<span data-ttu-id="8d906-129">Sie können Ihre iectt-Ergebnisse nach Objektname, Problemtyp oder beides filtern.</span><span class="sxs-lookup"><span data-stu-id="8d906-129">You can filter any of your IECTT results by object name, by issue type, or by both.</span></span>

<span data-ttu-id="8d906-130">**So filtern Sie Ihre Problem Ergebnisse**</span><span class="sxs-lookup"><span data-stu-id="8d906-130">**To filter your issue results**</span></span>

1.  <span data-ttu-id="8d906-131">Klicken Sie im Bildschirm **Kompatibilitäts Test-Tool für Internet Explorer** auf **Filtern**.</span><span class="sxs-lookup"><span data-stu-id="8d906-131">On the **Internet Explorer Compatibility Test Tool** screen, click **Filter**.</span></span>

    <span data-ttu-id="8d906-132">Das Dialogfeld **Probleme Filtern** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d906-132">The **Issues Filter** dialog box appears.</span></span>

2.  <span data-ttu-id="8d906-133">Geben Sie den Namen des Objekts ein, das Sie im Feld **Geben Sie den Namen des Objekts ein, das Probleme anzeigen soll** angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d906-133">Enter the name of the object that you intend to view in the **Enter the name of the object to view issues for** box.</span></span>

<span data-ttu-id="8d906-134">Weitere Informationen zu diesem Tool und anderen Entwicklertools finden Sie unter [Was ist das Internet Explorer-Kompatibilitäts Test-Tool?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) in der MSDN Library und im Blogbeitrag zur [Anwendungs Kompatibilitäts Protokollierung in IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) .</span><span class="sxs-lookup"><span data-stu-id="8d906-134">For more information about this tool and other developers tools, see [What is the Internet Explorer Compatibility Test Tool?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) in the MSDN Library and the [Application Compatibility Logging in IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) blog post.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d906-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8d906-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d906-136">Tools zum Debuggen von Webanwendungen und Add-ons</span><span class="sxs-lookup"><span data-stu-id="8d906-136">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
