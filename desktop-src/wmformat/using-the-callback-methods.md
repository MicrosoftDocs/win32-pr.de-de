---
title: Verwenden der Rückruf Methoden
description: Verwenden der Rückruf Methoden
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- Windows Media-Format-SDK, Rückruf Methoden
- Windows Media-Format-SDK, Methoden, die asynchron aufgerufen werden
- Rückrufmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39201c101c9031a7157f79f6c12ec88f07decfc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723416"
---
# <a name="using-the-callback-methods"></a>Verwenden der Rückruf Methoden

Mehrere Schnittstellen im Windows Media Format SDK enthalten Methoden, die asynchron aufgerufen werden. Die meisten dieser Methoden verwenden Rückruf Funktionen, um Informationen an die steuernde Anwendung zu übergeben.

In den folgenden Abschnitten werden einige allgemeine Probleme im Zusammenhang mit der Verwendung von Rückruf Methoden mit dem Windows Media-Format-SDK beschrieben.



| `Section`                                                                          | BESCHREIBUNG                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Verwenden des OnStatus-Rückrufs](using-the-onstatus-callback.md)                   | Beschreibt das Implementieren der [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode, die von mehreren-Objekten verwendet wird, um den Fortschritt des SDK-Vorgangs zu informieren. |
| [Verwenden von Ereignissen mit asynchronen Aufrufen](using-events-with-asynchronous-calls.md) | Beschreibt ein gängiges Verfahren zum Verarbeiten von asynchronen Methoden aufrufen in einer Anwendung.                                                                                                                  |
| [Verwenden des Kontext Parameters](using-the-context-parameter.md)                   | Führt den *pvcontext* -Parameter ein, der von mehreren Rückrufen und deren Aufruf Methoden gemeinsam genutzt wird, und erläutert, wie er verwendet werden kann.                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 




