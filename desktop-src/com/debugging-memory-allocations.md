---
title: Debuggen von Speicherzuweisungen
description: Debuggen von Speicherzuweisungen
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b3376b2ffee17ce747197eb57fecbdae18e086d5252dd5f4721975181885
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993450"
---
# <a name="debugging-memory-allocations"></a>Debuggen von Speicherzuweisungen

COM stellt die [**IMallocSpy-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) bereit, mit der Entwickler ihre Speicherzuweisungen debuggen können. Für jede Methode in [**IMalloc gibt**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc)es zwei Methoden in **IMallocSpy,** eine "pre"-Methode und eine "post"-Methode. Nachdem ein Entwickler sie implementiert und im System veröffentlicht hat, ruft das System die "pre"-Methode **von IMallocSpy** direkt vor der entsprechenden **IMalloc-Methode** auf, sodass der Debugcode den Zuordnungsvorgang "ausspionieren" kann, und ruft die "post"-Methode auf, um den Spy frei zu geben.

Wenn COM z. B. erkennt, dass der nächste Aufruf ein Aufruf von [**IMalloc::Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc)ist, ruft es [**IMallocSpy::P reAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc)auf, um alle Debugvorgänge durchzuführen, die der Entwickler während der **Alloc-Ausführung** möchte, und ruft dann nach der Rückgabe des **Alloc-Aufrufs** [**IMallocSpy::P ostAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) auf, um den Spy frei zu geben und die Steuerung an den Code zurückgibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten der Speicherzuordnung](managing-memory-allocation.md)
</dt> </dl>

 

 