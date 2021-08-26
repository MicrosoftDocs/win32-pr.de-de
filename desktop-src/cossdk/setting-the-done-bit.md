---
description: Festlegen des Done-Bits
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Festlegen des Done-Bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad2d9a9dc06caa623d3f7c58d51aec389b40a1f3315ae09a21052bdf6e2ae3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070250"
---
# <a name="setting-the-done-bit"></a>Festlegen des Done-Bits

COM+ deaktiviert ein JIT-aktiviertes Objekt basierend auf dem Status einer Kontexteigenschaft , dem done-Bit, wie folgt:

-   Wenn das fertige Bit auf True festgelegt ist, deaktiviert COM+ das Objekt, wenn der aktuelle Methodenaufruf zurückgegeben wird.
-   Wenn das fertige Bit auf False festgelegt ist, bleibt das Objekt aktiv, wenn der aktuelle Methodenaufruf zurückgegeben wird.

Standardmäßig wird das fertige Bit auf False festgelegt, wenn ein Objekt erstellt und sein Kontext initialisiert wird. (Jedes JIT-aktivierte Objekt wird in seinem eigenen Kontext erstellt, sodass ein eigenes done-Bit festgelegt werden muss.) Sie können diese Standardeinstellung jedoch auf Methodenbasis ändern, indem Sie die Auto Done-Eigenschaft verwenden. Sie können das fertige Bit wie folgt festlegen:

-   Verwenden von [ **IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)
-   Verwenden von [ **IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)
-   Verwenden der auto-done-Eigenschaft

## <a name="using-icontextstate"></a>Verwenden von IContextState

Sie können [**IContextState::SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) verwenden, um das fertige Bit auf True oder False festzulegen.

Sie können [**IContextState::GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) verwenden, um den aktuellen Status des done-Bits aus dem Objektkontext abzurufen.

## <a name="using-iobjectcontext"></a>Verwenden von IObjectContext

Sie können die folgenden Methoden in [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) verwenden, um das fertige Bit festzulegen und gleichzeitig das konsistente Bit festzulegen, das für die Abstimmung in Transaktionen verwendet wird:

-   [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) signalisiert sowohl, dass Sie fertig sind als auch dafür stimmen, die aktuelle Transaktion zu committen. Es legt sowohl das fertige als auch das konsistente Bit auf True fest.
-   [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) signalisiert, dass Sie fertig sind, und unterbricht die aktuelle Transaktion. Das fertige Bit wird auf True und das konsistente Bit auf False festgelegt.
-   [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) signalisiert, dass Sie nicht fertig sind, aber für den Commit der Transaktion abstimmen. Das fertige Bit wird auf False und das konsistente Bit auf True festgelegt.
-   [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) signalisiert, dass Sie nicht fertig sind und dass Sie zurzeit kein Commit für die Transaktion durchführen, in der Regel, weil der Zustand inkonsistent ist. Es legt sowohl das fertige als auch das konsistente Bit auf False fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+ Just-in-Time-Aktivierungskonzepte](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Aktivieren der JIT-Aktivierung für eine Komponente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Objektpooling und COM+-JIT-Aktivierung](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[Transaktionen und COM+-JIT-Aktivierung](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



