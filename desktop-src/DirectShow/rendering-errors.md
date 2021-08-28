---
description: Renderingfehler
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Renderingfehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31d49c5fbb82457282decdaa07152e75db6bc3e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482586"
---
# <a name="rendering-errors"></a>Renderingfehler

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Microsoft® DirectShow® Editing Services (DES) definiert verschiedene Fehlercodes, die zum Protokollieren von Renderingfehlern verwendet werden. Wenn ein Projekt nicht ordnungsgemäß gerendert wird, ruft die Render-Engine die [**IAMErrorLog::LogError-Methode**](iamerrorlog-logerror.md) auf. In der folgenden Tabelle sind die Parameter zusammengefasst, die **LogError gegeben sind:**

-   Der Fehlercode ist im *ErrorCode-Parameter* enthalten.
-   Die Beschreibung ist im ErrorString-Parameter enthalten.
-   Die Beschreibung ist im *ErrorString-Parameter* enthalten.
-   Wenn zusätzliche Informationen verfügbar sind, ist der **VARIANT-Typ** im **vt-Member** des **VARIANT-Objekts** enthalten, auf das *pExtraInfo zeigt.*

> [!Note]  
> Die hier beschriebenen Fehlercodes sind keine **HRESULT-Werte.** Eine Liste der **HRESULT-Rückgabewerte,** die für DES spezifisch sind, finden Sie unter [Fehler- und Erfolgscodes](error-and-success-codes.md).

 




| Fehlercode | BESCHREIBUNG | Zusätzliche Informationen | Varianttyp | 
|------------|-------------|-------------------|--------------|
| DEX_IDS_BAD_SOURCE_NAME | Der Dateiname ist nicht vorhanden, oder DirectShow erkennt die Dateierweiterung nicht. | Dateiname | <strong>BSTR</strong> | 
| DEX_IDS_BAD_SOURCE_NAME2 | Der Dateityp passt nicht zur Dateierweiterung, oder die Datei ist beschädigt. | Dateiname | <strong>BSTR</strong> | 
| DEX_IDS_MISSING_SOURCE_NAME | Der Dateiname war erforderlich, wurde aber nicht angegeben. | Keine | Nicht zutreffend | 
| DEX_IDS_UNKNOWN_SOURCE | Die von dieser Quelle bereitgestellte Datenquelle kann nicht analysiert werden. | Keine | Nicht zutreffend | 
| DEX_IDS_INSTALL_PROBLEM | Unerwarteter Fehler. Einige DirectShow-Komponenten sind nicht ordnungsgemäß installiert. | Keine | Nicht zutreffend | 
| DEX_IDS_NO_SOURCE_NAMES | Der Quellfilter akzeptiert keine Dateinamen. | Keine | Nicht zutreffend | 
| DEX_IDS_BAD_MEDIATYPE | Der Medientyp der Gruppe wird nicht unterstützt. | Gruppennummer | <strong>int</strong> | 
| DEX_IDS_STREAM_NUMBER | Ungültige Streamnummer für diese Quelle. | Streamnummer | <strong>int</strong> | 
| DEX_IDS_OUTOFMEMORY | Nicht genügend Arbeitsspeicher. | Keine | Nicht zutreffend | 
| DEX_IDS_DIBSEQ_NOTALLSAME | Eine Bitmap in der Sequenz war nicht der gleiche Typ wie die anderen. | Bitmapname | <strong>BSTR</strong> | 
| DEX_IDS_CLIPTOOSHORT | Die Medienzeiten des Clips sind ungültig, oder die DIB-Sequenz (Device-Independent Bitmap) ist zu kurz.<blockquote>[!Note]<br />Wenn andere Renderingfehler auftreten, kann dieser Fehler auftreten, obwohl die Medienzeiten gültig sind.</blockquote><br /> | Keine | Nicht zutreffend | 
| DEX_IDS_INVALID_DXT | Der Klassenbezeichner (CLSID) des Effekts oder Übergangs ist ungültig. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_INVALID_DEFAULT_DXT | Die CLSID des Standardeffekts oder -übergangs ist ungültig. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_NO_3D | Ihre Version von DirectX unterstützt keine dreidimensionalen Übergänge. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_BROKEN_DXT | Dieser Effekt ist nicht die richtige Art oder ist beschädigt. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_NO_SUCH_PROPERTY | Für das Objekt ist keine solche Eigenschaft vorhanden. | Eigenschaftenname | <strong>BSTR</strong> | 
| DEX_IDS_ILLEGAL_PROPERTY_VAL | Ungültiger Wert für diese Eigenschaft. | Angegebener Wert | <strong>VARIANTE</strong> | 
| DEX_IDS_INVALID_XML | Syntaxfehler in der XML-Datei. | Zeilennummer | VT_I4 (4-Byte-Ganzzahl) | 
| DEX_IDS_CANT_FIND_FILTER | Der in XML angegebene Filter wurde nach Kategorie und Instanz nicht finden. | Benutzerfreundlich (Instanz) | <strong>BSTR</strong> | 
| DEX_IDS_DISK_WRITE_ERROR | Fehler beim Schreiben der XML-Datei auf den Datenträger. | Keine | Nicht zutreffend | 
| DEX_IDS_INVALID_AUDIO_FX | CLSID ist kein gültiger DirectShow-Audioeffektfilter. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_CANT_FIND_COMPRESSOR | Es kann kein Komprimierungsformat gefunden werden, um das angegebene Komprimierungsformat zu erzeugen. | Keine | Nicht zutreffend | 




 

Die folgenden Fehler sollten nie auftreten. Wenn einer dieser Fehler auftritt, senden Sie einen Fehlerbericht an Microsoft.



| Fehlercode                 | BESCHREIBUNG                                 |
|----------------------------|---------------------------------------------|
| ANALYSE \_ DER \_ DEX-IDS-ZEITACHSE \_  | Unerwarteter Fehler beim Analysieren der Zeitachse.      |
| \_ \_ DEX-IDS-DIAGRAMMFEHLER \_     | Unerwarteter Fehler beim Erstellen des Filterdiagramms. |
| \_ \_ DEX-IDS-RASTERFEHLER \_      | Unerwarteter Fehler beim internen Raster.    |
| \_ \_ DEX-IDS-SCHNITTSTELLENFEHLER \_ | Unerwarteter Fehler beim Abrufen einer Schnittstelle.      |



 

 

 




