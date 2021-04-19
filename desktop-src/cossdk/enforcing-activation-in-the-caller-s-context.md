---
description: Erzwingen der Aktivierung im Aufruferkontext
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Erzwingen der Aktivierung im Aufruferkontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70af40f92056e679a9211964b8a614cbeaeb4a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346432"
---
# <a name="enforcing-activation-in-the-callers-context"></a>Erzwingen der Aktivierung im Kontext des Aufrufers

Sie können steuern, ob ein Objekt in seinem eigenen Kontext aktiviert wird. Wenn Sie das Verwaltungs Programmkomponenten Dienste verwenden, um die Komponenten Aktivierung im Kontext des Aufrufers anzufordern, erfolgt Folgendes, wenn com+ eine Instanz der Komponente in einem Kontext aktiviert:

-   Wenn möglich, wird das-Objekt im Kontext des Erstellers aktiviert.
-   Die Objekt Aktivierung schlägt fehl, wenn ein eigener Kontext erforderlich ist. Der \_ \_ Versuch \_ , einen \_ \_ externen Client Kontext zu erstellen, \_ \_ wird zurückgegeben.

Ob das Objekt einen eigenen Kontext erfordert, hängt von seiner Konfiguration relativ zum aktuellen Zustand der Kontexteigenschaften des Aufrufers ab. Weitere Details finden Sie unter [com+-Kontexte](com--contexts.md).

Wenn ein anderer Aspekt des Objekts nicht ordnungsgemäß funktioniert, sollten Sie die Aktivierung auf dieser Ebene steuern. Wenn die Komponente z. b. kein Marshalling unterstützt und Ihr eigener Kontext vorhanden ist, schlagen alle Aufrufe fehl, da Kontext übergreifende Aufrufe abgefangen und ein Lightweight-Marshal ausgeführt wird.

**So erzwingen Sie die Aktivierung im Kontext des Aufrufers**

1.  Klicken Sie im Detailbereich des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die Komponente (befindet sich im Ordner **Komponenten** der ausgewählten COM+-Anwendung), für die Sie Aktivierungs Eigenschaften festlegen, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Aktivierung** .

3.  Aktivieren Sie das Kontrollkästchen **muss im Kontext des aufruferaufrufern aktiviert werden** .

4.  Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte für die Just-in-Time-Aktivierung in com+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Erzwingen der Aktivierung im Standardkontext](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



