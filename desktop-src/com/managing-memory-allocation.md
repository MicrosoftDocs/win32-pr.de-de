---
title: Verwalten der Speicherbelegung
description: Verwalten der Speicherbelegung
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bb77ae0b425296100dc0520a44d942d29ba0fea78c143e329cc77be94eceef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118105408"
---
# <a name="managing-memory-allocation"></a>Verwalten der Speicherbelegung

In COM werden viele , wenn nicht die meisten Schnittstellenmethoden von Code aufgerufen, der von einer Programmierorganisation geschrieben und von Code implementiert wird, der von einer anderen geschrieben wurde. Viele der Parameter und Rückgabewerte dieser Funktionen sind von Typen, die als Wert übergeben werden können. Manchmal ist es jedoch notwendig, Datenstrukturen zu übergeben, für die dies nicht der Fall ist. Daher ist es erforderlich, dass sowohl der Aufrufer als auch der Aufgerufene über eine kompatible Zuordnungs- und Zuordnungsaufbelegungsrichtlinie verfügen. COM definiert eine universelle Konvention für die Speicherbelegung, da dies sinnvoller ist als das Definieren von Fall-für-Fall-Regeln, sodass die Implementierung des COM-Remoteprozeduraufrufs den Arbeitsspeicher ordnungsgemäß verwalten kann.

Die Methoden einer COM-Schnittstelle stellen immer die Speicherverwaltung von Zeigern auf die Schnittstelle bereit, indem sie die [**AddRef-**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) und [**Release-Funktionen**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) in der [**IUnknown-Schnittstelle**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) aufrufen, von der alle anderen COM-Schnittstellen abgeleitet werden. (Weitere Informationen finden Sie unter [Regeln zum Verwalten der Verweisanzahl.)](rules-for-managing-reference-counts.md)

In diesem Abschnitt wird nur beschrieben, wie Speicher für Parameter belegt wird, die nicht als Wert übergeben werden– keine Zeiger auf Schnittstellen, sondern eher alltägliche Dinge wie Zeichenfolgen, Zeiger auf Strukturen usw.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Die OLE-Speicherbezuweisung](the-ole-memory-allocator.md)
-   [Speicherverwaltungsregeln](memory-management-rules.md)
-   [Debuggen von Speicherbelegungen](debugging-memory-allocations.md)

 

 