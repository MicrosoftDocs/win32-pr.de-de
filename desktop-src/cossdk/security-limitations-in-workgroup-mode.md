---
description: Sicherheitseinschränkungen im Arbeitsgruppenmodus
ms.assetid: 05c0aba7-b94b-49d4-a0fc-1ff0a23550b3
title: Sicherheitseinschränkungen im Arbeitsgruppenmodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af613b8de16b99090bcdb02bde0015d01312df3d642c895d61ef59ff80873eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546274"
---
# <a name="security-limitations-in-workgroup-mode"></a>Sicherheitseinschränkungen im Arbeitsgruppenmodus

Die [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) Arbeitsgruppenkonfiguration lässt nicht zu, dass der COM+-Dienst für Komponenten in der Warteschlange die Anwendungssicherheit unterstützt. Wenn Sie Message Queuing mit der Arbeitsgruppenkonfiguration installiert haben, [](specifying-the-authentication-protocol.md) müssen Sie die Sicherheit für jede Anwendung  in der Warteschlange deaktivieren, auf die in dieser  Konfiguration zugegriffen wird, indem Sie im Dialogfeld Eigenschaften der COM+-Anwendung auf der Registerkarte **Queuing** die Option Nachrichten nicht authentifizieren auswählen, indem Sie das Verwaltungstool Komponentendienste verwenden. Dies sollte nur in einem vertrauenswürdigen Netzwerk erfolgen und muss sowohl auf dem Client als auch auf dem Server erfolgen, wenn die Anwendung bereits exportiert wurde.

 

 



