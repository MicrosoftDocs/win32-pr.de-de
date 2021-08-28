---
title: Verbindung wird getrennt
description: Wenn eine RAS-Clientanwendung einen Verbindungsvorgang startet, empfängt der RasDial-Aufruf ein HR STRETCHNN-Verbindungshandle, um die Verbindung zu identifizieren.
ms.assetid: a0fddc69-44bb-4bb0-ae57-ebecbe85cbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fde205dfeb838639447c9f9359ee5b1258b2426eb55dbdd592291aea002fad6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101860"
---
# <a name="disconnecting"></a>Verbindung wird getrennt

Wenn eine RAS-Clientanwendung einen Verbindungsvorgang startet, empfängt der [**RasDial-Aufruf**](/windows/desktop/api/Ras/nf-ras-rasdiala) ein **HR STRETCHNN-Verbindungshandle,** um die Verbindung zu identifizieren. Wenn das zurückgegebene Handle nicht **NULL** ist, muss der Client schließlich die [**RasHangUp-Funktion**](/windows/desktop/api/Ras/nf-ras-rashangupa) aufrufen, um die Verbindung zu beenden. Wenn während des Verbindungsvorgangs ein Fehler auftritt, muss der Client **RasHangUp** aufrufen, obwohl die Verbindung nie hergestellt wurde.

Die Anwendung, die [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) aufruft, sollte nicht sofort beendet werden, da der Remotezugriff Verbindungs-Manager Zeit zum ordnungsgemäßen Beenden der Verbindung benötigt. Stattdessen sollte die Anwendung warten, bis die [**RasGetConnectStatus-Funktion**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) ERROR \_ INVALID HANDLE zurückgibt, was \_ angibt, dass die Verbindung gelöscht wurde.

Eine RAS-Clientanwendung muss möglicherweise eine Verbindung beenden, obwohl sie nicht über das von [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)zurückgegebene Handle verfügt. Beispielsweise könnte die Anwendung, die **RasDial** aufgerufen hat, beendet worden sein, nachdem die Verbindung erfolgreich hergestellt wurde. In diesem Fall kann die Trennende Anwendung die [**RasEnumConnections-Funktion**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) verwenden, um alle aktuellen Verbindungen abzurufen. Für jede Verbindung gibt **RasEnumConnections** eine [**RASCONN-Struktur**](/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)) zurück, die das **HROANN-Verbindungshandle** und den Telefonbucheintragsnamen oder die Telefonnummer enthält, die beim Starten des Verbindungsvorgangs angegeben wurde. Diese Informationen können verwendet werden, um eine Liste der Verbindungen anzuzeigen, aus denen der Benutzer die Zu beendende Verbindung auswählen kann.

 

 