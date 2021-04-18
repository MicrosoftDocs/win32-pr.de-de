---
description: In Windows Sockets 1,1 wurde der Async-Select-Mechanismus eingeführt, um Netzwerk Ereignis Hinweise bereitzustellen, für die weder Abruf noch Blockierung aufgetreten ist.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Windows-Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0f60bb597a7dd92c0039dd805a971bb8587ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368167"
---
# <a name="windows-messages"></a>Windows-Meldungen

In Windows Sockets 1,1 wurde der Async-Select-Mechanismus eingeführt, um Netzwerk Ereignis Hinweise bereitzustellen, für die weder Abruf noch Blockierung aufgetreten ist. Die [**wspasyncselect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) -Funktion wird verwendet, um ein Interesse an einem oder mehreren Netzwerk Ereignissen zu registrieren, wie im vorherigen Abschnitt aufgeführt, und stellt ein Fenster Handle bereit, das für die Benachrichtigung verwendet wird. Wenn ein gedesigniertes Netzwerk Ereignis auftritt, wird eine vom Client angegebene Windows-Meldung an das angegebene Fenster gesendet. Der Dienstanbieter muss die [**wpupostmessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) -Funktion verwenden, um dies zu erreichen.

In Windows ist dies möglicherweise nicht der effizienteste Benachrichtigungs Mechanismus und für Daemons und Dienste, die keine Fenster öffnen möchten, unpraktisch. Das in den folgenden beschriebenen Verfahren zum Signalisieren von Ereignis Objekten wird eingeführt, um dieses Problem zu beheben.

 

 
