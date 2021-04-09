---
title: Eingabe des passiven Zustands
description: Eingabe des passiven Zustands
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f98a30117174c5953c19cc9e1092ebf79403e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856780"
---
# <a name="entering-the-passive-state"></a>Eingabe des passiven Zustands

Die Objekt Schließung erzwingt ein eingebettetes oder verknüpftes Objekt in den passiven Zustand. Sie wird in der Regel von der Benutzeroberfläche der OLE Server-Anwendung initiiert, z. b. wenn der Benutzer den Befehl zum Schließen der Datei auswählt. In diesem Fall benachrichtigt die OLE Server-Anwendung den Container, der seinen Verweis Zähler für das Objekt freigibt. Wenn alle Verweise auf das Objekt freigegeben wurden, kann das Objekt freigegeben werden. Wenn alle Objekte freigegeben wurden, kann die OLE-Serveranwendung sicher beendet werden.

Eine Containeranwendung kann auch die Objekt Schließung initiieren. Um ein Objekt zu schließen, gibt der Container seinen Verweis Zähler frei, nachdem ein optionaler Speichervorgang abgeschlossen wurde. Sie können Container so entwerfen, dass Objekte freigegeben werden, wenn Sie nach einer direkten Aktivierungs Sitzung deaktiviert werden, sodass der Benutzer außerhalb des Objekts auf das Objekt klicken kann, ohne die aktive Bearbeitungs Sitzung zu verlieren.

 

 




