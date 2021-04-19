---
description: ASF-ContentInfo-Objekt
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: ASF-ContentInfo-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bafa14279ab35c1c6986a8e19f302c764a587a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346054"
---
# <a name="asf-contentinfo-object"></a>ASF-ContentInfo-Objekt

Das Objekt "ASF *ContentInfo* " speichert Informationen aus dem ASF-Header Objekt einer Datei. Eine Anwendung kann das ContentInfo-Objekt für folgende Zwecke verwenden:

-   Lesen Sie das Header Objekt für eine vorhandene Mediendatei. In diesem Fall analysiert das ContentInfo-Objekt das Header Objekt und speichert Informationen über die Eigenschaften Datei. Media Foundation stellt einige dieser Eigenschaften über Attribute und Schnittstellen zur Verfügung. Diese werden in [Media Foundation Attributen für ASF-Header Objekte](media-foundation-attributes-for-asf-header-objects.md)beschrieben.
-   Schreiben Sie Header Informationen, und erstellen Sie ein Header Objekt für eine neue Datei.
-   Initialisieren Sie andere ASF-Objekte, z. b. den [ASF-Splitter](asf-splitter.md), den [ASF Multiplexer](asf-multiplexer.md)und den ASF-Indexer beim Lesen oder Schreiben einer Mediendatei.

Weitere Informationen zur Struktur einer ASF-Datei finden Sie unter [Struktur der ASF-Datei](asf-file-structure.md).

## <a name="creating-the-contentinfo-object"></a>Erstellen des ContentInfo-Objekts

Rufen Sie die [**mfkreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) -Funktion auf, um eine neue Instanz des ContentInfo-Objekts zu erstellen. Diese Methode gibt einen Zeiger auf ein leeres ContentInfo-Objekt zurück, das für die Arbeit mit einer bestimmten ASF-Datei initialisiert werden muss. Abhängig davon, ob die Anwendung eine vorhandene Datei liest oder eine neue ASF-Datei schreibt, muss Sie [**imfasfcontentinfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) oder [**imfasfcontentinfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) aufrufen, um das leere Objekt aufzufüllen.

Weitere Informationen zu diesen Methoden aufrufen finden Sie in den folgenden Themen:

-   [Lesen des ASF-Header Objekts einer vorhandenen Datei](reading-the-asf-header-object-of-an-existing-file.md)
-   [Informationen aus den ASF-Header Objekten werden erhalten.](getting-information-from-asf-header-objects.md)
-   [Schreiben eines ASF-Header Objekts für eine neue Datei](writing-an-asf-header-object-for-a-new-file.md)
-   [Media Foundation Attribute für ASF-Header Objekte](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wmcontainer-ASF-Komponenten](wmcontainer-asf-components.md)
</dt> </dl>

 

 



