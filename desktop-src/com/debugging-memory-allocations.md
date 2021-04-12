---
title: Debugging von Speicher Belegungen
description: Debugging von Speicher Belegungen
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb6a7dbe313cfe571fa6b4d244df35407fa331e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316526"
---
# <a name="debugging-memory-allocations"></a>Debugging von Speicher Belegungen

COM stellt die [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) -Schnittstelle bereit, die Entwickler zum Debuggen Ihrer Speicher Belegungen verwenden können. Für jede Methode in [**imzuzuordc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc)gibt es zwei Methoden in **imzuordcspy**, eine "Pre"-Methode und eine "Post"-Methode. Nachdem ein Entwickler es implementiert und im System veröffentlicht hat, ruft das System die **IMallocSpy** -Methode "Pre" direkt vor der entsprechenden **IMalloc** -Methode auf, sodass der Debugcode für die Zuordnungs Operation "Spy" und die Post-Methode aufgerufen wird, um den Spy freizugeben.

Wenn com z. b. erkennt, dass der nächste Aufruf ein Aufruf von [**imzuzuordc:: zuordc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc)ist, wird [**imzuzuordcspy::P rezuzuzuweisung**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc)aufgerufen. dabei werden die Debugvorgänge ausgeführt, die der Entwickler bei der **Zuord:P** **nungsausführung** wünscht [](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten der Speicher Belegung](managing-memory-allocation.md)
</dt> </dl>

 

 