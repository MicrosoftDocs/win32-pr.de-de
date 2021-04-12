---
title: Eigenschaften von Message und Message Queue
description: Eine Nachricht verfügt über Eigenschaften, mit denen eine Bezeichnung, ein Nachrichtentext und eine Reihe von Optionen angegeben werden.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0139a588b52f1de1de43d8ec50aebdaf57b995ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310516"
---
# <a name="message-and-message-queue-properties"></a>Eigenschaften von Message und Message Queue

Eine Nachricht verfügt über Eigenschaften, mit denen eine Bezeichnung, ein Nachrichtentext und eine Reihe von Optionen angegeben werden. Nachrichten Eigenschaften Optionen können Servicequalität, Priorität, Journalisierung, Datenschutz und Authentifizierungs Ebenen sowie die Lebensdauer der Nachricht einschließen. In herkömmlichen Message Queuinganwendungen (nicht-RPC) geben Sie diese Eigenschaften durch Aufrufen der MSMQ-API-Funktionen oder der com-Objektmethoden an, die in der MSMQ SDK-Dokumentation beschrieben werden. RPC-Client Anwendungen können bestimmte Eigenschaften für Remote Prozedur Aufrufe festlegen, indem [**rpcbindingsetoption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) und [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)aufgerufen werden. Nachdem die Eigenschaften festgelegt wurden, bleiben Sie für jede Nachricht wirksam, bis Sie von der Client Anwendung zurückgesetzt werden.

Eine Nachrichten Warteschlange verfügt über einen eigenen Satz von Eigenschaften, abgesehen von den Nachrichten. Diese Eigenschaften identifizieren eine Warteschlange eindeutig und definieren die Dienstklasse, die von der Warteschlange bereitgestellt wird, den Datenschutz und die Authentifizierungs Stufen, die für die Nachrichten in dieser Warteschlange erforderlich sind, und ob die Nachrichten Teil einer verteilten Transaktion sind. Wie bei den Nachrichten Eigenschaften geben Sie die Eigenschaften einer Nachrichten Warteschlange an, indem Sie die MSMQ-API-Funktionen oder com-Objektmethoden aufrufen, die in der MSMQ-Dokumentation beschrieben werden. Eine RPC-Serveranwendung kann jedoch Eigenschaften der eigenen Empfangs Warteschlange angeben, wenn [**rpcserveruseprotseqepex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) zum Einrichten der Bindung aufgerufen wird.

 

 




