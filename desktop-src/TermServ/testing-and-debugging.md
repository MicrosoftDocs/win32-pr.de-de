---
title: Testen und Debuggen
description: Es ist ein \ 0034; Echo \ 0034; vorhanden. der Listener, der vom RDC-Client (Remotedesktopverbindung) implementiert wird und auf eingehende Verbindungen lauscht.
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9028ccf0eea97a8651392baba094ac6dcda242f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338165"
---
# <a name="testing-and-debugging"></a>Testen und Debuggen

Es gibt einen "Echo"-Listener, der vom RDC-Client (Remotedesktopverbindung) implementiert wird, der immer vorhanden ist und auf eingehende Verbindungen lauscht. Wenn Sie die Serverseite eines Moduls eines dynamischen virtuellen Kanals (DVC) schreiben, können Sie als Schnelltest einen Endpunkt mit dem Namen "Echo" öffnen. Jeder Schreibvorgang in einen Kanal, der von diesem Endpunkt aus instanziiert wird, führt zum Empfang der gleichen Daten.

Mit dieser Technik können Sie eine Eingabe-/Ausgabe-Implementierung (e/a) des serverseitigen Moduls testen, um die Reaktionszeit für ein Remotedesktopverbindung (RDC)-Client-Plug-in zu messen oder um die Netzwerkverzögerung für den Remotedesktopverbindung-Client (RDC) zu messen. Es gibt keine Einschränkung hinsichtlich der Datenmenge, die über diesen Kanal gesendet werden kann.

 

 




