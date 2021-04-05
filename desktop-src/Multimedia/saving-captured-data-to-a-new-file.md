---
title: Speichern erfasster Daten in einer neuen Datei
description: Speichern erfasster Daten in einer neuen Datei
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- WM_CAP_FILE_SAVEAS Meldung
- capfilesaveas-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1966b8cf1e189038e9ee427a868b84a1fb1b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710451"
---
# <a name="saving-captured-data-to-a-new-file"></a>Speichern erfasster Daten in einer neuen Datei

Wenn der Benutzer erfasste Daten speichern möchte, sollte die Anwendung den Inhalt der Erfassungs Datei in einer anderen Datei speichern, indem [**die \_ \_ Datei " \_ SaveAs**](wm-cap-file-saveas.md) " der WM-Cap-Datei (oder das Makro " [**capfilesaveas**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) ") verwendet wird. Diese Meldung ändert nicht den Namen oder den Inhalt der Erfassungs Datei. Die Anwendung muss einen Namen für die neue Datei angeben, da die Erfassungs Datei den ursprünglichen Dateinamen beibehält.

In der Regel wird eine Erfassungs Datei für das größte erwartete Erfassungs Segment reserviert, und es kann nur ein Teil davon zum Erfassen von Daten verwendet werden. In dieser Meldung wird nur der Teil der Erfassungs Datei kopiert, der die Aufzeichnungsdaten enthält.

 

 




