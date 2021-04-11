---
description: Das konzeptionelle Modell
ms.assetid: f906466e-acdc-4d0f-bf27-c5a25dc56c01
title: Das konzeptionelle Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a17538e7fdb454fa8eb61ab951a3316b0f0c327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217505"
---
# <a name="the-conceptual-model"></a>Das konzeptionelle Modell

In diesem Abschnitt werden die Objekte, Eigenschaften und Ressourcen beschrieben, die das konzeptionelle WPD-Modell bilden.

### <a name="objects"></a>Objekte

In WPD werden logische Entitäten auf Geräten als Objekte bezeichnet. In der Regel, aber nicht immer, stellen diese Daten auf dem Gerät dar. -Objekte verfügen über Eigenschaften, auf die von Objekt bezeichmern verwiesen wird. Beispiele für Objekte sind Bilder und Ordner auf einer Kamera, Lieder und Wiedergabelisten auf einem Media Player, Kontakte auf einem Mobiltelefon usw.

Objekte können auch Funktions-oder Informationsteile des Geräts darstellen. Beispiele hierfür sind Player-Steuerelemente (Wiedergabe/Aufzeichnung/Pause), Kameraeinstellungen, SMS-Funktionen eines Mobiltelefons usw.

Die beiden folgenden Themen beschreiben Beispiele und Abbildungen zweier Objekttypen: das Image-Objekt und das Mediacast-Objekt.

### <a name="image-object"></a>Image-Objekt

Ein Image-Objekt stellt ein Image dar. Das folgende Diagramm zeigt die Beziehungen zwischen einem Bild Objekt, seinen Eigenschaften und den zugehörigen Ressourcen.

![Diagramm, das ein WPD-Objekt und seine Beziehung zu seinen Eigenschaften und Ressourcen anzeigt](images/wpd-overview-figure2.gif)

Weitere Informationen zum Image-Objekt und dessen Eigenschaften finden Sie im Thema [**WPD \_ - \_ Inhaltstyp \_ Image**](wpd-content-type-image.md) .

### <a name="mediacast-object"></a>Mediacast-Objekt

Ein Mediacast-Objekt kann als Container Objekt betrachtet werden, das verwandte Inhalte gruppiert, ebenso wie eine Wiedergabeliste Musik gruppiert. Häufig wird ein Mediacast-Objekt verwendet, um Medieninhalte zu gruppieren, die Online veröffentlicht wurden. Beispielsweise kann ein RSS-Kanal als Mediacast-Objekt dargestellt werden, dessen Objekt Verweise auf Inhalts Objekte verweisen, die jedes Element im Kanal darstellen. Das folgende Diagramm zeigt die Beziehung zwischen einem Mediacast-Objekt und den darin enthaltenen drei Audioobjekten.

![Diagramm mit der hierarchischen Struktur eines medicast-Objekts und drei darin enthaltenen Objekten](images/mediacast1.gif)

Die Verweise auf das Audioobjekt werden in der [WPD- \_ Objekt \_ Verweis](object-properties.md) Eigenschaft für das Mediacast-Objekt angegeben. Weitere Informationen zu den Eigenschaften, die von einem Mediacast-Objekt unterstützt werden, finden Sie im Thema zum [**WPD- \_ \_ Inhaltstyp \_ Media \_ Cast**](wpd-content-type-media-cast.md) .

### <a name="properties"></a>Eigenschaften

Objekteigenschaften bieten einen Mechanismus zum Austauschen von Objekt beschreibenden Metadaten. Ein Image-Objekt kann z. b. Eigenschaften enthalten, die den Dateinamen, die Größe, das Format, die Breite in Pixel usw. beschreiben.

Eigenschaften verfügen über einen aktuellen Wert sowie über Attribute. WPD definiert einen Satz von Standardeigenschaften, die die API-und DDI-Definitionen bilden. Anbieter sind nicht auf die vordefinierten WPD-Eigenschaften beschränkt und können Ihre eigenen Eigenschaften hinzufügen.

