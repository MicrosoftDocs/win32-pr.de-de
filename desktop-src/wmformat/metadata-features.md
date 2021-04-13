---
title: Metadatenfeatures
description: Metadaten werden in ASF-Dateien verwendet, um Dateiinhalte und-Eigenschaften zu beschreiben.
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- Windows Media-Format-SDK, Metadatenfeatures
- Windows Media-Format-SDK, Features
- Advanced Systems Format (ASF), Metadatenfeatures
- ASF (Advanced Systems Format), Metadatenfeatures
- Advanced Systems Format (ASF), Features
- ASF (Advanced Systems Format), Features
- Metadaten, Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ea31885a1c1635ee4778683858876572e32262
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104390056"
---
# <a name="metadata-features"></a>Metadatenfeatures

Metadaten werden in ASF-Dateien verwendet, um Dateiinhalte und-Eigenschaften zu beschreiben. Alle von Ihnen erstellten ASF-Dateien sollten entsprechende Metadaten enthalten. (Eine Übersicht finden Sie unter [Metadaten](metadata.md).) Das Windows Media-Format SDK bietet Unterstützung für die Metadatenbearbeitung über das Writer-Objekt, das Metadaten-Editor-Objekt und die Reader-und synchronen Reader-Objekte. Systemeigene Unterstützung für eine Vielzahl von Metadatenattributen ist enthalten. Eine Liste der vordefinierten Attribute finden Sie unter [Attribute](attributes.md) .

Die Metadatenunterstützung, die von den verschiedenen Objekten des Windows Media Format SDK bereitgestellt wird, ist flexibel und leistungsstark. Die wichtigsten Metadatenfeatures werden in der folgenden Liste zusammengefasst:

-   Flexible Attribut Größe. Metadatenattribute sind nicht in der Größe beschränkt.
-   Attribute auf Streamebene. Metadaten in ASF-Dateien können der Datei als Ganzes oder einem bestimmten Stream zugewiesen werden.
-   Doppelte Attribute. Ein benanntes Attribut kann mehrmals in derselben Datei verwendet werden. Diese Funktion wird besonders beim Zuweisen von beschreibenden Inhalts Attributen verwendet. Ein-Song kann z. b. mehrere Autoren aufweisen, die jeweils ein separates **Author** -Attribut in der Datei erfordern.
-   Mehrere Sprachen. Jedem Attribut ist eine Sprache zugeordnet. Sie können die unterstützten Sprachen festlegen und dann einem Attribut zuweisen, das Sie schreiben. Da Sie Attribute duplizieren können, können Sie die wichtigsten Attribute in mehreren Sprachen bereitstellen, um eine größere Zielgruppe zu erreichen. Wenn Sie keine Sprache angeben, wird die Standardsprache (abgerufen aus dem Betriebssystem des Computers, auf dem die Anwendung ausgeführt wird) verwendet.
-   Komplexe Attribute. Einige der vordefinierten Attribute unterstützen strukturierte Daten. Für diese Attribute ist der Datentyp binär, aber der Wert ist eine Struktur, die in diesem SDK definiert ist.

In den folgenden Themen werden die anderen unterstützten Metadatenfeatures erläutert.



| Thema                                  | BESCHREIBUNG                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [ID3-Unterstützung](id3.md)                 | Erläutert die Unterstützung für ID3-Frames mithilfe der Objekte des Windows Media-Format-SDKs. |
| [Benutzerdefinierte Metadaten](custom-metadata.md) | Erläutert die Auswirkungen der Verwendung von benutzerdefinierten Metadaten.                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aspekte**](features.md)
</dt> <dt>

[**Iwmheaderinfo-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**IWMHeaderInfo2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[**IWMHeaderInfo3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[**Metadaten**](metadata.md)
</dt> </dl>

 

 




