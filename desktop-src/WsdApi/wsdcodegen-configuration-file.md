---
description: Beschreibt die wsdcodegen-Konfigurationsdatei.
ms.assetid: 6dc340db-221e-4389-ba76-9f189f91866b
title: Wsdcodegen-Konfigurationsdatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8c252c5361fda411e2b7eca4f906ba92085a552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130952"
---
# <a name="wsdcodegen-configuration-file"></a>Wsdcodegen-Konfigurationsdatei

Eine wsdcodegen-Konfigurationsdatei wird normalerweise vom wsdcodegen-Tool generiert. Sie können Konfigurationsdateien manuell erstellen, aber die Komplexität und die Länge der Datei führen in der Regel dazu, dass die Hand Codierung nicht durchführen wird. Wir empfehlen dringend die Verwendung von wsdcodegen, um die Datei zu generieren. Weitere Informationen zum Erstellen von Konfigurationsdateien finden Sie unter Verwenden der Befehlszeilen Syntax von [wsdcodegen](using-wsdcodegen.md) und [wsdcodegen](wsdcodegen-command-line-syntax.md).

Sie sollten die generierte Konfigurationsdatei überprüfen und ggf. ändern, bevor Sie Sie zum Erstellen von Quellcode verwenden. Die von wsdcodegen generierte Konfigurationsdatei reicht in der Regel für die meisten Client Entwicklungen aus.

Um die Konfigurationsdatei für die Serverentwicklung zu verwenden, sind einige Änderungen erforderlich. Wenn das Hosting aktiviert ist (d. h., wenn der Modus "All" oder "Host" ausgewählt ist), ändern Sie den Inhalt des [**thismodelmetadata**](thismodelmetadata.md) -Elements und seiner untergeordneten Elemente nach Bedarf. Ändern oder entfernen Sie außerdem die Elemente [**pnpxde vicecategory**](/windows/desktop/WsdApi/pnpxdevicecategory), [**pnpxhardwareid**](pnpxhardwareid.md)und [**pnpxcompatibleid**](/windows/desktop/WsdApi/pnpxcompatibleid) im **thismodelmetadata** -Element oder die [**gehosteten**](hosted.md) Elemente nach Bedarf.

Eine Konfigurationsdatei besteht aus einer Sequenz von Elementen, die Eingabedaten für die Codegenerierung bereitstellen, gefolgt von einer beliebigen Anzahl von [**Datei**](file.md) Elementen, die die zu generierenden Dateien beschreiben. Eingabedaten enthalten einige globale Eigenschaften und Verweise auf Typen, die in WSDL, XSD und verwalteten Assemblys ausgedrückt werden. Text und CDATA in **Datei** Elementen werden ohne Änderung in die generierten Dateien geschrieben. Andere Elemente in **Datei** Elementen werden in den generierten Dateien durch generierten Code ersetzt.

XML-Konfigurationsdateien müssen einigen allgemeinen Regeln folgen, damit Sie ordnungsgemäß für die Verwendung mit dem Code Generator-Hilfsprogramm formatiert werden können. Diese lauten wie folgt:

-   Das Stamm Element einer beliebigen Konfigurationsdatei ist [**wsdcodegen**](wsdcodegen.md).

-   Elemente, die einfache Datentypen enthalten, sind mit Attributen austauschbar. Beispiel:

    ``` syntax
    <wsdCodeGen>
        <layerNumber>1</layerNumber>
    </wsdCodeGen>
    ```

    entspricht:

    ``` syntax
    <wsdCodeGen layerNumber="1"/>
    ```

-   Im Allgemeinen gibt es keine Einschränkung für die Reihenfolge von Elementen. Beispiel:

    ``` syntax
    <wsdCodeGen>
        <layerNumber>1</layerNumber>
        <layerPrefix>MEDIA_</layerPrefix>
    </wsdCodeGen>
    ```

    entspricht:

    ``` syntax
    <wsdCodeGen>
        <layerPrefix>MEDIA_</layerPrefix>
        <layerNumber>1</layerNumber>
    </wsdCodeGen>
    ```

    Der Code-Generator verarbeitet die Konfigurationsdatei jedoch in einem einzigen Durchlauf, und die Reihenfolge hat eine gewisse Relevanz. Beispielsweise müssen [**Datei**](file.md) Elemente, die Code im Zusammenhang mit einem bestimmten Porttyp generieren, nach dem Element auftreten, das den Code-Generator anweist, den Porttyp Vertrag zu lesen.

Eine umfassende Liste der Elemente, die in wsdcodegen-Konfigurationsdateien verwendet werden, finden Sie unter [wsdcodegen Configuration File XML Reference](wsdcodegen-configuration-file-xml-reference.md).

Beispiel Konfigurationsdateien sind im Windows SDK enthalten. Weitere Informationen finden Sie unter [WSDAPI Samples](wsdapi-samples.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu wsdcodegen](about-wsdcodegen.md)
</dt> <dt>

[WSDAPI-Beispiele](wsdapi-samples.md)
</dt> </dl>

 

 