### <a name="property-attributes"></a>Eigenschaftenattribute

Eigenschafts Attribute beschreiben die Zugriffsrechte, gültige Werte und andere Informationen, die sich auf eine Eigenschaft beziehen. Beispielsweise könnte die Eigenschaft, die die Bitrate darstellt, ein Bereich von 8 kbit pro Sekunde (Kbit/s) bis 20 kbit/s mit einem Schrittwert von 1 Kbit/s sein.

Zugriffsrechte geben an, ob Aufrufer die Eigenschaft lesen, schreiben und/oder löschen können. Gültige Werte geben Einschränkungen für Eigenschaftswerte an. Gültige Werte werden als ein bestimmtes Formular bezeichnet. Gültige Wert Formulare enthalten den Bereich (d. h. die Eigenschaft kann einen Wert von "min" auf "Max" mit dem angegebenen Schritt annehmen), die Enumeration (der Eigenschafts Wert ist einer der in der angegebenen Liste) und "None" (d. h. es sind keine spezifischen gültigen Werte vorhanden).

### <a name="resources"></a>Ressourcen

Ressourcen sind Platzhalter für Binärdaten. Ein Objekt kann mehr als eine Ressource aufweisen. Wenn das Objekt z. b. eine Bilddatei mit einer Audioanmerkung darstellt, können die Ressourcen für dieses Objekt wie folgt lauten:

-   Eine Standardressource. Diese Ressource stellt die gesamte Bilddatei dar. (Dies schließt alle eingebetteten Daten ein, z. b. Audioanmerkungen, Miniaturansichten usw.)
-   Eine Miniatur Ansichts Ressource. Diese Ressource stellt die Miniaturansicht für das Bild dar.
-   Eine audioannotation-Ressource. Diese Ressource stellt die Audiodaten dar, die dem Bild zugeordnet sind.

### <a name="resource-attributes"></a>Ressourcen Attribute

Ähnlich wie Eigenschafts Attribute beschreiben Ressourcen Attribute die Zugriffsrechte, die Größe, das Format und andere Informationen zu einer Ressource. Beispielsweise können die Attribute für eine audioannotation-Ressource auf einem Image-Objekt die Bitrate, die Kanalanzahl und das Datenformat der Audiodatei angeben.

### <a name="rendering-profiles-and-resource-attributes"></a>Renderingprofile und Ressourcen Attribute

Das renderingprofil ist eine Methode, die von Anwendungen verwendet wird, um die gültigen Attribute für eine bestimmte Ressource zu ermitteln. Ein Mobiltelefon kann z. b. Bitmaps mit spezifischen Einschränkungen der minimalen und maximalen Width-und Height-Werte unterstützen. Durch Abfragen der renderingprofile für das Bitmap-Objekt kann eine Anwendung diese exakten Werte abrufen.

Die folgende Beispielausgabe identifiziert die renderingprofilinformationen, die das Gerät zurückgeben würde, wenn es Bitmaps mit einer Mindesthöhe von 10 Pixeln, eine minimale Breite von 20 Pixeln, eine maximale Höhe von 1000 Pixel und eine maximale Breite von 2000 Pixel unterstützt.


```C++
WPD_OBJECT_FORMAT = WPD_OBJECT_FORMAT_BMP
WPD_MEDIA_HEIGHT:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  10
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  10 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_MEDIA_WIDTH:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX =  2000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE = 0
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  2000 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
```



Eine Beschreibung, wie Ihre Anwendung ein renderingprofil (und die zugehörigen Ressourcen Attribute) abrufen kann, finden Sie im Thema zum Abrufen [der von einem Gerät unterstützten Renderingfunktionen](retrieving-the-rendering-capabilities-supported-by-a-device.md) im-Programmier Handbuch.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anwendungs Übersicht**](application-overview.md)
</dt> </dl>

 

 



