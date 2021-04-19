---
description: Schreiben eines ASF-Header Objekts für eine neue Datei
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: Schreiben eines ASF-Header Objekts für eine neue Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dfcaf0d7c7c4ca469e75fb4c1bd47a4f8b1d32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366144"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a>Schreiben eines ASF-Header Objekts für eine neue Datei

Das Objekt "ASF ContentInfo" speichert Informationen zu den ASF-Header Objekten für eine Datei. Wenn eine ASF-Datei erstellt oder geändert wird, muss das Header Objekt generiert werden. Hierzu muss die Anwendung das Codierungs Profil des Inhalts für das ContentInfo-Objekt bereitstellen, damit Sie die Merkmale der zu erstellenden Mediendatei kennt.

Zum Schreiben einer neuen Datei können Sie das ContentInfo-Objekt für Folgendes verwenden:

-   Sammeln von Header Informationen aus dem Profil Objekt der zu erstellenden Datei
-   Auffüllen verschiedener Header Objekte in der von Media Foundation intern verwalteten ASF-Bibliothek,
-   Initialisieren Sie den [ASF Multiplexer](asf-multiplexer.md) für die Erstellung des ASF-Datenpakets.
-   Erstellen Sie das Header Objekt der obersten Ebene im Binärformat, das in eine Datei geschrieben werden kann.

Informationen zu Profilen finden Sie unter [ASF-Profil](asf-profile.md).

Dieser Abschnitt enthält die folgenden Themen:



| Thema                                                                                                              | BESCHREIBUNG                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Initialisieren des ContentInfo-Objekts einer neuen ASF-Datei](initializing-the-contentinfo-object-of-a-new-asf-file.md) | Beschreibt die [**imfasf ContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) -Methode, die das ContentInfo-Objekt mit in einem Profil Objekt gespeicherten Header Informationen initialisiert. |
| [Festlegen von Eigenschaften im ContentInfo-Objekt](setting-properties-in-the-contentinfo-object.md)                   | Informationen zu verschiedenen Konfigurations Eigenschaften, die für das ContentInfo-Objekt festgelegt werden müssen.                                                                                         |
| [Erstellen eines neuen ASF-Header Objekts](generating-a-new-asf-header-object.md)                                       | Generieren eines Medien Puffers, der das tatsächliche ASF-Header Objekt der neuen Datei enthält, aus dem ContentInfo-Objekt.                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-ContentInfo-Objekt](asf-contentinfo-object.md)
</dt> <dt>

[ASF-Header Objekt](asf-file-structure.md)
</dt> <dt>

Struktur der ASF-Datei
</dt> </dl>

 

 



