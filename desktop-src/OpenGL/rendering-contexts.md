---
title: Renderingkontexte
description: Ein OpenGL-renderingkontext ist ein Port, über den alle OpenGL-Befehle bestanden werden. Jeder Thread, der OpenGL-Aufrufe ausführt, muss über einen aktuellen renderingkontext verfügen. Renderingkontexte verknüpfen OpenGL mit den Windows-windowingsystemen.
ms.assetid: 9fbbb0be-2db4-4bfc-9a5c-a43d71554abc
keywords:
- OpenGL unter Windows, renderingkontexte
- Rendern von Kontexten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ac2ac6c5948da2b7372d600377666cd9e4e074
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310532"
---
# <a name="rendering-contexts"></a>Renderingkontexte

Ein OpenGL- *renderingkontext* ist ein Port, über den alle OpenGL-Befehle bestanden werden. Jeder Thread, der OpenGL-Aufrufe ausführt, muss über einen aktuellen renderingkontext verfügen. Renderingkontexte verknüpfen OpenGL mit den Windows-windowingsystemen.

Eine Anwendung gibt einen Windows-Gerätekontext an, wenn ein renderingkontext erstellt wird. Dieser renderingkontext eignet sich zum Zeichnen auf dem Gerät, auf das der angegebene Gerätekontext verweist. Insbesondere hat der renderingkontext das gleiche Pixel Format wie der Gerätekontext. Weitere Informationen finden Sie unter [Rendern von Kontextfunktionen](rendering-context-functions.md).

Trotz dieser Beziehung ist ein renderingkontext nicht mit einem Gerätekontext identisch. Ein Gerätekontext enthält Informationen, die für die Grafik Komponente (GDI) von Windows relevant sind. Ein renderingkontext enthält Informationen, die für OpenGL relevant sind. Ein Gerätekontext muss explizit in einem GDI-Befehl angegeben werden. Ein renderingkontext ist in einem OpenGL-Befehl implizit. Vor dem Erstellen eines renderingkontexts sollten Sie das Pixel Format eines Geräte Kontexts festlegen.

Ein Thread, der OpenGL-Aufrufe ausführt, muss über einen aktuellen renderingkontext verfügen. Wenn eine Anwendung OpenGL-Aufrufe von einem Thread durchführt, der keinen aktuellen renderingkontext hat, geschieht nichts. der-Befehl hat keine Auswirkung. Eine Anwendung erstellt in der Regel einen renderingkontext, legt sie als aktuellen renderingkontext eines Threads fest und ruft dann OpenGL-Funktionen auf. Wenn der Aufruf von OpenGL-Funktionen abgeschlossen ist, entkoppelt die Anwendung den renderingkontext aus dem Thread und löscht dann den renderingkontext. Ein Fenster kann mehrere renderingkontexte gleichzeitig zeichnen, aber ein Thread kann nur über einen aktuellen aktiven renderingkontext verfügen.

Ein aktueller renderingkontext verfügt über einen zugeordneten Gerätekontext. Dieser Gerätekontext muss nicht der gleiche Gerätekontext sein, den er beim Erstellen des renderingkontexts verwendet hat, er muss jedoch auf dasselbe Gerät verweisen und das gleiche Pixel Format aufweisen.

Ein Thread kann nur über einen aktuellen renderingkontext verfügen. Ein renderingkontext kann nur auf einen Thread aktuell sein.

 

 




