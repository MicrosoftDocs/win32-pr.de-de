---
description: Das konzeptionelle Modell
ms.assetid: f906466e-acdc-4d0f-bf27-c5a25dc56c01
title: Das konzeptionelle Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a653d3658e0785fcc729be335fc4d648ea9bc91af676678aece0c43ce046f419
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806550"
---
# <a name="the-conceptual-model"></a>Das konzeptionelle Modell

In diesem Abschnitt werden die Objekte, Eigenschaften und Ressourcen beschrieben, die das WPD-Konzeptionelle Modell bilden.

### <a name="objects"></a>Objekte

In WPD werden logische Entitäten auf Geräten als Objekte bezeichnet. In der Regel, aber nicht immer, stellen diese Daten auf dem Gerät dar. Objekte verfügen über Eigenschaften und werden von Objektbezeichnern referenziert. Beispiele für Objekte sind Bilder und Ordner auf einer Kamera, Titel und Wiedergabelisten auf einem Media Player, Kontakte auf einem Mobiltelefon usw.

Objekte können auch funktionale oder informationsbedingte Teile des Geräts darstellen. Beispiele hierfür sind Player-Steuerelemente (Wiedergabe/Aufzeichnung/Pause), Kameraeinstellungen, SMS-Funktionen eines Mobiltelefons usw.

Die beiden folgenden Themen enthalten Beispiele und Abbildungen von zwei Objekttypen: das Image-Objekt und das Mediacast-Objekt.

### <a name="image-object"></a>Image-Objekt

Ein Bildobjekt stellt ein Standbild dar. Das folgende Diagramm zeigt die Beziehungen zwischen einem Image-Objekt, seinen Eigenschaften und seinen Ressourcen.

![Diagramm eines wpd-Objekts und seiner Beziehung zu seinen Eigenschaften und Ressourcen](images/wpd-overview-figure2.gif)

Weitere Informationen zum Image-Objekt und seinen Eigenschaften finden Sie im Thema [**WPD \_ CONTENT TYPE \_ \_ IMAGE.**](wpd-content-type-image.md)

### <a name="mediacast-object"></a>Mediacast-Objekt

Ein Mediacast-Objekt kann als Containerobjekt bezeichnet werden, das verwandte Inhalte gruppiert, ebenso wie eine Wiedergabeliste Musik gruppiert. Häufig wird ein Mediacast-Objekt verwendet, um Medieninhalte zu gruppieren, die online veröffentlicht wurden. Beispielsweise kann ein RSS-Kanal als Mediacast-Objekt dargestellt werden, dessen Objektverweise auf Inhaltsobjekte verweisen, die jedes Element im Kanal darstellen. Das folgende Diagramm zeigt die Beziehung zwischen einem Mediacast-Objekt und den drei darin enthaltenen Audioobjekten.

![Diagramm, das die hierarchische Struktur eines 1000-Objekts und drei darin enthaltener Objekte zeigt](images/mediacast1.gif)

Die Verweise auf das Audioobjekt werden in der [WPD \_ OBJECT \_ REFERENCES-Eigenschaft](object-properties.md) für das Mediacast-Objekt angegeben. Weitere Informationen zu den eigenschaften, die von einem Mediacast-Objekt unterstützt werden, finden Sie im Thema [**WPD \_ CONTENT TYPE \_ MEDIA \_ \_ CAST.**](wpd-content-type-media-cast.md)

### <a name="properties"></a>Eigenschaften

Objekteigenschaften stellen einen Mechanismus zum Austauschen objektbeschreibender Metadaten bereit. Beispielsweise kann ein Bildobjekt Eigenschaften enthalten, die den Dateinamen, die Größe, das Format, die Breite in Pixel usw. beschreiben.

Eigenschaften haben einen aktuellen Wert sowie Attribute. WPD definiert eine Reihe von Standardeigenschaften, aus denen die API- und DDI-Definitionen besteht. Anbieter sind nicht auf die vordefinierten WPD-Eigenschaften beschränkt und können eigene hinzufügen.

### <a name="property-attributes"></a>Eigenschaftenattribute

Eigenschaftenattribute beschreiben die Zugriffsrechte, gültigen Werte und andere Informationen im Zusammenhang mit einer Eigenschaft. Die Eigenschaft, die die Bitrate darstellt, kann beispielsweise einen Bereich von 8 Kilobits pro Sekunde (KBit/s) bis 20 KBit/s mit einem Schrittwert von 1 KBit/s aufweisen.

Zugriffsrechte geben an, ob Aufrufer die Eigenschaft lesen, schreiben und/oder löschen können. Gültige Werte geben Einschränkungen für Eigenschaftswerte an. Gültige Werte werden als von einem bestimmten Format bezeichnet. Gültige Wertformulare sind Range (d. h. die Eigenschaft kann einen Wert von Min bis Max mit dem angegebenen Schritt annehmen), Enumeration (d. h. der Eigenschaftswert ist einer der Werte in der angegebenen Liste) und None (d. h. es gibt keine spezifischen gültigen Werte).

### <a name="resources"></a>Ressourcen

Ressourcen sind Platzhalter für Binärdaten. Ein Objekt kann über mehrere Ressourcen verfügen. Wenn das Objekt beispielsweise eine Bilddatei mit einer Audioanmerkung darstellt, können die Ressourcen für dieses Objekt wie folgt aussehen:

-   Eine Standardressource. Diese Ressource stellt die gesamte Imagedatei dar. (Dies schließt alle eingebetteten Daten ein, z. B. Audioanmerkungen, Miniaturansichten usw.)
-   Eine Miniaturansichtsressource. Diese Ressource stellt die Miniaturansichtsdaten für das Bild dar.
-   Eine Audioanmerkungsressource. Diese Ressource stellt die dem Bild zugeordneten Audiodaten dar.

### <a name="resource-attributes"></a>Ressourcenattribute

Ähnlich wie Eigenschaftsattribute beschreiben Ressourcenattribute die Zugriffsrechte, die Größe, das Format und andere Informationen im Zusammenhang mit einer Ressource. Beispielsweise können die Attribute für eine Audioanmerkungsressource in einem Bildobjekt die Bitrate, die Kanalanzahl und das Datenformat des Audios angeben.

### <a name="rendering-profiles-and-resource-attributes"></a>Rendern von Profilen und Ressourcenattributen

Das Renderingprofil ist eine Methode, mit der Anwendungen die gültigen Attribute für eine bestimmte Ressource ermitteln. Ein Mobiltelefon kann z. B. Bitmaps mit bestimmten Einschränkungen für die Minimal- und Höchstwerte für Breite und Höhe unterstützen. Durch Abfragen der Renderingprofile für das Bitmapobjekt kann eine Anwendung diese genauen Werte abrufen.

Die folgende Beispielausgabe identifiziert die Renderingprofilinformationen, die das Gerät zurückgeben würde, wenn es Bitmaps mit einer Mindesthöhe von 10 Pixeln, einer Mindestbreite von 20 Pixeln, einer maximalen Höhe von 1000 Pixeln und einer maximalen Breite von 2000 Pixeln unterstützt.


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



Eine Beschreibung, wie Ihre Anwendung ein Renderingprofil (und die zugehörigen Ressourcenattribute) abrufen kann, finden Sie im Thema Abrufen der [von einem Gerät unterstützten Renderingfunktionen](retrieving-the-rendering-capabilities-supported-by-a-device.md) im Programmierhandbuch.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anwendungsübersicht**](application-overview.md)
</dt> </dl>

 

 



