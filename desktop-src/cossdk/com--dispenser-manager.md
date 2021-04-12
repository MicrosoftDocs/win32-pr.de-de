---
description: Der Dispenser-Manager stellt Ressourcen Pooling für die Ressourcen Spender bereit und stellt sicher, dass eine von einem Ressourcen Verteiler bereitgestellte Ressource ordnungsgemäß in der Anwendungs Objekt Transaktion eingetragen ist.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: Com+-Dispenser-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2422b7debb8ee12ed97444f3b16f31e663e1e71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523579"
---
# <a name="com-dispenser-manager"></a>Com+-Dispenser-Manager

Der Dispenser-Manager bietet Ressourcen Pooling für die Ressourcen Spender und stellt sicher, dass eine von einem Ressourcen Verteiler bereitgestellte Ressource ordnungsgemäß in der Transaktion des Anwendungs Objekts eingetragen ist. Der Dispenser-Manager gibt automatisch Ressourcen frei, die noch am Ende der Lebensdauer eines Objekts reserviert sind, wodurch die Wahrscheinlichkeit von Ressourcenverlusten entfällt. Der Dispenser Manager kann einen Ressourcen Verteiler bitten, eine neue Ressource zu erstellen oder im Leerlauf befindliche Ressourcen zu zerstören, wenn dies erforderlich ist, um Inventur Ebenen anzupassen, anstatt statische Einstellungen zu verwenden.

> [!Note]  
> Da Ressourcen Verteiler Schnittstellen, die für die Anwendung verfügbar gemacht werden, keine COM-Schnittstellen sein müssen, kann der Dispenser-Manager in einem Prozess verwendet werden, ohne com zu initialisieren, z. b. zur Unterstützung des ODBC-Ressourcen Verteilers.

 

Bei der Erstellung von Ressourcen kann der Ressourcen Verteiler angeben, wie lange eine Leerlauf Ressource im Pool verbleiben darf, bevor Sie zerstört wird. Ein Thread, der im Dispenser-Manager ausgeführt wird, sucht immer nach diesen im Leerlauf befindlichen Ressourcen.

## <a name="the-inventory-statistics-manager"></a>Der Inventur Statistik-Manager

Der Dispenser-Manager verwendet den *Inventur Statistik-Manager* zum Verwalten der Ressourcen Inventur Ebenen des Pools. Der Inventur Statistik-Manager verwaltet einen Datensatz darüber, wann die einzelnen Ressourcen verwendet wurden, und entfernt Ressourcen aus dem Inventar, wenn Sie nicht für *x* Sekunden verwendet wurden, wobei der Wert von *x* für jede Ressource festgelegt wird, wenn die Ressource erstellt wird.

## <a name="the-holder-component"></a>Die Inhaber Komponente

Der Dispenser-Manager fragt jeden einzelnen *Inhaber* ab, eine Komponente, die vom Dispenser Manager erstellt wird und die den Ressourcen bestand für jeden Ressourcen Verteiler alle 10 Sekunden auflistet, damit er die Ressourcen Inventur nur noch lesen kann. Jeder Inhaber Ruft den Inventur Statistik-Manager auf, um Inventur Ebenen für jeden Ressourcentyp vorzuschlagen. Demzufolge kann der Inhaber den Ressourcen Verteiler auffordern, eine Inventur zu erstellen oder zu zerstören.

Der Inhaber und der Ressourcen Spender kommunizieren mit den Anforderungs Ressourcen eines bestimmten Typs. Zwischen dem Inhaber und dem Ressourcen Verteiler bestehen folgende Beziehungen:

-   Der Inhaber kann eine Ressource vom Ressourcen Verteiler anfordern. Der Ressourcen Spender gibt entweder eine verfügbare Ressource zurück oder erstellt eine neue Ressource.
-   Der Inhaber kann den Ressourcen Verteiler Benachrichtigen, dass eine Anwendung keine Ressource mehr benötigt, und Sie dann an den Ressourcenpool zurückgeben.
-   Der Inhaber und der Ressourcen Verteiler arbeiten zusammen, um die Größe des Ressourcenpools beizubehalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte des com+-Ressourcen Verteilers](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



