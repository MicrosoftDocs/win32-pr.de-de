---
description: Mit dem Microsoft XPS Document Writer (MXDW) können Benutzer XPS-Dokumentdateien erstellen, indem sie aus einer beliebigen Windows drucken.
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: MXDW-Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a75d45ea3ad9c8c74280d1e70e418ee0bf4823d1f0332e3d5c772d29976cf2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971189"
---
# <a name="mxdw-configuration-settings"></a>MXDW-Einstellungen

Mit dem Microsoft XPS Document Writer (MXDW) können Benutzer XPS-Dokumentdateien erstellen, indem sie aus einer beliebigen Windows drucken. Anwendungsentwickler können die folgenden Ausgabeeinstellungen des MXDW mithilfe der PrintTicket- und PrintCapabilities-Teile des [Druckschemas steuern.](./printschema.md)

## <a name="jobinterleaving"></a>JobInterleaving

Die JobInterleaving-Einstellung steuert die Reihenfolge der zwischengespeicherten Inhalte für die XPS-Dokumente. Informationen zur Überlappung von Aufgaben finden Sie im [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf). MXDW unterstützt die folgenden beiden Optionen für diese Einstellung:

-   **Off:** Diese Option deaktiviert die Überlappung, sodass alle Daten für jedes Inhaltselement im Dokument zusammenhängend sind, wodurch die Effizienz des zufälligen Zugriffs verbessert wird. Diese Option ist am besten zum Anzeigen eines XPS-Dokuments.
-   **Ein:** Diese Option ermöglicht die Überlappung, sodass die Daten für jedes Inhaltselement aufgebrochen und neu angeordnet werden, um eine effizientere sequenzielle Verarbeitung zu ermöglichen. Diese Option ist am besten für Webdownloads und -drucke.

Das folgende Beispiel ist ein Beispiel für printCapabilities XML, das die JobInterleaving-Einstellung enthält.


```XML
<psf:Feature name="ns0000:JobInterleaving">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Interleaving</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:OFF" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">Off - Best for viewing</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:ON" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">On - Best for the web/printing</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



Die PrintTicket XML-Datei ist ähnlich, mit der Ausnahme, dass sie eine bestimmte Option angibt. Weitere Informationen finden [Sie unter Druckschema.](./printschema.md)

Da JobInterleaving nicht zu den öffentlichen Schlüsselwörtern des Druckschemas [gehört,](./print-schema-public-keywords.md)müssen Sie eine Deklaration des Namespace (in diesem Fall "ns0000" im **PrintCapabilities-Tag** (oder **PrintTicket)** am Anfang des PrintCapabilities-Dokuments (oder PrintTicket) hinzufügen, wie im folgenden Beispiel gezeigt:


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a>JobImageType

JobImageType steuert das Ausgabeformat eingebetteter Bitmapformate. MXDW unterstützt die folgenden vier Optionen für diese Einstellung:

-   **JPEGHigh:** Diese Option gibt das JPEG-Bild mit einem hohen Komprimierungsgrad an. Diese Option erzeugt die kleinste Dateigröße, aber die niedrigste Bildqualität.
-   **JPEGMed:** Diese Option gibt das JPEG-Bild mit einer mittleren Komprimierungsebene an. Diese Option bietet das beste Gleichgewicht zwischen Dateigröße und Imagequalität.
-   **JPEGLow:** Diese Option gibt das JPEG-Bild mit geringer Komprimierung an. Diese Option führt zu einer geringsten Verringerung der Dateigröße und hoher Qualität.
-   **PNG:** Diese Option gibt das PNG-Bildformat mit verlustfreier Komprimierung an. Diese Option erzeugt die größte Dateigröße und die höchste Imagequalität.

Die PrintCapabilities-XML-Datei der JobImageType-Einstellung wird unten angezeigt:


```XML
<psf:Feature name="ns0000:JobImageType">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Images</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:JPEGHigh" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Maximum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGMed" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
        <psf:Value xsi:type="xsd:string">JPG - Medium compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGLow" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Minimum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:PNG" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">PNG - Lossless compression</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



Die PrintTicket XML-Datei ist ähnlich, mit der Ausnahme, dass sie eine bestimmte Option angibt. Weitere Informationen finden [Sie unter Druckschema.](./printschema.md)

Da JobImageType nicht zu den öffentlichen Schlüsselwörtern des Druckschemas [gehört,](./print-schema-public-keywords.md)müssen Sie eine Deklaration des Namespace (in diesem Fall "ns0000" im **PrintCapabilities-Tag** (oder **PrintTicket)** am Anfang des PrintCapabilities-Dokuments (oder PrintTicket) hinzufügen, wie im folgenden Beispiel gezeigt:


```XML
<psf:PrintTicket 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[Druckschema](./printschema.md)
</dt> <dt>

[XPS-Spezifikation und Lizenzdownloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
