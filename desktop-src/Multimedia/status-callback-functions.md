---
title: Status Rückruf Funktionen
description: Status Rückruf Funktionen
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- Avicap-Rückruf Funktionen, Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b4b4bf4cad5f689f1e146986f9d1b55b00f1aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388309"
---
# <a name="status-callback-functions"></a>Status Rückruf Funktionen

Ein Aufzeichnungs Fenster kann Nachrichten an die Status Rückruffunktion senden, während Sie Videos auf dem Datenträger aufzeichnen oder während andere langwierige Vorgänge ausgeführt werden, um die Anwendung über den Fortschritt eines Vorgangs zu informieren. Die Statusinformationen umfassen eine Nachrichten-ID und eine formatierte Text Zeichenfolge, die für die Anzeige bereit Die Anwendung kann die Nachrichten-ID verwenden, um die Benachrichtigungen zu filtern und die Nachrichten so einzuschränken, dass Sie dem Benutzer angezeigt werden. Bei Erfassungs Vorgängen ist die erste an die Rückruffunktion gesendete Nachricht immer IDs \_ Cap \_ Begin und die letzte immer IDs \_ Cap- \_ Ende. Der Nachrichten Bezeichner NULL gibt an, dass ein neuer Vorgang gestartet wird und die Rückruffunktion den aktuellen Status löschen soll.

 

 




