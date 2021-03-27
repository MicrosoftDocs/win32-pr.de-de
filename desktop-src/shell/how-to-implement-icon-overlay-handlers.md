---
description: Symbol Überlagerungs Handler sind Prozess interne Component Object Model (com)-Objekte, die als DLLs implementiert werden.
ms.assetid: ADF27BFD-CC96-43F9-9EBB-DEBE0DEA7B92
title: Implementieren von Symbol Überlagerungs Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22c1057f65c50b31c6627846ec77103827a0283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979536"
---
# <a name="how-to-implement-icon-overlay-handlers"></a>Implementieren von Symbol Überlagerungs Handlern

Symbol Überlagerungs Handler sind Prozess interne Component Object Model (com)-Objekte, die als DLLs implementiert werden. Sie exportieren eine Schnittstelle zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ishellienoverlayidentifier**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier). Diese Schnittstelle verfügt über drei Methoden: [**ishellienoverlayidentifier:: getoverlayinfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo), [**ishellienoverlayidentifier:: GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority)und [**ishellienoverlayidentifier:: ismembership of**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof).

## <a name="instructions"></a>Instructions

### <a name="step-1-implementing-getoverlayinfo"></a>Schritt 1: Implementieren von getoverlayinfo

Die [**getoverlayinfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) -Methode wird zuerst während der Initialisierung aufgerufen. Die-Methode gibt den voll qualifizierten Pfad der Datei zurück, die das Symbol Überlagerungs Bild enthält, und den zugehörigen Null basierten Index in der Datei. Anschließend wird das Bild von der Shell der System Abbild Liste hinzugefügt. Symbol Überlagerungen können in jedem der Standard Dateitypen enthalten sein, einschließlich. exe,. dll und. ico.

Nachdem die Initialisierung fertiggestellt wurde, ruft die Shell [**getoverlayinfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) auf, wenn die Symbol Überlagerung des Handlers angezeigt werden muss. Die-Methode sollte denselben Dateinamen und Index wie bei der Initialisierung zurückgeben. Obwohl die Shell das in der System Abbild Liste zwischengespeicherte Bild verwendet, anstatt das Bild aus der Datei zu laden, wird eine Symbol Überlagerung weiterhin durch den Dateinamen und den Index identifiziert.

### <a name="step-2-implementing-getpriority"></a>Schritt 2: Implementieren von GetPriority

Die [**GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) -Methode wird nur während der Initialisierung aufgerufen. Er weist der Symbol Überlagerung des Handlers einen Prioritätswert zu. Der Wert kann zwischen 0 und 100 liegen, wobei 100 die niedrigste Priorität aufweist. Der Zweck dieses Prioritäts Werts besteht darin, die Shell zu helfen, den Konflikt zu lösen, der auftritt, wenn für ein einzelnes Objekt mehrere Symbol Überlagerungen angegeben werden. Die Shell verwendet zunächst einen internen Satz von Regeln, um das Symbol Overlay mit der höchsten Priorität zu bestimmen. Wenn diese Regeln den Konflikt nicht lösen, bestimmen die Werte, die den Symbolen zugewiesen sind, **die Priorität.**

Der Prioritätswert, der von [**GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) festgelegt wird, ist keine zuverlässige Methode zum Auflösen von Konflikten zwischen nicht verknüpften Symbolen-Handlern. Es gibt keine Möglichkeit für den Handler, zu bestimmen, welche Prioritätswerte andere Handler verwenden. Normalerweise sollten Sie den Wert auf 0 (null) festlegen. Der Prioritätswert ist jedoch nützlich, wenn Sie zwei oder mehr Symbol Überlagerungs Handler implementiert haben, die Symbol Überlagerungs Symbole für dasselbe Objekt anfordern können. Indem Sie die Prioritätswerte entsprechend festlegen, können Sie angeben, welche der angeforderten Symbol Überlagerungen angezeigt werden.

### <a name="step-3-implementing-ismemberof"></a>Schritt 3: Implementieren von ismembership of

Die Shell Ruft die [**ismembership of**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof) -Methode auf, um zu bestimmen, ob die Symbol Überlagerung eines Handlers für ein bestimmtes Objekt angezeigt werden soll. Die Shell gibt das-Objekt an, indem der Name an die-Methode übergeben wird. Wenn für einen Handler das Symbol Overlay angezeigt werden soll, gibt **ismembership of** S \_ OK zurück. Andernfalls wird S false zurückgegeben \_ .

Symbol Überlagerungs Handler sind normalerweise für die Arbeit mit einer bestimmten Gruppe von Dateien vorgesehen. Ein typisches Beispiel ist ein [Dateityp](fa-file-types.md), der durch eine bestimmte Dateinamenerweiterung gekennzeichnet wird. Ein Symbol Überlagerungs Handler kann eine Symbol Überlagerung für alle Dateien des Dateityps anfordern. Einige Handler fordern eine Symbol Überlagerung nur an, wenn sich eine Datei mit dem Dateityp in einem bestimmten Zustand befindet. Allerdings können Symbol Überlagerungs Handler das Symbol Overlay für jedes beliebige Objekt anfordern.

 

 
