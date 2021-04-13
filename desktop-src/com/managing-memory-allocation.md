---
title: Verwalten der Speicher Belegung
description: Verwalten der Speicher Belegung
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2af04b4ecc5b8480230b17ae710b84ce8e6ce5d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391090"
---
# <a name="managing-memory-allocation"></a>Verwalten der Speicher Belegung

In com werden viele, wenn nicht die meisten, Schnittstellen Methoden von Code aufgerufen, der von einer Programmier Organisation geschrieben und durch Code implementiert wird, der von einem anderen geschrieben wurde. Viele Parameter und Rückgabewerte dieser Funktionen sind Typen, die als Wert umgegeben werden können. Manchmal ist es jedoch erforderlich, Datenstrukturen zu übergeben, für die dies nicht der Fall ist. Daher ist es erforderlich, dass sowohl der Aufrufer als auch der Aufruf einer kompatiblen Zuordnungs-und Aufhebung der Zuordnungs Richtlinie ausgeführt wird. COM definiert eine universelle Konvention für die Speicher Belegung, da dies sinnvoller ist als das Definieren von Regeln für die Groß-/Kleinschreibung und die Implementierung des com-remote Prozedur Aufrufes.

Die Methoden einer COM-Schnittstelle bieten immer eine Speicherverwaltung von Zeigern auf die-Schnittstelle, indem die [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -und [**releasefunktionen**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) aufgerufen werden, die in der [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle gefunden werden, von der alle anderen com- (Weitere Informationen finden Sie unter [Regeln zum Verwalten der Verweis Anzahl](rules-for-managing-reference-counts.md) .)

In diesem Abschnitt wird nur beschrieben, wie Arbeitsspeicher für Parameter belegt wird, die nicht als Wert weitergereicht werden – nicht als Zeiger auf Schnittstellen, sondern um mehr alltägliche Dinge, wie z. b. Zeichen folgen, Zeiger auf Strukturen usw.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Die OLE-Speicherzuweisung](the-ole-memory-allocator.md)
-   [Speicher Verwaltungsregeln](memory-management-rules.md)
-   [Debugging von Speicher Belegungen](debugging-memory-allocations.md)

 

 