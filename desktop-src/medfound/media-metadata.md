---
description: Medienmetadaten
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Medienmetadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ef9f8a852bbce2dfb8d38a5883acc219cde8019
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477085"
---
# <a name="media-metadata"></a>Medienmetadaten

Mediendateien enthalten Eigenschaften, die den Inhalt der Datei beschreiben. In Microsoft Media Foundation können diese Eigenschaften wie folgt kategorisiert werden:

-   **Medientypattribute** geben die Codierungsparameter an, z. B. den Codierungsalgorithmus (Medienuntertyp), die Videoframegröße, die Videobildrate, die Audiobitrate und die Audio-Abtastrate. Weitere Informationen zu Medientypattributen finden Sie unter [Medientypen.](media-types.md)
-   **Metadaten** enthalten beschreibende Informationen für den Medieninhalt, z. B. Titel, Interpret, Composer und Genre. Metadaten können auch Codierungsparameter beschreiben. Es kann schneller sein, über Metadaten auf diese Informationen zu zugreifen als über Medientypattribute.
-   **DRM-Eigenschaften** enthalten Informationen zu Nutzungseinschränkungen. Derzeit Media Foundation keine DRM-Eigenschaften über Metadaten unterstützt, mit Ausnahme der **PKEY \_ DRM \_ IsProtected-Eigenschaft.**

Es gibt zwei Möglichkeiten zum Lesen von Metadaten in Media Foundation:

-   Die [**BENUTZEROBERFLÄCHEMetadata-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) (Media Foundation Metadaten der Version 1).
-   Die Windows [**Shell-IPropertyStore-Schnittstelle**](/windows/win32/api/propsys/nn-propsys-ipropertystore) (Shellmetadaten).

Shellmetadaten beziehen sich nicht nur auf Mediendateien, sondern auch auf einen viel größeren Bereich von Dateien im System.

In der folgenden Tabelle werden die Features und Einschränkungen der einzelnen Metadaten-APIs verglichen.




| Media Foundation v1-Metadaten | Shellmetadaten | 
|------------------------------|----------------|
| Erfordert Windows Vista oder höher. | Erfordert Windows 7.<blockquote>[!Note]<br />Shellmetadaten erfordern im Allgemeinen keine Windows 7, aber Media Foundation shell metadata did not support Shell metadata prior to Windows 7.</blockquote><br /> | 
| Eigenschaften sind nicht mit dem Shell-Eigenschaftensystem kompatibel. | Eigenschaften sind mit dem Shell-Eigenschaftensystem kompatibel. | 
| Eigenschaften können auf die gesamte Datei oder auf Streamebene angewendet werden. | Nur Eigenschaften auf Dateiebene werden unterstützt. Eigenschaften auf Streamebene werden nicht unterstützt. | 
| Eigenschaften können Werte in mehreren Sprachen enthalten. | Werte in mehreren Sprachen werden nicht unterstützt. | 
| Eigenschaftsschlüssel sind Breitzeichenzeichenfolgen. | Eigenschaftsschlüssel sind <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY-Werte.</strong></a> | 
| Eigenschaftswerte sind <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT-Werte.</strong></a> | Eigenschaftswerte sind <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT-Werte.</strong></a> | 




 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                     | BESCHREIBUNG                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Shellmetadatenanbieter](shell-metadata-providers.md)<br/>                       | Ab Windows 7 macht Media Foundation Metadaten über die [**IPropertyStore-Schnittstelle**](/windows/win32/api/propsys/nn-propsys-ipropertystore) verfügbar.<br/> |
| [Metadateneigenschaften für Mediendateien](metadata-properties-for-media-files.md)<br/> | In diesem Thema werden die gängigsten Metadateneigenschaften für Mediendateien aufgeführt.<br/>                                                           |
| [Metadatenanbieter in Windows Vista](metadata-providers-in-windows-vista.md)<br/> | In Windows Vista macht Media Foundation Metadaten über die [**BEFMetadata-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) verfügbar.<br/>                   |



 

Wenn Sie eine benutzerdefinierte Medienquelle implementieren und Shellmetadaten verfügbar machen möchten, finden Sie weitere Informationen unter [Benutzerdefinierte Metadatenanbieter für Mediendateien.](custom-metadata-providers-for-media-files.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Programmierhandbuch](media-foundation-programming-guide.md)
</dt> </dl>

 

 
