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
# <a name="error"></a><span data-ttu-id="680f4-104">Fehler</span><span class="sxs-lookup"><span data-stu-id="680f4-104">Error</span></span>

<span data-ttu-id="680f4-105">Ein Aufzeichnungs Fenster verwendet Fehler Benachrichtigungs Meldungen, um die Anwendung über avicap-Fehler zu benachrichtigen, wie z. b. das Fehlen des Speicherplatzes, das Schreiben in eine schreibgeschützte Datei, das Fehlschlagen des Zugriffs auf die Hardware oder das Löschen zu vieler Frames.</span><span class="sxs-lookup"><span data-stu-id="680f4-105">A capture window uses error notification messages to notify your application of AVICap errors, such as running out of disk space, attempting to write to a read-only file, failing to access hardware, or dropping too many frames.</span></span> <span data-ttu-id="680f4-106">Der Inhalt einer Fehler Benachrichtigung enthält eine Nachrichten-ID und eine formatierte Text Zeichenfolge, die für die Anzeige bereit ist.</span><span class="sxs-lookup"><span data-stu-id="680f4-106">The content of an error notification includes a message identifier and a formatted text string ready for display.</span></span> <span data-ttu-id="680f4-107">Die Anwendung kann die Nachrichten-ID verwenden, um die Benachrichtigungen zu filtern und die Nachrichten so einzuschränken, dass Sie dem Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="680f4-107">Your application can use the message identifier to filter the notifications and limit the messages to present to the user.</span></span> <span data-ttu-id="680f4-108">Der Nachrichten Bezeichner 0 (null) gibt an, dass ein neuer Vorgang gestartet wird und die Rückruffunktion jede angezeigte Fehlermeldung löschen soll.</span><span class="sxs-lookup"><span data-stu-id="680f4-108">A message identifier of zero indicates a new operation is starting and the callback function should clear any displayed error message.</span></span>

 

 




