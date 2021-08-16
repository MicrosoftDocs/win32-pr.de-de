---
title: Nachrichten- und Nachrichtenwarteschlangeneigenschaften
description: Eine Nachricht verfügt über Eigenschaften, die eine Bezeichnung, einen Nachrichtentext und eine Reihe von Optionen angeben.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c18b3a4751cd3be4473067dd9ca5aca17717672e6b67b559c10c502513fa2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928109"
---
# <a name="message-and-message-queue-properties"></a>Nachrichten- und Nachrichtenwarteschlangeneigenschaften

Eine Nachricht verfügt über Eigenschaften, die eine Bezeichnung, einen Nachrichtentext und eine Reihe von Optionen angeben. Zu den Optionen für Nachrichteneigenschaften können dienstqualität, Priorität, Journaling, Datenschutz und Authentifizierungsebenen sowie die Lebensdauer der Nachricht gehören. In herkömmlichen (Nicht-RPC)-Nachrichtenwarteschlangenanwendungen geben Sie diese Eigenschaften an, indem Sie die MSMQ-API-Funktionen oder COM-Objektmethoden aufrufen, die in der MSMQ SDK-Dokumentation beschrieben werden. RPC-Clientanwendungen können bestimmte Eigenschaften für Remoteprozeduraufrufe festlegen, indem [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) und [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)aufgerufen werden. Nach dem Festlegen bleiben die Eigenschaften für jede Nachricht wirksam, bis sie von der Clientanwendung zurückgesetzt werden.

Eine Nachrichtenwarteschlange verfügt über einen eigenen Satz von Eigenschaften, die sich von denen der Nachrichten unterscheiden. Diese Eigenschaften identifizieren eindeutig eine Warteschlange und definieren die Dienstklasse, die die Warteschlange bereitstellt, den Datenschutz und die Authentifizierungsebenen, die für Nachrichten in dieser Warteschlange erforderlich sind, und ob die Nachrichten Teil einer verteilten Transaktion sein sollen. Wie bei Nachrichteneigenschaften geben Sie die Eigenschaften einer Nachrichtenwarteschlange an, indem Sie die MSMQ-API-Funktionen oder COM-Objektmethoden aufrufen, die in der MSMQ-Dokumentation beschrieben werden. Eine RPC-Serveranwendung kann jedoch Eigenschaften ihrer eigenen Empfangswarteschlange angeben, wenn [**sie RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) aufruft, um die Bindung herzustellen.

 

 




