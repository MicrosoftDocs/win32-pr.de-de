---
description: Ein Benutzer kann den Status der Teredo-Schnittstelle über die Eingabeaufforderung überprüfen, indem er netsh interface teredo show state eintippen und die Ausgabe untersuchen.
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: Peerinfrastruktur und Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18dfa3fe075d0829358849b3783272aac74e60545c1e58e1d9bf1663738e3721
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794237"
---
# <a name="the-peer-infrastructure-and-teredo"></a>Peerinfrastruktur und Teredo

Ein Benutzer kann den Status der [Teredo-Schnittstelle](https://msdn.microsoft.com/library/ms819742.aspx) über die Eingabeaufforderung überprüfen, indem er **netsh interface teredo show state** eintippen und die Ausgabe untersuchen. Wenn der Status "offline" ist, ist Teredo nicht aktiv, was verhindert, dass der Benutzer über seine Teredo-Adressen eine Verbindung mit anderen Benutzern herstellen kann. Es ist möglich, dass Teredo offline ist, da Ihre Firewall deaktiviert ist oder [IPv6 nicht unterstützt.](/previous-versions/windows/embedded/ms898970(v=msdn.10))

 

 
