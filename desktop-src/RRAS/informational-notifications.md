---
title: Informationsbenachrichtigungen
description: Für die Verbindungszustände, die als Ausführungszustände bezeichnet werden, ist keine Aktion des Benachrichtigungshandlers erforderlich, es sei denn, es tritt ein Fehler auf.
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f526dcd0cd52eaa15929f970debe3ba78788fdb7525e734ee2e26e348b32552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790994"
---
# <a name="informational-notifications"></a>Informationsbenachrichtigungen

Für die [Verbindungszustände,](connection-states.md) die als Ausführungszustände bezeichnet werden, ist keine Aktion des Benachrichtigungshandlers erforderlich, es sei denn, es tritt ein Fehler auf. Ausführungszustände treten während der Teile des Verbindungsvorgangs auf, die RAS automatisch verarbeitet, z. B. beim Herstellen einer Verbindung mit den erforderlichen Geräten, beim Authentifizieren des Benutzers und beim Warten auf einen Rückruf vom Remoteserver. Die Benachrichtigung ist einfach ein Statusbericht an den Client.

Der Client kann diese Informationsbenachrichtigungen an den Benutzer übergeben. In einigen Ausführungszuständen möchte der Client möglicherweise zusätzliche Informationen anzeigen. Beispielsweise kann ein Benachrichtigungshandler, der eine RASCS \_ ConnectDevice-Benachrichtigung empfängt, die [**RasGetConnectStatus-Funktion**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) aufrufen, um den Namen und Typ des Geräts abzurufen, mit dem eine Verbindung hergestellt wird. Ein weiteres Beispiel ist, wenn der Client eine \_ rascs-projizierte Benachrichtigung empfängt. Dies tritt auf, wenn die RAS-Projektionsphase des Verbindungsvorgangs abgeschlossen wurde. Der Client kann die [**RasGetProjectionInfo-Funktion**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) aufrufen, um zusätzliche Informationen zur Projektion abzurufen. Der Client kann diese Informationen verwenden, um den Benutzer darüber zu informieren, welche Netzwerkprotokolle von dieser Verbindung verwendet werden können.

Sie sollten vermeiden, Code zu schreiben, der von der Reihenfolge oder dem Vorkommen bestimmter Informationszustände abhängt, da dies je nach Plattform variieren kann.

 

 




