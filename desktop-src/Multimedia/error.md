---
title: Fehler
description: Fehler
ms.assetid: d3a087e4-7b57-4070-aa82-3673bc18a54f
keywords:
- Avicap-Rückruf Funktionen, Fehler Benachrichtigungs Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f418f16ae2af15902e96927990d79a4ecac08b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037381"
---
# <a name="error"></a>Fehler

Ein Aufzeichnungs Fenster verwendet Fehler Benachrichtigungs Meldungen, um die Anwendung über avicap-Fehler zu benachrichtigen, wie z. b. das Fehlen des Speicherplatzes, das Schreiben in eine schreibgeschützte Datei, das Fehlschlagen des Zugriffs auf die Hardware oder das Löschen zu vieler Frames. Der Inhalt einer Fehler Benachrichtigung enthält eine Nachrichten-ID und eine formatierte Text Zeichenfolge, die für die Anzeige bereit ist. Die Anwendung kann die Nachrichten-ID verwenden, um die Benachrichtigungen zu filtern und die Nachrichten so einzuschränken, dass Sie dem Benutzer angezeigt werden. Der Nachrichten Bezeichner 0 (null) gibt an, dass ein neuer Vorgang gestartet wird und die Rückruffunktion jede angezeigte Fehlermeldung löschen soll.

 

 




