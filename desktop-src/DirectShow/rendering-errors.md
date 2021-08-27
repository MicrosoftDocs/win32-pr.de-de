---
description: Renderingfehler
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Renderingfehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5af72ccf7ca76b2d4899178757282f1879c06052d2db2f3e1d929ddeef0f53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050610"
---
# <a name="rendering-errors"></a>Renderingfehler

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Microsoft® DirectShow® Editing Services (DES) definiert verschiedene Fehlercodes, die zum Protokollieren von Renderingfehlern verwendet werden. Wenn ein Projekt nicht ordnungsgemäß gerendert wird, ruft die Render-Engine die [**IAMErrorLog::LogError-Methode**](iamerrorlog-logerror.md) auf. In der folgenden Tabelle sind die parameter für **LogError** zusammengefasst:

-   Der Fehlercode ist im *ErrorCode-Parameter* enthalten.
-   Die Beschreibung ist im ErrorString-Parameter enthalten.
-   Die Beschreibung ist im *ErrorString-Parameter* enthalten.
-   Wenn zusätzliche Informationen vorhanden sind, ist der **VARIANT-Typ** im **vt-Member** des **VARIANT enthalten,** auf den *pExtraInfo* zeigt.

> [!Note]  
> Die hier beschriebenen Fehlercodes sind keine **HRESULT-Werte.** Eine Liste  der HRESULT-Rückgabewerte, die für DES spezifisch sind, finden Sie unter [Fehler- und Erfolgscodes.](error-and-success-codes.md)

 



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Fehlercode</th>
<th>BESCHREIBUNG</th>
<th>Zusätzliche Informationen</th>
<th>Varianttyp</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DEX_IDS_BAD_SOURCE_NAME</td>
<td>Der Dateiname ist nicht vorhanden, oder DirectShow erkennt die Dateierweiterung nicht.</td>
<td>Dateiname</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_BAD_SOURCE_NAME2</td>
<td>Der Dateityp stimmt nicht mit der Dateierweiterung überein, oder die Datei ist beschädigt.</td>
<td>Dateiname</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_MISSING_SOURCE_NAME</td>
<td>Der Dateiname war erforderlich, wurde jedoch nicht angegeben.</td>
<td>Keine</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="even">
<td>DEX_IDS_UNKNOWN_SOURCE</td>
<td>Die von dieser Quelle bereitgestellte Datenquelle kann nicht analysiert werden.</td>
<td>Keine</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INSTALL_PROBLEM</td>
<td>Unerwarteter Fehler. Einige DirectShow-Komponenten sind nicht ordnungsgemäß installiert.</td>
<td>Keine</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SOURCE_NAMES</td>
<td>Der Quellfilter akzeptiert keine Dateinamen.</td>
<td>Keine</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>DEX_IDS_BAD_MEDIATYPE</td>
<td>Der Medientyp der Gruppe wird nicht unterstützt.</td>
<td>Gruppennummer</td>
<td><strong>int</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_STREAM_NUMBER</td>
<td>Ungültige Streamnummer für diese Quelle.</td>
<td>Streamnummer</td>
<td><strong>int</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_OUTOFMEMORY</td>
<td>Nicht genügend Arbeitsspeicher.</td>
<td>Keine</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="even">
<td>DEX_IDS_DIBSEQ_NOTALLSAME</td>
<td>Eine Bitmap in der Sequenz war nicht der gleiche Typ wie die anderen.</td>
<td>Bitmapname</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_CLIPTOOSHORT</td>
<td>Die Medienzeiten des Clips sind ungültig, oder die Geräteunabhängige Bitmapsequenz (DIB) ist zu kurz.
<blockquote>
[!Note]<br />
Wenn andere Renderingfehler auftreten, kann dieser Fehler auftreten, obwohl die Medienzeiten gültig sind.
</blockquote>
<br/></td>
<td>Keine</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_DXT</td>
<td>Der Klassenbezeichner (CLSID) des Effekts oder Übergangs ist ungültig.</td>
<td>CLSID</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_DEFAULT_DXT</td>
<td>Die CLSID des Standardeffekts oder -übergangs ist ungültig.</td>
<td>CLSID</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_3D</td>
<td>Ihre DirectX-Version unterstützt keine dreidimensionalen Übergänge.</td>
<td>CLSID</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_BROKEN_DXT</td>
<td>Dieser Effekt ist nicht die richtige Art oder fehlerhaft.</td>
<td>CLSID</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SUCH_PROPERTY</td>
<td>Für das Objekt ist keine solche Eigenschaft vorhanden.</td>
<td>Eigenschaftenname</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_ILLEGAL_PROPERTY_VAL</td>
<td>Ungültiger Wert für diese Eigenschaft.</td>
<td>Angegebener Wert</td>
<td><strong>Variante</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_XML</td>
<td>Syntaxfehler in XML-Datei.</td>
<td>Zeilennummer</td>
<td>VT_I4 (4-Byte-Ganzzahl)</td>
</tr>
<tr class="odd">
<td>DEX_IDS_CANT_FIND_FILTER</td>
<td>Der in XML angegebene Filter kann nicht nach Kategorie und Instanz gefunden werden.</td>
<td>Anzeigename (Instanz)</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_DISK_WRITE_ERROR</td>
<td>Fehler beim Schreiben einer XML-Datei auf den Datenträger.</td>
<td>Keine</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_AUDIO_FX</td>
<td>CLSID ist kein gültiger DirectShow-Audioeffektfilter.</td>
<td>CLSID</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_CANT_FIND_COMPRESSOR</td>
<td>Es wurde kein Komprimierungsformat zum Erzeugen des angegebenen Komprimierungsformats finden.</td>
<td>Keine</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>



 

Die folgenden Fehler sollten nie auftreten. Wenn einer dieser Fehler angezeigt wird, senden Sie bitte einen Fehlerbericht an Microsoft.



| Fehlercode                 | BESCHREIBUNG                                 |
|----------------------------|---------------------------------------------|
| ANALYSE DER \_ DEX-IDS-ZEITACHSE \_ \_  | Unerwarteter Fehler beim Analyse der Zeitachse.      |
| \_ \_ DEX-IDS-GRAPHFEHLER \_     | Unerwarteter Fehler beim Erstellen des Filterdiagramms. |
| \_ \_ DEX-IDS-RASTERFEHLER \_      | Unerwarteter Fehler beim internen Raster.    |
| FEHLER BEI DER \_ DEX-IDS-SCHNITTSTELLE \_ \_ | Unerwarteter Fehler beim Abrufen einer Schnittstelle.      |



 

 

 




