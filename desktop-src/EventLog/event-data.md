---
description: Jedem Ereignis können ereignisspezifische Daten zugeordnet sein.
ms.assetid: fa2f9e71-44c3-4569-bde4-24112a756664
title: Ereignisdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf6809b837d36f4cf2ddc0d74b90fe3a925f5eae7efc96973a9bf845c610bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901480"
---
# <a name="event-data"></a>Ereignisdaten

Jedem Ereignis können ereignisspezifische Daten zugeordnet sein. Die Ereignisanzeige interpretiert diese Daten nicht. Es werden zusätzliche Daten nur in einem kombinierten Hexadezimal- und Textformat angezeigt. Der maximale Grenzwert für die Größe eines Ereignisses im geraden Protokoll beträgt 0x3FFFF Bytes. Verwenden Sie daher ereignisspezifische Daten nur dann, wenn Sie sicher sind, dass sie für das Debuggen eines Problems nützlich sind. Beispielsweise enthalten viele netzwerkbezogene Ereignisse Netzwerksteuerungsblöcke (NCB) als ereignisspezifische Daten.

Wenn Sie ereignisspezifische Daten verwenden, sollte der letzte Teil der Beschreibungszeichenfolge einen Hinweis zu den Informationen enthalten, die als ereignisspezifische Daten bereitgestellt werden. Beispielsweise könnte die Netzwerksoftware einen Hinweis wie den folgenden bereitstellen: "(The NCB is the event data.)" (Der NCB ist die Ereignisdaten.)" Verwenden Sie gemäß der Konvention Klammern um solche Hinweise, wie in diesem Beispiel gezeigt.

Sie können ereignisspezifische Daten auch verwenden, um Informationen zu speichern, die die Anwendung unabhängig vom Ereignisanzeige verarbeiten kann. Beispielsweise können Sie einen Viewer speziell für Ihre Ereignisse schreiben oder ein Programm schreiben, das das Protokoll überprüft und einen Bericht erstellt, der Informationen aus den ereignisspezifischen Daten enthält.

 

 



