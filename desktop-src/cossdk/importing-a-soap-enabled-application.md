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
# <a name="importing-a-soap-enabled-application"></a>Importieren einer SOAP-Enabled Anwendung

Wenn eine SOAP-fähige Anwendung von einem Server im Proxy Modus [exportiert](exporting-a-soap-enabled-application.md) wurde, können Clients, die Sie importieren, automatisch auf die Methoden der enthaltenen Komponenten zugreifen, Remote als Webdienste, die vom Server im Client aktivierten Objekt Modus (Cao) angeboten werden. Dies ermöglicht die einfache Bereitstellung der Funktionalität einer COM+-Anwendung in einem Netzwerk als XML-Webdienst.

Wenn die Komponenten einer Anwendung, die auf diese Weise importiert werden, auf dem Client verwendet werden, werden Sie nicht auf dem Client ausgeführt, sondern der Zugriff erfolgt über einen Remote Zugriff mithilfe des XML-Webdiensts, der von dem Server bereitgestellt wird, von dem die Anwendung exportiert wurde. Ausführliche Informationen zur Verwendung der Komponenten einer Anwendung, die auf diese Weise importiert werden, finden Sie unter [zugreifen auf XML-Webdienste im Modus "Cao](accessing-xml-web-services-in-cao-mode.md)".

## <a name="component-services-administrative-tool"></a>Verwaltungs Tool für Komponenten Dienste

Führen Sie die folgenden Schritte aus, um eine SOAP-fähige Anwendung in einen Client zu importieren:

1.  Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste unter **Komponenten Dienste** den Ordner, der dem Client Computer zugeordnet ist, auf dem Sie die Anwendung installieren möchten.

2.  Klicken Sie mit der rechten Maustaste auf den **com+-Anwendungs** Ordner des Clients, und wählen Sie dann **neu** aus. Der **COM+-Anwendungsinstallations-Assistent** wird angezeigt.

3.  Klicken Sie im **com+**-Anwendungsinstallations-Assistenten auf **vorgefertigte Anwendung (en) installieren**.

4.  Suchen Sie im Netzwerk nach dem Netzwerkpfad der MSI-Datei auf dem Server, auf dem Sie die Anwendung installieren möchten, oder geben Sie ihn an.

## <a name="visual-basic"></a>Visual Basic

Nicht anwendbar.

## <a name="cc"></a>C/C++

Nicht anwendbar.

## <a name="remarks"></a>Bemerkungen

COM-Komponenten werden durch eine GUID identifiziert, die sich ändert, wenn die Komponenten neu kompiliert werden. Wenn eine konfigurierte COM-Komponente, die als XML-Webdienst verfügbar gemacht wird, neu kompiliert wird, werden die Client Anwendungen, die Sie verwenden, unterbrechen. Wenn also eine Komponente, die als XML-Webdienst verfügbar gemacht wird, neu kompiliert wird, sollten die Clients die Anwendungen erneut importieren, die die Komponente verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über den COM+ SOAP-Dienst](com--soap-service-overview.md)
</dt> <dt>

[Erstellen von XML-Webdiensten](creating-xml-web-services.md)
</dt> <dt>

[Exportieren einer SOAP-Enabled Anwendung](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



