---
description: Medienmetadaten
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Medienmetadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ce2ba0881dc37d9b026625961635eeaf4561bfe0d6dc37328e12451e1d8bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062233"
---
# <a name="media-metadata"></a>Medienmetadaten

Mediendateien enthalten Eigenschaften, die den Inhalt der Datei beschreiben. In Microsoft Media Foundation können diese Eigenschaften wie folgt kategorisiert werden:

-   **Medientypattribute** geben die Codierungsparameter an, z. B. den Codierungsalgorithmus (Medienuntertyp), die Videoframegröße, die Videobildrate, die Audiobitrate und die Audioabtastrate. Weitere Informationen zu Medientypattributen finden Sie unter [Medientypen.](media-types.md)
-   **Metadaten** enthalten beschreibende Informationen zu Medieninhalten wie Titel, Interpret, Composer und Genre. Metadaten können auch Codierungsparameter beschreiben. Es kann schneller sein, über Metadaten auf diese Informationen zuzugreifen als über Medientypattribute.
-   **DRM-Eigenschaften** enthalten Informationen zu Verwendungseinschränkungen. Derzeit unterstützt Media Foundation keine DRM-Eigenschaften über Metadaten, mit Ausnahme der **PKEY \_ DRM \_ IsProtected-Eigenschaft.**

Es gibt zwei Möglichkeiten, Metadaten in Media Foundation zu lesen:

-   DIE [**INTERFACESMetadata-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) (Media Foundation Metadaten der Version 1).
-   Die Windows [**Shell-IPropertyStore-Schnittstelle**](/windows/win32/api/propsys/nn-propsys-ipropertystore) (Shellmetadaten).

Shellmetadaten beziehen sich nicht nur auf Mediendateien, sondern auch auf einen viel größeren Bereich von Dateien auf dem System.

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
Shellmetadaten erfordern im Allgemeinen nicht Windows 7, aber Media Foundation haben shell-Metadaten vor Windows 7 nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Eigenschaften sind nicht mit dem Shell-Eigenschaftensystem kompatibel.</td>
<td>Eigenschaften sind mit dem Shell-Eigenschaftensystem kompatibel.</td>
</tr>
<tr class="odd">
<td>Eigenschaften können für die gesamte Datei oder auf Streamebene gelten.</td>
<td>Es werden nur Eigenschaften auf Dateiebene unterstützt. Eigenschaften auf Streamebene werden nicht unterstützt.</td>
</tr>
<tr class="even">
<td>Eigenschaften können Werte in mehreren Sprachen aufweisen.</td>
<td>Werte in mehreren Sprachen werden nicht unterstützt.</td>
</tr>
<tr class="odd">
<td>Eigenschaftsschlüssel sind Breitzeichenzeichenfolgen.</td>
<td>Eigenschaftsschlüssel sind <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY-Werte.</strong></a></td>
</tr>
<tr class="even">
<td>Eigenschaftswerte sind <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT-Werte.</strong></a></td>
<td>Eigenschaftswerte sind <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT-Werte.</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                     | BESCHREIBUNG                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Shellmetadatenanbieter](shell-metadata-providers.md)<br/>                       | Ab Windows 7 macht Media Foundation Metadaten über die [**IPropertyStore-Schnittstelle**](/windows/win32/api/propsys/nn-propsys-ipropertystore) verfügbar.<br/> |
| [Metadateneigenschaften für Mediendateien](metadata-properties-for-media-files.md)<br/> | In diesem Thema werden die gängigsten Metadateneigenschaften für Mediendateien aufgeführt.<br/>                                                           |
| [Metadatenanbieter in Windows Vista](metadata-providers-in-windows-vista.md)<br/> | In Windows Vista macht Media Foundation Metadaten über die [**INTERFACESMetadata-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) verfügbar.<br/>                   |



 

Wenn Sie eine benutzerdefinierte Medienquelle implementieren und Shellmetadaten verfügbar machen möchten, finden Sie weitere Informationen unter [Benutzerdefinierte Metadatenanbieter für Mediendateien.](custom-metadata-providers-for-media-files.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Programmierhandbuch](media-foundation-programming-guide.md)
</dt> </dl>

 

 
