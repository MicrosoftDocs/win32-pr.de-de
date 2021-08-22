---
description: Windows Mit Sockets 1.1 wurde der Async-Select-Mechanismus eingeführt, um Netzwerkereignisanzeigen ohne Abruf oder Blockierung zu ermöglichen.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Windows-Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bab33ecb4d2898c8f1e363ab19ad425503e9d005bf24229a29f581aadf1788f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993210"
---
# <a name="windows-messages"></a>Windows-Meldungen

Windows Mit Sockets 1.1 wurde der Async-Select-Mechanismus eingeführt, um Netzwerkereignisanzeigen ohne Abruf oder Blockierung zu ermöglichen. Die [**WSPAsyncSelect-Funktion**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) wird verwendet, um ein Interesse an einem oder mehr Netzwerkereignissen zu registrieren, wie in der vorherigen Liste aufgeführt, und um ein Fensterhand handle für die Benachrichtigung bereitstellen. Wenn ein nicht eintretendes Netzwerkereignis auftritt, wird eine vom Client Windows Nachricht an das angegebene Fenster gesendet. Der Dienstanbieter muss dazu die [**WPUPostMessage-Funktion**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) verwenden.

In Windows ist dies möglicherweise nicht der effizienteste Benachrichtigungsmechanismus und un umständlich für Daemons und Dienste, die keine Fenster öffnen möchten. Der im Folgenden beschriebene Signalisierungsmechanismus für Ereignisobjekt wird eingeführt, um dieses Problem zu lösen.

 

 
