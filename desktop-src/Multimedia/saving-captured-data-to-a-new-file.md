---
title: Speichern erfasster Daten in einer neuen Datei
description: Speichern erfasster Daten in einer neuen Datei
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- WM_CAP_FILE_SAVEAS Nachricht
- capFileSaveAs-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f552f6f2f94ed1a7c7f7f8cae20b20c6fa4b5aa27e8105ab3f5dc33e60b7aff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892910"
---
# <a name="saving-captured-data-to-a-new-file"></a>Speichern erfasster Daten in einer neuen Datei

Wenn der Benutzer erfasste Daten speichern möchte, sollte die Anwendung den Inhalt der Erfassungsdatei mithilfe der [**WM \_ CAP FILE \_ \_ SAVEAS-Meldung**](wm-cap-file-saveas.md) (oder des [**Makros capFileSaveAs)**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) in einer anderen Datei speichern. Diese Meldung ändert weder den Namen noch den Inhalt der Erfassungsdatei. Ihre Anwendung muss einen Namen für die neue Datei angeben, da die Erfassungsdatei ihren ursprünglichen Dateinamen beibebehalte.

In der Regel ist eine Erfassungsdatei für das größte erwartete Erfassungssegment vorab zugewiesen, und es kann nur ein Teil davon zum Erfassen von Daten verwendet werden. Diese Meldung kopiert nur den Teil der Erfassungsdatei, der die Erfassungsdaten enthält.

 

 




