---
description: Das akkumulierte umschließende Rechteck ist das kleinste Rechteck, das den Teil eines Fensters oder Client Bereichs schließt, der sich auf die letzten Zeichnungsvorgänge auswirkt.
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: Akkumuliertes Rechteck
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ae3237304af68a4b8ff447b7ea2d64d3f81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528400"
---
# <a name="accumulated-bounding-rectangle"></a>Akkumuliertes Rechteck

Das *akkumulierte* umschließende Rechteck ist das kleinste Rechteck, das den Teil eines Fensters oder Client Bereichs schließt, der sich auf die letzten Zeichnungsvorgänge auswirkt. Mithilfe dieses Rechtecks kann eine Anwendung den Umfang der Änderungen, die durch Zeichnungsvorgänge verursacht werden, bequem ermitteln. Sie wird manchmal zusammen mit [**lockwindowupdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) verwendet, um zu bestimmen, welcher Teil des Client Bereichs nach dem Löschen der Update Sperre neu gezeichnet werden muss.

Eine Anwendung verwendet die [**setboundsrect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) -Funktion (durch Angabe \_ von DCB Enable), um mit der Anhäufung des umgebenden Rechtecks zu beginnen. Anschließend sammelt das System Punkte für das umgebende Rechteck, wenn die Anwendung den angegebenen Anzeigegeräte Kontext verwendet. Die Anwendung kann das aktuelle umgebende Rechteck jederzeit mithilfe der [**getboundsrect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) -Funktion abrufen. Die Anwendung beendet die Akkumulation, indem **setboundsrect** erneut aufgerufen wird, wobei der DCB- \_ Wert deaktiviert wird.

 

 



