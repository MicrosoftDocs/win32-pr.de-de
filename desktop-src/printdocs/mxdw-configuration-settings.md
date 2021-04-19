---
description: Mit dem Microsoft XPS Document Writer (MXDW) können Benutzer XPS-Dokument Dateien erstellen, indem Sie Sie aus jeder Windows-Anwendung drucken.
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: MXDW-Konfigurationseinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4026a99baa33ec50bc3ad129ef6610a428f83ab
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106366382"
---
# <a name="mxdw-configuration-settings"></a>MXDW-Konfigurationseinstellungen

Mit dem Microsoft XPS Document Writer (MXDW) können Benutzer XPS-Dokument Dateien erstellen, indem Sie Sie aus jeder Windows-Anwendung drucken. Anwendungsentwickler können die folgenden Ausgabeeinstellungen von MXDW mithilfe der PrintTicket-und Print-Funktionen des [Druck Schemas](./printschema.md)steuern.

## <a name="jobinterleaving"></a>Jobinterleaving

Die jobinterleaving-Einstellung steuert die Inhalts Austausch Reihenfolge für die XPS-Dokumente. Weitere Informationen zum Überschreiben von Aufträgen finden Sie in der [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf). MXDW unterstützt die folgenden beiden Optionen für diese Einstellung:

-   **Off** : bei dieser Option wird die Überlappungen deaktiviert, sodass alle Daten für jedes Inhalts Element im Dokument zusammenhängend sind, wodurch die Effizienz des zufälligen Zugriffs verbessert wird. Diese Option eignet sich am besten zum Anzeigen eines XPS-Dokuments.
-   **On** : diese Option ermöglicht das überlappen, sodass Daten für jedes Inhalts Element untergliedert und neu angeordnet werden, um eine effizientere sequenzielle Verarbeitung zu ermöglichen. Diese Option eignet sich am besten für das herunterladen und Drucken von Web.

Das folgende Beispiel ist ein Beispiel für die printfunktionen-XML-Datei, die die jobinterleaving-Einstellung enthält.


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



Die PrintTicket-XML-Datei ist ähnlich, mit der Ausnahme, dass Sie eine bestimmte Option angibt. Weitere Informationen finden Sie im [Druck Schema](./printschema.md) .

Da jobinterleaving nicht zu den [öffentlichen Schlüsselwörtern des Print-Schemas](./print-schema-public-keywords.md)gehört, müssen Sie eine Deklaration des Namespace (in diesem Fall "ns0000" im **Print-Funktionen** -Tag (oder **PrintTicket**) am Anfang des Printworks-Dokuments (oder PrintTicket) einschließen, wie im folgenden Beispiel gezeigt:


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a>Jobimagetype

Jobimagetype steuert das Ausgabeformat von eingebetteten Bitmapformaten. MXDW unterstützt die folgenden vier Optionen für diese Einstellung:

-   **Jpeghigh** : diese Option gibt das JPEG-Bild mit einer hohen Komprimierungs Ebene an. Diese Option erzeugt die kleinste Dateigröße, jedoch die niedrigste Bildqualität.
-   **Jpegmed** : diese Option gibt das JPEG-Bild mit mittlerer Komprimierungs Ebene an. Diese Option bietet ein optimales Gleichgewicht zwischen Dateigröße und Bildqualität.
-   **Jpeglow** : diese Option gibt das JPEG-Bild mit einer geringen Komprimierungs Ebene an. Mit dieser Option wird die Dateigröße und hohe Bildqualität am geringsten reduziert.
-   **PNG** : diese Option gibt das PNG-Bildformat mit Verlust loser Komprimierung an. Diese Option erzeugt die größte Dateigröße und die höchste Bildqualität.

Die printfunktionen-XML-Datei der Einstellung "jobimagetype" wird unten angezeigt:


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



Die PrintTicket-XML-Datei ist ähnlich, mit der Ausnahme, dass Sie eine bestimmte Option angibt. Weitere Informationen finden Sie im [Druck Schema](./printschema.md) .

Da jobimagetype kein öffentliches Schlüsselwort für den [Druck Schema](./print-schema-public-keywords.md)ist, müssen Sie eine Deklaration des Namespaces (in diesem Fall "ns0000" in das **Print-Funktionen** -Tag (oder **PrintTicket**) am Anfang des Printworks-Dokuments (oder PrintTicket) einschließen, wie im folgenden Beispiel gezeigt:


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

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[Druck Schema](./printschema.md)
</dt> <dt>

[XPS-Spezifikation und Lizenz Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
