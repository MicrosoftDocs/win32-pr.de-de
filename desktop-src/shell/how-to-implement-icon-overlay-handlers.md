---
description: Symbolüberlagerungshandler sind COM-Objekte (In-Process Component Object Model), die als DLLs implementiert werden.
ms.assetid: ADF27BFD-CC96-43F9-9EBB-DEBE0DEA7B92
title: Implementieren von Symbolüberlagerungshandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8745d0d5c0cf9c69f28f0235ecc82acb07a14f1e3408d7fa7d65cf729e01403f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859697"
---
# <a name="how-to-implement-icon-overlay-handlers"></a>Implementieren von Symbolüberlagerungshandlern

Symbolüberlagerungshandler sind COM-Objekte (In-Process Component Object Model), die als DLLs implementiert werden. Sie exportieren zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)eine Schnittstelle: [**IShellIconOverlayIdentifier**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier). Diese Schnittstelle verfügt über drei Methoden: [**IShellIconOverlayIdentifier::GetOverlayInfo,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) [**IShellIconOverlayIdentifier::GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority)und [**IShellIconOverlayIdentifier::IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof).

## <a name="instructions"></a>Anweisungen

### <a name="step-1-implementing-getoverlayinfo"></a>Schritt 1: Implementieren von GetOverlayInfo

Die [**GetOverlayInfo-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) wird zuerst während der Initialisierung aufgerufen. Die -Methode gibt den vollqualifizierten Pfad der Datei zurück, die das Symbolüberlagerungsbild und den zugehörigen nullbasierten Index in der Datei enthält. Die Shell fügt das Image dann der Systemimageliste hinzu. Symbolüberlagerungen können in allen Standarddateitypen enthalten sein, einschließlich .exe, .dll und ICO.

Nach Abschluss der Initialisierung ruft die Shell [**GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) auf, wenn die Symbolüberlagerung des Handlers angezeigt werden muss. Die Methode sollte den gleichen Dateinamen und Index zurückgeben, den sie während der Initialisierung verwendet hat. Obwohl die Shell das Image verwendet, das in der Systemimageliste zwischengespeichert wird, anstatt das Bild aus der Datei zu laden, wird eine Symbolüberlagerung weiterhin durch den Dateinamen und index identifiziert.

### <a name="step-2-implementing-getpriority"></a>Schritt 2: Implementieren von GetPriority

Die [**GetPriority-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) wird nur während der Initialisierung aufgerufen. Der Symbolüberlagerung des Handlers wird ein Prioritätswert zugewiesen. Der Wert kann zwischen 0 und 100 liegen, wobei 100 die niedrigste Priorität darstellt. Der Zweck dieses Prioritätswerts besteht darin, die Shell bei der Lösung des Konflikts zu unterstützen, der auftritt, wenn mehrere Symbolüberlagerungen für ein einzelnes Objekt angegeben werden. Die Shell verwendet zunächst einen internen Satz von Regeln, um die Symbolüberlagerung mit der höchsten Priorität zu bestimmen. Wenn diese Regeln den Konflikt nicht lösen, bestimmen die Werte, die den Symbolüberlagerungen von **GetPriority** zugewiesen werden, die Priorität.

Der von [**GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) festgelegte Prioritätswert ist keine zuverlässige Möglichkeit, Konflikte zwischen nicht verknüpften Symbolüberlagerungshandlern aufzulösen. Der Handler kann nicht bestimmen, welche Prioritätswerte von anderen Handlern verwendet werden. Normalerweise sollten Sie den Wert auf 0 (null) festlegen. Der Prioritätswert ist jedoch nützlich, wenn Sie zwei oder mehr Symbolüberlagerungshandler implementiert haben, die Symbolüberlagerungssymbole für dasselbe Objekt anfordern können. Indem Sie die Prioritätswerte entsprechend festlegen, können Sie angeben, welche der angeforderten Symbolüberlagerungen angezeigt werden.

### <a name="step-3-implementing-ismemberof"></a>Schritt 3: Implementieren von IsMemberOf

Die Shell ruft die [**IsMemberOf-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof) auf, um zu bestimmen, ob die Symbolüberlagerung eines Handlers für ein bestimmtes Objekt angezeigt werden soll. Die Shell gibt das Objekt an, indem ihr Name an die -Methode übergeben wird. Wenn ein Handler seine Symbolüberlagerung anzeigen lassen möchte, gibt **IsMemberOf** S \_ OK zurück. Wenn nicht, wird S \_ FALSE zurückgegeben.

Symbolüberlagerungshandler sind normalerweise für die Arbeit mit einer bestimmten Gruppe von Dateien vorgesehen. Ein typisches Beispiel ist ein [Dateityp,](fa-file-types.md)der durch eine bestimmte Dateinamenerweiterung identifiziert wird. Ein Symbolüberlagerungshandler kann eine Symbolüberlagerung für alle Dateien des Dateityps anfordern. Einige Handler fordern nur dann eine Symbolüberlagerung an, wenn sich eine Datei des Dateityps in einem bestimmten Zustand befindet. Allerdings können Symbolüberlagerungshandler ihre Symbolüberlagerung für jedes objekt anfordern, das sie auswählen.

 

 
