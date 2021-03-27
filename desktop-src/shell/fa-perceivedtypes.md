---
description: Ein wahrgenommener Typ ist eine Kategorie von Dateitypen, mit der Sie den Dateityp für Windows (und Anwendungen) als Bild, Audiodaten, Dokument oder anderen Typ identifizieren können.
title: Wahrgenommene Typen (die Windows-Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 56d4c495-a886-4723-88ca-5b7753398062
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6136389c717fd4e27621a4d7f9f4cf2895c4116
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104995278"
---
# <a name="perceived-types-the-windows-shell"></a>Wahrgenommene Typen (die Windows-Shell)

Ein wahrgenommener Typ ist eine Kategorie von Dateitypen, mit der Sie den Dateityp für Windows (und Anwendungen) als Bild, Audiodaten, Dokument oder anderen Typ identifizieren können. Wahrgenommene Typen werden für verschiedene Zwecke verwendet, einschließlich der Bestimmung des Ordner Typs, der dann zum Festlegen der Standard Ansichts Einstellungen verwendet wird. So wird z. b. einem Ordner, der in Dateien mit dem Bild des Typs wahrgenommen ist, ein Standard Ansichtsmodus für Miniaturansichten zugewiesen.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zu wahrgenommenen Typen](#about-perceived-types)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="about-perceived-types"></a>Informationen zu wahrgenommenen Typen

Wahrgenommene Typen, die als "wahrnehmdtype"-Werte definiert sind, ähneln Dateitypen, außer dass Sie auf allgemeine Kategorien von Dateiformat Typen anstatt auf bestimmte Dateitypen verweisen. Beispielsweise werden Bild-, Text-, Audiodaten und komprimierte Typen als Typen angesehen. Dateitypen (in der Regel öffentliche Dateitypen) kann ein wahr gegebener Typ zugewiesen werden, und Sie sollten immer eine zugewiesen werden, wenn eine geeignete vorhanden ist. Die Bild Dateitypen BMP, PNG, JPG und GIF sind z. b. auch das wahrgenommene typimage.

Die standardmäßig erkannten Typen lauten wie folgt:

-   Ordner
-   Text
-   Image
-   Audio
-   Video
-   Compressed
-   Dokument
-   System
-   Application
-   GameMedia
-   Kontakte

## <a name="additional-resources"></a>Weitere Ressourcen

-   Informationen zum Registrieren von wahrgenommenen Typen finden Sie unter [Anwendungs Registrierung](app-registration.md).
-   Eine Liste der erkannten Standardtypen finden Sie unter der [**wahrgenommenen**](/windows/win32/api/shtypes/ne-shtypes-perceived) Enumeration.
-   Informationen zum Abrufen des wahrgenommenen Datentyps einer Datei anhand ihrer Dateinamenerweiterung finden Sie unter der Funktion " [**assocgetwahrnehmvedtype**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) ".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Registrierung](app-registration.md)
</dt> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Funktionsweise von Dateizuordnungen](fa-how-work.md)
</dt> <dt>

[Inhaltsansicht nach Dateityp oder-Art](prophand-content-view.md)
</dt> <dt>

[Dateityp Überprüfung](file-type-verifier.md)
</dt> <dt>

[Dateityp Handler](fa-file-extensions.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Zuordnungs Arrays](fa-associationarray.md)
</dt> </dl>

 

 



