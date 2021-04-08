---
title: Rückrufe (RPC)
description: Häufig erfordert das Programmiermodell einen Server Rückruf für einen Client über einen Remote Prozedur Aufruf (RPC) oder Client Aufrufe an einen nicht vertrauenswürdigen Server. Dies führt zu vielen potenziellen Fehlerquellen.
ms.assetid: a4f3ea26-ac4b-41e5-abde-96b4baedf2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6260e2cff2cbaff86f210764e89d55859c4d33af
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104040013"
---
# <a name="callbacks-rpc"></a>Rückrufe (RPC)

Häufig erfordert das Programmiermodell einen Server Rückruf für einen Client über einen Remote Prozedur Aufruf (RPC) oder Client Aufrufe an einen nicht vertrauenswürdigen Server. Dies führt zu vielen potenziellen Fehlerquellen.

Zuerst muss der Rückruf an den Client mit einer ausreichend niedrigen Identitätswechsel Ebene durchgeführt werden. Wenn es sich bei dem Server um einen Systemdienst mit hohen Berechtigungen handelt, kann es für den Client ausreichend Berechtigungen geben, das System zu übernehmen, wenn Sie einen lokalen Client mit einer Identitätswechsel Ebene von Identitätswechsel oder höher aufrufen. Wenn Sie einen Remote Client mit einer höheren Identitätswechsel Ebene als notwendig aufrufen, kann dies auch zu unerwünschten Folgen führen.

Zweitens: Wenn ein Angreifer den Dienst zur Durchführung eines Rückrufs veranlasst, kann er das sogenannte *Black Hole*– Denial of Service-Angriff starten. Derartige Angriffe sind nicht spezifisch für RPC. bei diesen Angriffen werden Sie von einem Computer dazu veranlasst, Datenverkehr an ihn zu senden, aber er antwortet nicht auf Ihre Anforderungen. Sie werden immer mehr Ressourcen zum Aufrufen der schwarzen Lücke, aber Sie werden nie zurückgegeben. Ein allgemeines Beispiel für einen solchen Angriff ist ein Angriff auf TCP-Ebene, der als TCP/IP-SYN-Überflutungs Angriff bezeichnet wird.

Auf der RPC-Ebene kommt es zu einem einfachen Black-Hole-Angriff, wenn ein Angreifer eine Schnittstelle aufruft, und fordert den Server auf, die Schnittstelle zurück aufzurufen. Die-Schnittstelle erfüllt, aber der Angreifer gibt den-Befehl nicht zurück: ein Thread auf dem Server ist gebunden. Der Angreifer führt dies 100-Mal durch, wobei 100 Threads auf dem Server gebunden werden. Der Server hat schließlich nicht mehr genügend Arbeitsspeicher. Das Debuggen des Servers kann die Identität des Aufrufers der schwarzen Löcher offenlegen, aber häufig wird der Server neu gestartet, ohne dass ein falsches Spiel zu vermuten ist, oder es ist nicht genügend Fachwissen verfügbar, um den Angreifer zu ermitteln.

Der dritte Fall ist auf dem Client. Häufig Ruft ein Client den Server auf, der den Server darüber informiert, wie Sie ihn zurück aufrufen (normalerweise eine Zeichen folgen Bindung), und wartet dann auf den Empfang eines Aufrufens vom Server Das Rückruf Protokoll vom Server an den Client sollte über einen Überprüfungsmechanismus verfügen, um sicherzustellen, dass der Rückruf beim Client tatsächlich vom Server stammt.

 

 




