---
description: Jedem Ereignis können ereignisspezifische Daten zugeordnet werden.
ms.assetid: fa2f9e71-44c3-4569-bde4-24112a756664
title: Ereignisdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459377d9cdf78fba46133b494723008df025caad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357404"
---
# <a name="event-data"></a>Ereignisdaten

Jedem Ereignis können ereignisspezifische Daten zugeordnet werden. Die Ereignisanzeige interpretiert diese Daten nicht. Es werden zusätzliche Daten nur in einem kombinierten Hexadezimal-und Textformat angezeigt. Der maximale Grenzwert für die Größe eines Ereignisses in der gerade Protokollierung beträgt 0x3ffff bytes. Verwenden Sie daher ereignisspezifische Daten sparsam, darunter auch, wenn Sie sicher sind, dass Sie für das Debuggen eines Problems hilfreich sein werden. Viele netzwerkbezogene Ereignisse enthalten beispielsweise Netzwerk Steuerungsblöcke (NCB) als ereignisspezifische Daten.

Wenn Sie ereignisspezifische Daten verwenden, sollte der letzte Teil der Beschreibungs Zeichenfolge einen Hinweis zu den Informationen bereitstellen, die als ereignisspezifische Daten bereitgestellt werden. Beispielsweise könnte die Netzwerk Software einen Hinweis wie z. b. "(NCB ist die Ereignisdaten)" bereitstellen. Verwenden Sie als Konvention Klammern um diese Hinweise, wie in diesem Beispiel angegeben.

Sie können auch ereignisspezifische Daten verwenden, um Informationen zu speichern, die von der Anwendung unabhängig vom Ereignisanzeige verarbeitet werden können. Beispielsweise können Sie einen Viewer speziell für Ihre Ereignisse schreiben oder ein Programm schreiben, das das Protokoll scannt und einen Bericht erstellt, der Informationen aus den ereignisspezifischen Daten enthält.

 

 



