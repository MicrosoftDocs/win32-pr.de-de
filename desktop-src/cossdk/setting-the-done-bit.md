---
description: Festlegen des done-Bits
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Festlegen des done-Bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a53368377016c88633d91d942cde1970d979563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344220"
---
# <a name="setting-the-done-bit"></a>Festlegen des done-Bits

Com+ deaktiviert ein JIT-aktiviertes Objekt basierend auf dem Status einer Kontext Eigenschaft, dem done-Bit, wie folgt:

-   Wenn das done-Bit auf true festgelegt ist, deaktiviert com+ das Objekt, wenn der aktuelle Methoden Aufrufwert zurückgibt.
-   Wenn das done-Bit auf false festgelegt ist, bleibt das Objekt aktiv, wenn der aktuelle Methoden Aufrufwert zurückgegeben wird.

Standardmäßig ist das done-Bit auf false festgelegt, wenn ein Objekt erstellt und der Kontext initialisiert wird. (Jedes JIT-aktivierte Objekt wird in einem eigenen Kontext erstellt, sodass es ein eigenes done-Bit festgelegt werden kann.) Sie können diese Standardeinstellung jedoch für jede Methode ändern, indem Sie die Auto-done-Eigenschaft verwenden. Sie können das done-Bit auf folgende Weise festlegen:

-   Verwenden von [ **IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)
-   Verwenden von [ **IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)
-   Verwenden der Auto-done-Eigenschaft

## <a name="using-icontextstate"></a>Verwenden von IContextState

Sie können [**IContextState:: setde activateonreturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) verwenden, um das done-Bit auf true oder false festzulegen.

Sie können [**IContextState:: getdeactivateonreturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) verwenden, um den aktuellen Status des done-Bits aus dem Objekt Kontext zu erhalten.

## <a name="using-iobjectcontext"></a>Verwenden von IObjectContext

Mit den folgenden Methoden für [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) können Sie das done-Bit festlegen und gleichzeitig das konsistente Bit festlegen, das für die Abstimmung in Transaktionen verwendet wird:

-   [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) signalisiert Ihnen, dass Sie fertig sind, und dass Sie abstimmen, um für die aktuelle Transaktion ein Commit auszuführen. Sowohl das done-Bit als auch das konsistente Bit werden auf true festgelegt.
-   " [**Abtabort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) " signalisiert, dass Sie abgeschlossen sind, und Dooms die aktuelle Transaktion. Dabei wird das done-Bit auf true und das konsistente Bit auf false festgelegt.
-   [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) signalisiert, dass Sie nicht abgeschlossen sind, aber dass Sie für die Transaktion ein Commit durchgeführt haben. Dabei wird das done-Bit auf false und das konsistente Bit auf true festgelegt.
-   [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) signalisiert, dass Sie nicht ausgeführt werden, und dass Sie die Transaktion zu diesem Zeitpunkt nicht committen müssen, normalerweise weil der Status inkonsistent ist. Sowohl das done-Bit als auch das konsistente Bit werden auf false festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte für die Just-in-Time-Aktivierung in com+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Aktivieren der JIT-Aktivierung für eine Komponente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Objekt Pooling und com+-JIT-Aktivierung](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[Transaktionen und com+-JIT-Aktivierung](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



