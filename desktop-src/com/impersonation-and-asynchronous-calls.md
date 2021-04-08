---
title: Identitätswechsel und asynchrone Aufrufe
description: Identitätswechsel und asynchrone Aufrufe
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0854946b619f7580173ffcbc97c9af3f2540361b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730680"
---
# <a name="impersonation-and-asynchronous-calls"></a>Identitätswechsel und asynchrone Aufrufe

Der Server kann die Identität des Clients nicht annehmen, nachdem der [**isynchronize:: Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) -Aufrufe des Servers abgeschlossen wurde, auch wenn die BEGIN- \_ Methode noch nicht abgeschlossen wurde. Angenommen, ein Client ruft die BEGIN- \_ Methode auf, der Server verarbeitet den Aufruf sofort und der Server Ruft ein **Signal** auf, um anzugeben, dass die Verarbeitung abgeschlossen ist. Auch wenn die Arbeit in der Begin-Methode ausgeführt wird \_ , kann der Server den Client nicht annehmen, nachdem der **Signal** Vorgang abgeschlossen wurde.

Wenn der Server die Identität des Clients annimmt, bevor er [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal)aufruft, wird das Identitätswechsel Token erst dann aus dem Thread entfernt, wenn der Server [**IServerSecurity:: RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) aufruft oder bis der Aufruf des Servers \_ zurückgibt, je nachdem, was zuerst eintritt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Delegierung und Identitätswechsel](delegation-and-impersonation.md)
</dt> <dt>

[Ausführen eines asynchronen Aufrufes](making-an-asynchronous-call.md)
</dt> </dl>

 

 