---
description: Wenn Sie COM+ zum Erstellen eines XML-Webdiensts verwenden, kann dieser Dienst von jedem autorisierten Client verwendet werden, einschließlich clients, die COM+ oder sogar Microsoft Windows.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Exportieren einer SOAP-Enabled Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce79bbc5dca59feb23ba9e976575b3b33570ecd27cf1e6a68560b02e073f48bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307287"
---
# <a name="exporting-a-soap-enabled-application"></a>Exportieren einer SOAP-Enabled Anwendung

Wenn Sie COM+ zum Erstellen eines XML-Webdiensts verwenden, kann dieser Dienst von jedem autorisierten Client verwendet werden, einschließlich clients, die COM+ oder sogar Microsoft Windows. Die Verwendung eines COM+-Webdiensts im CAO-Modus (Client-Activated Object) aus einer COM+-Clientanwendung ist jedoch besonders einfach. Exportieren Sie einfach die SOAP-fähige Anwendung [](importing-a-soap-enabled-application.md) im Proxymodus, und importieren Sie sie dann in den Client, für den Sie auf den entsprechenden XML-Webdienst zugreifen möchten.

## <a name="component-services-administrative-tool"></a>Verwaltungstool für Komponentendienste

Führen Sie die folgenden Schritte aus, um eine SOAP-fähige Anwendung von einem Server zu exportieren:

1.  Öffnen Sie in der Konsolenstruktur des Verwaltungstool Komponentendienste unter Komponentendienste den **Ordner COM+-Anwendungen,** der dem computer zugeordnet ist, den Sie verwalten möchten.

2.  Klicken Sie mit der rechten Maustaste auf die Komponente, die Sie als XML-Webdienst verfügbar machen möchten, und wählen Sie **Exportieren aus.** Der **COM+-Anwendungsexport-Assistent wird** angezeigt.

3.  Geben Sie im Textfeld Geben Sie den vollständigen Pfad und Dateinamen für die zu erstellende Anwendungsdatei **ein,** geben  Sie den vollständigen Pfad und Dateinamen für die MSI-Datei ein, die die exportierte Anwendung enthalten soll, oder klicken Sie auf Durchsuchen, um den vollständigen Pfad und Dateinamen mithilfe eines Dialogfelds auszuwählen.

4.  Wählen **Sie unter Exportieren** als das Optionsfeld Anwendungsproxy – Auf anderen Computern installieren **aus, um den** Zugriff auf diesen Computer zu ermöglichen.

## <a name="visual-basic"></a>Visual Basic

Nicht anwendbar.

## <a name="cc"></a>C/C++

Nicht anwendbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ÜBERSICHT ÜBER DEN COM+-SOAP-Dienst](com--soap-service-overview.md)
</dt> <dt>

[Erstellen von XML-Webdiensten](creating-xml-web-services.md)
</dt> <dt>

[Importieren einer SOAP-Enabled Anwendung](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



