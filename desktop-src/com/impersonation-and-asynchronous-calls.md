---
title: Identitätswechsel und asynchrone Aufrufe
description: Identitätswechsel und asynchrone Aufrufe
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84f7fcbdc820b50ef4eaaedd81ac579fcce64f1371bc57219348f6dcbedc0f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070880"
---
# <a name="impersonation-and-asynchronous-calls"></a>Identitätswechsel und asynchrone Aufrufe

Der Server kann die Identität des Clients nicht annehmen, nachdem der Serveraufruf von [**ISynchronize::Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) abgeschlossen wurde, auch wenn die \_ Begin-Methode noch nicht abgeschlossen wurde. Angenommen, ein Client ruft die \_ Begin-Methode auf, der Server verarbeitet den Aufruf sofort, und der Server ruft **Signal** auf, um anzugeben, dass die Verarbeitung abgeschlossen ist. Auch wenn in der Begin-Methode noch Arbeit erforderlich \_ ist, kann der Server die Identität des Clients nicht annehmen, nachdem der **Aufruf** von Signal abgeschlossen wurde.

Wenn der Server vor dem Aufruf von [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal)die Identität des Clients angibt, wird das Identitätswechseltoken erst dann aus dem Thread entfernt, wenn der Server [**IServerSecurity::RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) aufruft oder bis der Aufruf von Begin des Servers \_ zurückgibt, je nachdem, was zuerst eintritt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Delegierung und Identitätswechsel](delegation-and-impersonation.md)
</dt> <dt>

[Erstellen eines asynchronen Aufrufs](making-an-asynchronous-call.md)
</dt> </dl>

 

 