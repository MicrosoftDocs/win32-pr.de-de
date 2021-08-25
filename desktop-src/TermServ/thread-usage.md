---
title: Verwendung von Threads
description: Sie sollten die Verwendung von Anwendungsthreads für eine Multiuser-, Multiprozessor- und Remotedesktopdienste optimieren und ausgleichen.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22959c6950458c95670d71479a2efe04fdafea765048508b9bd371b0a215064d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869520"
---
# <a name="thread-usage"></a>Verwendung von Threads

Threads bieten eine praktische Möglichkeit, einer Anwendung zu ermöglichen, ihre Nutzung von CPU-Ressourcen in einem System zu maximieren, insbesondere in einer Konfiguration mit mehreren Prozessoren. In einer Remotedesktopdienste-Umgebung können jedoch mehrere Benutzer Multithreadanwendungen ausführen, und alle Threads für alle Benutzer konkurrieren um die zentralen CPU-Ressourcen dieses Systems. Vor diesem Hintergrund sollten Sie die Verwendung von Anwendungsthreads für eine Umgebung mit mehreren Prozessoren und Remotedesktopdienste ausgleichen. Während eine schlecht entworfene Multithreadanwendung mit leeren oder verschwendeten Threads auf einem Clientcomputer möglicherweise eine angemessene Leistung auf einem Clientcomputer hat, kann dieselbe Anwendung auf einem Server mit mehreren Remotedesktopdienste sein.

 

 




