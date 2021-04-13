---
description: Renderingfehler
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Renderingfehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e106a55363bf50e49a4966600662e26b03b53307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482235"
---
# <a name="rendering-errors"></a>Renderingfehler

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Microsoft® DirectShow® Bearbeitungs Dienste (des) definiert verschiedene Fehlercodes, die zum Protokollieren von renderingfehlern verwendet werden. Wenn ein Projekt nicht ordnungsgemäß gerengt wird, ruft die Renderingengine die [**iamerrorlog:: LogError**](iamerrorlog-logerror.md) -Methode auf. In der folgenden Tabelle werden die Parameter von **LogError** zusammengefasst:

-   Der Fehlercode ist im *errorCode* -Parameter enthalten.
-   Die Beschreibung ist im Parameter ErrorString enthalten.
-   Die Beschreibung ist im Parameter *ErrorString* enthalten.
-   Wenn zusätzliche Informationen vorliegen, ist der **Variant** -Typ im **VT** -Member der **Variante** enthalten, auf die von *pextrainfo* verwiesen wird.

> [!Note]  
> Die hier beschriebenen Fehlercodes sind keine **HRESULT** -Werte. Eine Liste der **HRESULT** -Rückgabewerte, die für des spezifisch sind, finden Sie unter [Fehler-und Erfolgs Codes](error-and-success-codes.md).

 



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
<td>Der Dateiname ist nicht vorhanden, oder die Dateierweiterung wird nicht von DirectShow erkannt.</td>
<td>Dateiname</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_BAD_SOURCE_NAME2</td>
<td>Der Dateityp entspricht nicht der Dateierweiterung, oder die Datei ist beschädigt.</td>
<td>Dateiname</td>
<td><strong>BSTR</strong></td>
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
<td>Der Quell Filter akzeptiert keine Dateinamen.</td>
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
<td>Ungültige streamnummer für diese Quelle.</td>
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
<td>Eine Bitmap in der Sequenz hatte nicht denselben Typ wie die anderen.</td>
<td>Bitmapname</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_CLIPTOOSHORT</td>
<td>Die Medien Zeiten des Clips sind ungültig, oder die geräteunabhängige Bitmap-Sequenz (DIB) ist zu kurz.
<blockquote>
[!Note]<br />
Wenn andere Renderingfehler auftreten, kann dieser Fehler auch dann auftreten, wenn die Medien Zeiten gültig sind.
</blockquote>
<br/></td>
<td>Keine</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_DXT</td>
<td>Der Klassen Bezeichner (CLSID) des Effekts oder Übergangs ist ungültig.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_DEFAULT_DXT</td>
<td>Die CLSID des Standard Effekts oder-Übergangs ist ungültig.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_3D</td>
<td>Die Version von DirectX unterstützt keine dreidimensionalen Übergänge.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_BROKEN_DXT</td>
<td>Dieser Effekt ist nicht die richtige Art oder ist beschädigt.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SUCH_PROPERTY</td>
<td>Für das Objekt ist keine solche Eigenschaft vorhanden.</td>
<td>Eigenschaftenname</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_ILLEGAL_PROPERTY_VAL</td>
<td>Ungültiger Wert für diese Eigenschaft.</td>
<td>Wert angegeben</td>
<td><strong>Konfigur</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_XML</td>
<td>Syntax Fehler in der XML-Datei.</td>
<td>Zeilennummer</td>
<td>VT_I4 (ganze 4-Byte-Zahl)</td>
</tr>
<tr class="odd">
<td>DEX_IDS_CANT_FIND_FILTER</td>
<td>Der in XML angegebene Filter wurde nach Kategorie und Instanz nicht gefunden.</td>
<td>Anzeige Name (Instanz)</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_DISK_WRITE_ERROR</td>
<td>Fehler beim Schreiben der XML-Datei auf den Datenträger.</td>
<td>Keine</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_AUDIO_FX</td>
<td>CLSID ist kein gültiger DirectShow-Audioeffekt-Filter.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_CANT_FIND_COMPRESSOR</td>
<td>Es wurde kein Kompressor gefunden, der das angegebene Komprimierungs Format erzeugt.</td>
<td>Keine</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>



 

Die folgenden Fehler sollten nie auftreten. Wenn einer dieser Fehler auftritt, senden Sie einen Fehlerbericht an Microsoft.



| Fehlercode                 | BESCHREIBUNG                                 |
|----------------------------|---------------------------------------------|
| Index- \_ IDs- \_ Zeitachse \_ analysieren  | Unerwarteter Fehler beim Auswerten der Zeitachse.      |
| Fehler im DEX- \_ IDs- \_ Diagramm \_     | Unerwarteter Fehler beim Aufbau des Filter Diagramms. |
| Fehler bei DEX- \_ IDs- \_ Raster \_      | Unerwarteter Fehler beim internen Raster.    |
| \_Schnittstellen-IDs- \_ Schnittstellen \_ Fehler | Unerwarteter Fehler beim erhalten einer Schnittstelle.      |



 

 

 




