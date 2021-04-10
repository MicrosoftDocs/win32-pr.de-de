---
title: Verbindung wird getrennt
description: Wenn eine RAS-Client Anwendung einen Verbindungsvorgang startet, empfängt der rasdial-Befehl ein hrasconn-Verbindungs Handle, um die Verbindung zu identifizieren.
ms.assetid: a0fddc69-44bb-4bb0-ae57-ebecbe85cbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859a3751bcbaf7d95927cdf6d14de859ddcc731e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039527"
---
# <a name="disconnecting"></a>Verbindung wird getrennt

Wenn eine RAS-Client Anwendung einen Verbindungsvorgang startet, empfängt der [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) -Befehl ein **hrasconn** -Verbindungs Handle, um die Verbindung zu identifizieren. Wenn das zurückgegebene Handle nicht **null** ist, muss der Client schließlich die [**rashangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) -Funktion zum Beenden der Verbindung abrufen. Wenn während des Verbindungs Vorgangs ein Fehler auftritt, muss der Client **rashangup** anrufen, auch wenn die Verbindung nie hergestellt wurde.

Die Anwendung, die [**rashangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) aufruft, sollte nicht sofort beendet werden, da der Remote Zugriffs-Verbindungs-Manager Zeit benötigt, um die Verbindung ordnungsgemäß zu beenden. Stattdessen sollte die Anwendung warten, bis die Funktion " [**rasgetconnectstatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) " ein \_ Ungültiges Handle zurückgibt \_ , das angibt, dass die Verbindung gelöscht wurde.

Eine RAS-Client Anwendung muss möglicherweise eine Verbindung beenden, auch wenn Sie nicht über das von [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala)zurückgegebene Handle verfügt. Beispielsweise kann die Anwendung, die " **rasdial** " aufgerufen hat, beendet werden, nachdem die Verbindung erfolgreich hergestellt wurde. In diesem Fall kann die Anwendung, die die Verbindung trennt, die Funktion " [**Rasen-Connections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) " verwenden, um alle aktuellen Verbindungen zu erhalten. Für jede Verbindung gibt **rasenumschlag Connections** eine [**rasconn**](/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)) -Struktur zurück, die das **hrasconn** -Verbindungs Handle und den Namen des Telefonbucheintrags oder die Telefonnummer enthält, die beim Starten des Verbindungs Vorgangs angegeben wurde. Diese Informationen können verwendet werden, um eine Liste der Verbindungen anzuzeigen, von denen der Benutzer die zu Ende Verbindung auswählen kann.

 

 