---
description: Ein wahrgenommener Typ ist eine Kategorie von Dateitypen, mit der Sie Ihren Dateityp identifizieren können, um Windows (und Anwendungen) als Bild-, Audio-, Dokument- oder anderen Typ zu identifizieren.
title: Erkannte Typen (die Windows Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 56d4c495-a886-4723-88ca-5b7753398062
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fbbd459c610deb0b597e23bd4dc7217289b94c8a907b5341fa5667454ee778a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050329"
---
# <a name="perceived-types-the-windows-shell"></a>Erkannte Typen (die Windows Shell)

Ein wahrgenommener Typ ist eine Kategorie von Dateitypen, mit der Sie Ihren Dateityp identifizieren können, um Windows (und Anwendungen) als Bild-, Audio-, Dokument- oder anderen Typ zu identifizieren. Erkannte Typen werden für verschiedene Zwecke verwendet, einschließlich der Bestimmung des Ordnertyps, der dann zum Festlegen der Standardansichtseinstellungen verwendet wird. Beispielsweise wird einem Ordner mit Dateien des wahrgenommenen Bildtyps ein Standardansichtsmodus von Miniaturansichten zugewiesen.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zu wahrgenommenen Typen](#about-perceived-types)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="about-perceived-types"></a>Informationen zu wahrgenommenen Typen

Als PerceivedType-Werte definierte typen ähneln Dateitypen, mit der Ausnahme, dass sie auf allgemeine Kategorien von Dateiformattypen und nicht auf bestimmte Dateitypen verweisen. Bild, Text, Audio und komprimiert werden beispielsweise als Typen wahrgenommen. Dateitypen (im Allgemeinen öffentliche Dateitypen) können einem wahrgenommenen Typ zugewiesen werden und sollten immer dann zugewiesen werden, wenn es einen geeigneten Typ gibt. Beispielsweise werden die Bilddateitypen .bmp, .png, .jpg und .gif ebenfalls als Bildtyp wahrgenommen.

Die standardmäßig erkannten Typen sind wie folgt:

-   Ordner
-   Text
-   Image
-   Audio
-   Video
-   Compressed
-   Dokument
-   System
-   Application
-   Gamemedia
-   Kontakte

## <a name="additional-resources"></a>Weitere Ressourcen

-   Informationen zum Registrieren von wahrgenommenen Typen finden Sie unter [Anwendungsregistrierung.](app-registration.md)
-   Eine Liste der standardmäßig erkannten Typen finden Sie in der [**PERCEIVED-Enumeration.**](/windows/win32/api/shtypes/ne-shtypes-perceived)
-   Informationen zum Abrufen des erkannten Typs einer Datei basierend auf ihrer Dateinamenerweiterung finden Sie in der [**AssocGetPerceivedType-Funktion.**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsregistrierung](app-registration.md)
</dt> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Funktionsweise von Dateizuordnungen](fa-how-work.md)
</dt> <dt>

[Inhaltsansicht nach Dateityp oder Art](prophand-content-view.md)
</dt> <dt>

[Dateitypüberprüfung](file-type-verifier.md)
</dt> <dt>

[Dateityphandler](fa-file-extensions.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Zuordnungsarrays](fa-associationarray.md)
</dt> </dl>

 

 



