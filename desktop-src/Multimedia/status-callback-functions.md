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
# <a name="status-callback-functions"></a><span data-ttu-id="32251-104">Status Rückruf Funktionen</span><span class="sxs-lookup"><span data-stu-id="32251-104">Status Callback Functions</span></span>

<span data-ttu-id="32251-105">Ein Aufzeichnungs Fenster kann Nachrichten an die Status Rückruffunktion senden, während Sie Videos auf dem Datenträger aufzeichnen oder während andere langwierige Vorgänge ausgeführt werden, um die Anwendung über den Fortschritt eines Vorgangs zu informieren.</span><span class="sxs-lookup"><span data-stu-id="32251-105">A capture window can send messages to the status callback function while capturing video to disk or during other lengthy operations to notify your application of the progress of an operation.</span></span> <span data-ttu-id="32251-106">Die Statusinformationen umfassen eine Nachrichten-ID und eine formatierte Text Zeichenfolge, die für die Anzeige bereit</span><span class="sxs-lookup"><span data-stu-id="32251-106">The status information includes a message identifier and a formatted text string ready for display.</span></span> <span data-ttu-id="32251-107">Die Anwendung kann die Nachrichten-ID verwenden, um die Benachrichtigungen zu filtern und die Nachrichten so einzuschränken, dass Sie dem Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="32251-107">Your application can use the message identifier to filter the notifications and limit the messages to present to the user.</span></span> <span data-ttu-id="32251-108">Bei Erfassungs Vorgängen ist die erste an die Rückruffunktion gesendete Nachricht immer IDs \_ Cap \_ Begin und die letzte immer IDs \_ Cap- \_ Ende.</span><span class="sxs-lookup"><span data-stu-id="32251-108">During capture operations, the first message sent to the callback function is always IDS\_CAP\_BEGIN and the last is always IDS\_CAP\_END.</span></span> <span data-ttu-id="32251-109">Der Nachrichten Bezeichner NULL gibt an, dass ein neuer Vorgang gestartet wird und die Rückruffunktion den aktuellen Status löschen soll.</span><span class="sxs-lookup"><span data-stu-id="32251-109">A message identifier of zero indicates a new operation is starting and the callback function should clear the current status.</span></span>

 

 




