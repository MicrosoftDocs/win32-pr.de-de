---
description: Schreiben von Erfassungs Filtern
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Schreiben von Erfassungs Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1a64de2b56dbc0728432307036fc46387f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350279"
---
# <a name="writing-capture-filters"></a>Schreiben von Erfassungs Filtern

Das Schreiben eines Audiofilters oder Video Erfassungs Filters für DirectShow wird nicht empfohlen. Stattdessen bietet DirectShow automatische Unterstützung für Audiogeräte und Video Erfassungsgeräte, mithilfe von Wrapper Filtern und dem [Enumerator des System Geräts](system-device-enumerator.md). Weitere Informationen zum Implementieren eines Gerätetreibers finden Sie in der Dokumentation zum Windows-Treiberkit (WDK).

Dieser Abschnitt ist nur für Entwickler gedacht, die benutzerdefinierte Daten von einem ungewöhnlichen Hardware Gerät erfassen müssen.

Dieser Artikel enthält folgende Abschnitte:

-   [PIN-Anforderungen für Erfassungs Filter](pin-requirements-for-capture-filters.md)
-   [Implementieren einer Vorschau-PIN (optional)](implementing-a-preview-pin--optional.md)
-   [Erstellen von Daten in einem Erfassungs Filter](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



