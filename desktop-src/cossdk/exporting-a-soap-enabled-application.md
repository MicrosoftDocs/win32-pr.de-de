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
# <a name="exporting-a-soap-enabled-application"></a>Exportieren einer SOAP-Enabled Anwendung

Wenn Sie com+ zum Erstellen eines XML-Webdiensts verwenden, kann dieser Dienst von jedem autorisierten Client verwendet werden, einschließlich derjenigen, die nicht com+ oder sogar Microsoft Windows verwenden. Die Verwendung eines com+-Webdiensts im-Client aktivierten Objekt Modus (Cao) aus einer com+-Client Anwendung ist jedoch besonders einfach. Exportieren Sie einfach die SOAP-aktivierte Anwendung im Proxy Modus, und [importieren](importing-a-soap-enabled-application.md) Sie Sie dann in den Client, für den Sie auf den entsprechenden XML-Webdienst zugreifen möchten.

## <a name="component-services-administrative-tool"></a>Verwaltungs Tool für Komponenten Dienste

Führen Sie die folgenden Schritte aus, um eine SOAP-fähige Anwendung von einem Server zu exportieren:

1.  Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste unter **Komponenten Dienste** den Ordner **com+-Anwendungen** , der dem Computer zugeordnet ist, den Sie verwalten möchten.

2.  Klicken Sie mit der rechten Maustaste auf die Komponente, die Sie als XML-Webdienst verfügbar machen möchten, und wählen Sie **exportieren** aus. Der **com+-Anwendungs Export-Assistent** wird angezeigt.

3.  Geben Sie im Textfeld mit **der Bezeichnung den vollständigen Pfad und Dateinamen für die zu erstellende Anwendungsdatei** ein. Geben Sie den vollständigen Pfad und Dateinamen für die MSI-Datei ein, die die exportierte Anwendung enthalten soll, oder klicken Sie auf **Durchsuchen** , um den vollständigen Pfad und Dateinamen

4.  Wählen Sie unter **Exportieren als** den **Anwendungs Proxy – auf anderen Computern installieren aus, um den Zugriff auf diesen Computer zu aktivieren** .

## <a name="visual-basic"></a>Visual Basic

Nicht anwendbar.

## <a name="cc"></a>C/C++

Nicht anwendbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über den COM+ SOAP-Dienst](com--soap-service-overview.md)
</dt> <dt>

[Erstellen von XML-Webdiensten](creating-xml-web-services.md)
</dt> <dt>

[Importieren einer SOAP-Enabled Anwendung](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



