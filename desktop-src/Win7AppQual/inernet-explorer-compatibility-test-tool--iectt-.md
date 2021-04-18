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
# <a name="internet-explorer-compatibility-test-tool-iectt"></a>Internet Explorer-Kompatibilitätstest-Tool (Internet Explorer Compatibility Test Tool, IECTT)

Das Internet Explorer Compatibility Test Tool (iectt) ist eine Komponente des [Microsoft Anwendungskompatibilitäts-Toolkits](/windows-hardware/get-started/adk-install). Mithilfe dieses Tools können Sie Probleme in Ihren Webanwendungen diagnostizieren, indem Sie Probleme in Echtzeit anzeigen und optional die Ergebnisse in eine ACT-Datenbank hochladen. Die Ergebnisse enthalten Details zu möglichen Kompatibilitätsproblemen und Links, um weitere Informationen zu jedem Kompatibilitätsproblem zu erhalten. Iectt ermöglicht es Ihnen außerdem, Probleme auszuschließen und verfügbare Attribute zu ändern.

## <a name="to-open-iectt"></a>So öffnen Sie iectt

1.  Installieren Sie das [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).
2.  Klicken Sie auf **Start**, zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft Application Compatibility Toolkit 5,6**, zeigen Sie auf **Entwickler-und Tester-Tools**, und klicken Sie dann auf **Internet Explorer Compatibility Test Tool**.

In den folgenden Abschnitten werden gängige iectt-Szenarios beschrieben.

## <a name="view-issues-in-real-time"></a>Anzeigen von Problemen in Echtzeit

Sie können Ihre webbasierten Probleme in Echtzeit suchen und anzeigen, während Sie Ihre Websites und Webanwendungen mit Windows Internet Explorer 7 und Windows Internet Explorer 8 testen. Nachdem Sie die Tests durchgeführt haben, können Sie die Ergebnisse im Bildschirm **Live Daten** von iectt anzeigen.

## <a name="upload-issues-to-your-act-database"></a>Hochladen von Problemen in Ihre Act-Datenbank

Sie können Ihre webbasierten Probleme in die ACT-Datenbank hochladen, die die Informationen verarbeitet und es Ihnen ermöglicht, die Ergebnisse auf dem **Analyse** Bildschirm des Anwendungskompatibilitäts-Managers anzuzeigen.

## <a name="collect-your-compatibility-data"></a>Sammeln von Kompatibilitäts Daten

Sie können Ihre Website-und Webanwendungs bezogenen Kompatibilitäts Daten erfassen, indem Sie das iectt-Tool entweder mit Internet Explorer 7 oder Internet Explorer 7 verwenden.

**So erfassen Sie Kompatibilitäts Daten**

1.  Schließen Sie alle aktiven Windows Internet Explorer-Fenster.
2.  Klicken Sie in iectt auf der Symbolleiste des **Kompatibilitäts Testtools für Internet Explorer** auf **aktivieren**.
3.  Öffnen Sie ein Fenster von Internet Explorer 7 oder Internet Explorer 8.

    Eine Meldung wird angezeigt, die besagt, dass die Kompatibilitäts Bewertungs Protokollierung aktiviert ist.

4.  Besuchen Sie die Websites oder Webanwendungen, die für die Verwendung durch Ihre Organisation erforderlich sind. Beim Besuch der einzelnen Standorte zeigt das iectt-Tool in Echtzeit Ihre potenziellen Kompatibilitätsprobleme an.
5.  Klicken Sie in der Symbolleiste des **Kompatibilitäts Testtools für Internet Explorer** auf **Deaktivieren** , wenn Sie dies abgeschlossen haben.

    Der Kompatibilitäts Protokollierungs Prozess wird beendet und beendet.

## <a name="filter-your-issue-results"></a>Filtern Ihrer Problem Ergebnisse

Sie können Ihre iectt-Ergebnisse nach Objektname, Problemtyp oder beides filtern.

**So filtern Sie Ihre Problem Ergebnisse**

1.  Klicken Sie im Bildschirm **Kompatibilitäts Test-Tool für Internet Explorer** auf **Filtern**.

    Das Dialogfeld **Probleme Filtern** wird angezeigt.

2.  Geben Sie den Namen des Objekts ein, das Sie im Feld **Geben Sie den Namen des Objekts ein, das Probleme anzeigen soll** angezeigt werden soll.

Weitere Informationen zu diesem Tool und anderen Entwicklertools finden Sie unter [Was ist das Internet Explorer-Kompatibilitäts Test-Tool?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) in der MSDN Library und im Blogbeitrag zur [Anwendungs Kompatibilitäts Protokollierung in IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Tools zum Debuggen von Webanwendungen und Add-ons](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
