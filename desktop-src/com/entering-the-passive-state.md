---
title: Eingabe des passiven Zustands
description: Eingabe des passiven Zustands
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a0a3a93b0ff0bd1c16701c82f271847ee435375112a8e7a03120155928fe1ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736854"
---
# <a name="entering-the-passive-state"></a>Eingabe des passiven Zustands

Der Objektabschluss erzwingt den passiven Zustand eines eingebetteten oder verknüpften Objekts. Sie wird in der Regel über die Benutzeroberfläche der OLE-Serveranwendung initiiert, z. B. wenn der Benutzer den Befehl Datei schließen auswählt. In diesem Fall benachrichtigt die OLE-Serveranwendung den Container, der seinen Verweiszähler für das Objekt freigibt. Wenn alle Verweise auf das Objekt freigegeben wurden, kann das Objekt freigegeben werden. Wenn alle Objekte freigegeben wurden, kann die OLE-Serveranwendung sicher beendet werden.

Eine Containeranwendung kann auch den Objektabschluss initiieren. Um ein Objekt zu schließen, gibt der Container seinen Verweiszähler frei, nachdem ein optionaler Speichervorgang abgeschlossen wurde. Sie können Container so entwerfen, dass sie Objekte freigeben, wenn sie nach einer aktiven Aktivierungssitzung deaktiviert werden, sodass der Benutzer außerhalb des Objekts klicken kann, ohne die aktive Bearbeitungssitzung zu verlieren.

 

 




