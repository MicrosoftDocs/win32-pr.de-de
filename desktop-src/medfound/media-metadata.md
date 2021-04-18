---
description: Medien Metadaten
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Medien Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb17f286673663976e17b4178239507765c2101
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106365000"
---
# <a name="media-metadata"></a>Medien Metadaten

Mediendateien enthalten Eigenschaften, die den Inhalt der Datei beschreiben. In Microsoft Media Foundation können diese Eigenschaften wie folgt kategorisiert werden:

-   **Medientyp Attribute** geben die Codierungs Parameter an, z. b. den Codierungs Algorithmus (Medien Untertyp), Video Frame Größe, Video Frame Rate, Audiobitrate und audiobeispielrate. Weitere Informationen zu Medientyp Attributen finden Sie unter [Medientypen](media-types.md).
-   **Metadaten** enthalten beschreibende Informationen für den Medieninhalt, z. b. Titel, Interpret, Composer und Genre. Metadaten können auch Codierungs Parameter beschreiben. Es kann schneller sein, über Metadaten auf diese Informationen zuzugreifen, als mithilfe von Medientyp Attributen.
-   **DRM-Eigenschaften** enthalten Informationen zu Nutzungseinschränkungen. Derzeit werden von Media Foundation keine DRM-Eigenschaften durch Metadaten unterstützt, mit Ausnahme der **pkey DRM-Eigenschaft \_ \_ IsProtected** .

Es gibt zwei Möglichkeiten, Metadaten in Media Foundation zu lesen:

-   Die [**IMF Metadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) -Schnittstelle (Media Foundation Metadaten der Version 1).
-   Die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle von Windows Shell (shellmetadaten).

Shellmetadaten beziehen sich nicht nur auf Mediendateien, sondern auf eine viel größere Anzahl von Dateien auf dem System.

In der folgenden Tabelle werden die Features und Einschränkungen der einzelnen Metadaten-APIs verglichen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Media Foundation v1-Metadaten</th>
<th>Shellmetadaten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Erfordert Windows Vista oder höher.</td>
<td>Erfordert Windows 7.
<blockquote>
[!Note]<br />
Shell-Metadaten im Allgemeinen erfordern nicht Windows 7, aber Media Foundation keine shellmetadaten vor Windows 7 unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Eigenschaften sind nicht mit dem shelleigenschaftensystem kompatibel.</td>
<td>Eigenschaften sind mit dem shelleigenschaftensystem kompatibel.</td>
</tr>
<tr class="odd">
<td>Eigenschaften können auf die gesamte Datei oder auf Streamebene angewendet werden.</td>
<td>Es werden nur Eigenschaften auf Dateiebene unterstützt. Eigenschaften auf Streamebene werden nicht unterstützt.</td>
</tr>
<tr class="even">
<td>Eigenschaften können über Werte in mehreren Sprachen verfügen.</td>
<td>Werte in mehreren Sprachen werden nicht unterstützt.</td>
</tr>
<tr class="odd">
<td>Eigenschafts Schlüssel sind Zeichen folgen mit breit Zeichen.</td>
<td>Eigenschafts Schlüssel sind <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PropertyKey</strong></a> -Werte.</td>
</tr>
<tr class="even">
<td>Eigenschaftswerte sind <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> -Werte.</td>
<td>Eigenschaftswerte sind <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> -Werte.</td>
</tr>
</tbody>
</table>



 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                     | BESCHREIBUNG                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Shellmetadatenanbieter](shell-metadata-providers.md)<br/>                       | Ab Windows 7 macht Media Foundation Metadaten über die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle verfügbar.<br/> |
| [Metadateneigenschaften für Mediendateien](metadata-properties-for-media-files.md)<br/> | In diesem Thema werden die gängigsten Metadateneigenschaften für Mediendateien aufgelistet.<br/>                                                           |
| [Metadatenanbieter in Windows Vista](metadata-providers-in-windows-vista.md)<br/> | In Windows Vista macht Media Foundation Metadaten über die [**IMF Metadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) -Schnittstelle verfügbar.<br/>                   |



 

Wenn Sie eine benutzerdefinierte Medienquelle implementieren und shellmetadaten verfügbar machen möchten, finden Sie unter [benutzerdefinierte Metadatenanbieter für Mediendateien](custom-metadata-providers-for-media-files.md)Weitere Informationen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Programmier Handbuch](media-foundation-programming-guide.md)
</dt> </dl>

 

 
