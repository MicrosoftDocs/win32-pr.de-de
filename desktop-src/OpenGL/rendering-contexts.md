---
title: Renderingkontexte
description: Ein OpenGL-Renderingkontext ist ein Port, über den alle OpenGL-Befehle übergeben werden. Jeder Thread, der OpenGL-Aufrufe macht, muss über einen aktuellen Renderingkontext verfügen. Renderingkontexte verknüpfen OpenGL mit Windows Fenstersystemen.
ms.assetid: 9fbbb0be-2db4-4bfc-9a5c-a43d71554abc
keywords:
- OpenGL auf Windows,Renderingkontexte
- Renderingkontexte OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51167161662501f8aaaca6a392b2efc84217be139842c343056746abf0c35161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011948"
---
# <a name="rendering-contexts"></a>Renderingkontexte

Ein *OpenGL-Renderingkontext* ist ein Port, über den alle OpenGL-Befehle übergeben werden. Jeder Thread, der OpenGL-Aufrufe macht, muss über einen aktuellen Renderingkontext verfügen. Renderingkontexte verknüpfen OpenGL mit Windows Fenstersystemen.

Eine Anwendung gibt einen Windows gerätekontext an, wenn sie einen Renderingkontext erstellt. Dieser Renderingkontext eignet sich zum Zeichnen auf dem Gerät, auf das der angegebene Gerätekontext verweist. Insbesondere hat der Renderingkontext das gleiche Pixelformat wie der Gerätekontext. Weitere Informationen finden Sie unter [RenderingKontextfunktionen](rendering-context-functions.md).

Trotz dieser Beziehung ist ein Renderingkontext nicht identisch mit einem Gerätekontext. Ein Gerätekontext enthält Informationen, die für die Grafikkomponente (GDI) des Windows. Ein Renderingkontext enthält Informationen, die für OpenGL relevant sind. Ein Gerätekontext muss explizit in einem GDI-Aufruf angegeben werden. Ein Renderingkontext ist implizit in einem OpenGL-Aufruf. Sie sollten das Pixelformat eines Gerätekontexts festlegen, bevor Sie einen Renderingkontext erstellen.

Ein Thread, der OpenGL-Aufrufe macht, muss über einen aktuellen Renderingkontext verfügen. Wenn eine Anwendung OpenGL-Aufrufe aus einem Thread ohne aktuellen Renderingkontext vor sich geht, geschieht nichts. der Aufruf hat keine Auswirkungen. Eine Anwendung erstellt in der Regel einen Renderingkontext, legt ihn als aktuellen Renderingkontext eines Threads fest und ruft dann OpenGL-Funktionen auf. Wenn der Aufruf von OpenGL-Funktionen abgeschlossen ist, entfällt die Anwendung den Renderingkontext aus dem Thread und löscht dann den Renderingkontext. Ein Fenster kann mehrere Renderingkontexte gleichzeitig haben, aber ein Thread kann nur einen aktuellen, aktiven Renderingkontext haben.

Einem aktuellen Renderingkontext ist ein Gerätekontext zugeordnet. Dieser Gerätekontext muss nicht mit dem Gerätekontext identisch sein, der beim Erstellen des Renderingkontexts verwendet wurde. Er muss jedoch auf dasselbe Gerät verweisen und das gleiche Pixelformat haben.

Ein Thread kann nur einen aktuellen Renderingkontext haben. Ein Renderingkontext kann nur für einen Thread aktuell sein.

 

 




