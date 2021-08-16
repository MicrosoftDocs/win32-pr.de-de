---
description: Wenn Sie COM+ verwenden, um einen XML-Webdienst zu erstellen, kann dieser Dienst von jedem autorisierten Client verwendet werden, einschließlich derjenigen, die COM+ oder sogar Microsoft Windows nicht verwenden.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Exportieren einer SOAP-Enabled-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce79bbc5dca59feb23ba9e976575b3b33570ecd27cf1e6a68560b02e073f48bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307287"
---
# <a name="exporting-a-soap-enabled-application"></a>Exportieren einer SOAP-Enabled-Anwendung

Wenn Sie COM+ verwenden, um einen XML-Webdienst zu erstellen, kann dieser Dienst von jedem autorisierten Client verwendet werden, einschließlich derjenigen, die COM+ oder sogar Microsoft Windows nicht verwenden. Die Verwendung eines COM+-Webdiensts im Cao-Modus (Client-Activated Object) einer COM+-Clientanwendung ist jedoch besonders einfach. Exportieren Sie einfach die SOAP-fähige Anwendung im Proxymodus, und [importieren](importing-a-soap-enabled-application.md) Sie sie dann in den Client, für den Sie auf den entsprechenden XML-Webdienst zugreifen möchten.

## <a name="component-services-administrative-tool"></a>Verwaltungstool "Komponentendienste"

Um eine SOAP-fähige Anwendung von einem Server zu exportieren, verwenden Sie die folgenden Schritte:

1.  Öffnen Sie in der Konsolenstruktur des Component Services-Verwaltungstools unter **Komponentendienste** den Ordner **COM+-Anwendungen,** der dem zu verwaltenden Computer zugeordnet ist.

2.  Klicken Sie mit der rechten Maustaste auf die Komponente, die Sie als XML-Webdienst verfügbar machen möchten, und wählen Sie **Exportieren** aus. Der **COM+-Anwendungsexport-Assistent** wird angezeigt.

3.  Geben Sie im Textfeld mit der Bezeichnung **Geben Sie den vollständigen Pfad und Dateinamen für die zu erstellende Anwendungsdatei** ein, geben Sie den vollständigen Pfad und Dateinamen für die MSI-Datei ein, die die exportierte Anwendung enthalten soll, oder klicken Sie auf **Durchsuchen,** um den vollständigen Pfad und Dateinamen in einem Dialogfeld auszuwählen.

4.  Wählen Sie unter **Exportieren als** das Optionsfeld Anwendungsproxy – Installation auf anderen **Computern aus, um den Zugriff auf diesen Computer zu ermöglichen.**

## <a name="visual-basic"></a>Visual Basic

Nicht anwendbar.

## <a name="cc"></a>C/C++

Nicht anwendbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über den COM+-SOAP-Dienst](com--soap-service-overview.md)
</dt> <dt>

[Erstellen von XML-Webdiensten](creating-xml-web-services.md)
</dt> <dt>

[Importieren einer SOAP-Enabled-Anwendung](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



