---
title: Metadatenfeatures
description: Metadaten werden in ASF-Dateien verwendet, um Dateiinhalte und -eigenschaften zu beschreiben.
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- Windows Medienformat-SDK, Metadatenfeatures
- Windows Medienformat-SDK, Features
- Advanced Systems Format (ASF), Metadatenfeatures
- ASF (Advanced Systems Format), Metadatenfeatures
- Advanced Systems Format (ASF), Features
- ASF (Advanced Systems Format), Features
- Metadaten, Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6865e54f2eeabcb96dd88df27aba578a9169ed84857d17af5602848041f24118
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700452"
---
# <a name="metadata-features"></a>Metadatenfeatures

Metadaten werden in ASF-Dateien verwendet, um Dateiinhalte und -eigenschaften zu beschreiben. Alle asf-Dateien, die Sie erstellen, sollten entsprechende Metadaten enthalten. (Eine Übersicht finden Sie unter [Metadaten](metadata.md).) Das Windows Media Format SDK bietet Unterstützung für die Bearbeitung von Metadaten über das Writer-Objekt, das Metadaten-Editor-Objekt und die Reader- und synchronen Readerobjekte. Native Unterstützung für eine Vielzahl von Metadatenattributen ist enthalten. Eine Liste der vordefinierten Attribute finden Sie unter [Attribute.](attributes.md)

Die Metadatenunterstützung, die von den verschiedenen Objekten des Windows Media Format SDK bereitgestellt wird, ist flexibel und leistungsstark. Die wichtigsten Metadatenfeatures sind in der folgenden Liste zusammengefasst:

-   Flexible Attributgröße. Die Größe von Metadatenattributen ist nicht beschränkt.
-   Attribute auf Streamebene. Metadaten in ASF-Dateien können der Datei als Ganzes oder einem bestimmten Stream zugewiesen werden.
-   Duplizierte Attribute. Ein benanntes Attribut kann mehrmals in derselben Datei verwendet werden. Dieses Feature ist bei der Zuweisung beschreibender Attribute von Inhalten von besonderem Nutzen. Beispielsweise kann ein Titel mehrere Autoren haben, von denen jeder ein separates **Author-Attribut** in der Datei erfordert.
-   Mehrere Sprachen. Jedem Attribut ist eine Sprache zugeordnet. Sie können die unterstützten Sprachen festlegen und dann jedem von Ihnen geschriebenen Attribut eine sprache zuweisen. Da Sie Attribute duplizieren können, können Sie die wichtigsten Attribute in mehreren Sprachen bereitstellen, um eine größere Zielgruppe zu erreichen. Wenn Sie keine Sprache angeben, wird die Standardsprache (abgerufen vom Betriebssystem des Computers, auf dem Ihre Anwendung ausgeführt wird) verwendet.
-   Komplexe Attribute. Einige der vordefinierten Attribute unterstützen strukturierte Daten. Für diese Attribute ist der Datentyp binär, aber der Wert ist eine in diesem SDK definierte Struktur.

In den folgenden Themen werden die anderen unterstützten Metadatenfeatures erläutert.



| Thema                                  | Beschreibung                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [ID3-Unterstützung](id3.md)                 | Erläutert die Unterstützung für ID3-Frames mithilfe der Objekte des Windows Media Format SDK. |
| [Benutzerdefinierte Metadaten](custom-metadata.md) | Erläutert die Auswirkungen der Verwendung benutzerdefinierter Metadaten.                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features**](features.md)
</dt> <dt>

[**IWMHeaderInfo-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**IWMHeaderInfo2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[**IWMHeaderInfo3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[**Metadaten**](metadata.md)
</dt> </dl>

 

 




