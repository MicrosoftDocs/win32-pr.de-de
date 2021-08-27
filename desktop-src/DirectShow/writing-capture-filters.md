---
description: Schreiben von Erfassungsfiltern
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Schreiben von Erfassungsfiltern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa4807f381dc925a68fa3c60e45d5c8c5c444653230f366895b370e97aaccb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049090"
---
# <a name="writing-capture-filters"></a>Schreiben von Erfassungsfiltern

Das Schreiben eines Audio- oder Videoaufnahmefilters für DirectShow wird nicht empfohlen. Stattdessen bietet DirectShow automatische Unterstützung für Audio- und Videoerfassungsgeräte mit Wrapperfiltern und dem [Systemgeräte-Enumerator](system-device-enumerator.md). Weitere Informationen zum Implementieren eines Gerätetreibers finden Sie in der WDK-Dokumentation (Windows Driver Kit).

Dieser Abschnitt richtet sich nur an Entwickler, die eine Art benutzerdefinierter Daten von einem ungewöhnlichen Hardwaregerät erfassen müssen.

Dieser Artikel enthält folgende Abschnitte:

-   [Anforderungen für Erfassungsfilter anheften](pin-requirements-for-capture-filters.md)
-   [Implementieren eines Vorschaupins (optional)](implementing-a-preview-pin--optional.md)
-   [Erstellen von Daten in einem Erfassungsfilter](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



