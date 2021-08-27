---
title: Verwenden der Rückrufmethoden
description: Verwenden der Rückrufmethoden
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- Windows Medienformat-SDK, Rückrufmethoden
- Windows Medienformat-SDK, asynchron aufgerufene Methoden
- Rückrufmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ee2bcf6587e2e9e75e18404a60c3b85fb4bac5e9f14fd0164304bcc3f3338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110060"
---
# <a name="using-the-callback-methods"></a>Verwenden der Rückrufmethoden

Mehrere Schnittstellen im Windows Media Format SDK enthalten Methoden, die asynchron aufgerufen werden. Die meisten dieser Methoden verwenden Rückruffunktionen, um Informationen an die steuernde Anwendung zu übergeben.

In den folgenden Abschnitten werden einige allgemeine Probleme in Bezug auf die Verwendung von Rückrufmethoden mit dem Windows Media Format SDK beschrieben.



| `Section`                                                                          | BESCHREIBUNG                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Verwenden des OnStatus-Rückrufs](using-the-onstatus-callback.md)                   | Beschreibt, wie die [**IWMStatusCallback::OnStatus-Rückrufmethode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) implementiert wird, die von mehreren -Objekten verwendet wird, um Anwendungen über den Fortschritt des SDK-Vorgangs zu informieren. |
| [Verwenden von Ereignissen mit asynchronen Aufrufen](using-events-with-asynchronous-calls.md) | Beschreibt eine gängige Technik zum Verarbeiten asynchroner Methodenaufrufe in einer Anwendung.                                                                                                                  |
| [Verwenden des Kontextparameters](using-the-context-parameter.md)                   | Führt den *pvContext-Parameter* ein, der von mehreren Rückrufen und deren aufrufenden Methoden gemeinsam verwendet wird, und erläutert die Verwendung.                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 




