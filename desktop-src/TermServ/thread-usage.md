---
title: Verwendung von Threads
description: Sie sollten die Anwendungs Thread Verwendung für eine mehr Benutzer-, multiprozessorRemotedesktopdienste Umgebung optimieren und ausgleichen.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a3b432cf4960c6ec7a8e51b458b9f574663ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337146"
---
# <a name="thread-usage"></a>Verwendung von Threads

Threads bieten eine bequeme Möglichkeit, eine Anwendung zu ermöglichen, die Nutzung von CPU-Ressourcen in einem System zu maximieren, insbesondere in einer Konfiguration mit mehreren Prozessoren. In einer Remotedesktopdienste Umgebung können allerdings mehrere Benutzer Multithreadanwendungen ausführen, und alle Threads für alle Benutzer konkurrieren mit den zentralen CPU-Ressourcen dieses Systems. Vor diesem Hintergrund sollten Sie die Anwendungs Thread Verwendung für eine mehr Benutzer-, multiprozessorRemotedesktopdienste Umgebung optimieren und ausgleichen. Obwohl eine schlecht entwickelte Multithreadanwendung mit Leerlauf-oder verschwendeten Threads auf einem Client Computer ausreichend funktionieren kann, kann die gleiche Anwendung auf einem mehr Benutzer-Remotedesktopdienste Server nicht gut funktionieren.

 

 




