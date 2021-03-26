---
description: Eine Anwendung führt Treffer Tests für Regionen durch, um die Koordinaten der aktuellen Cursorposition zu bestimmen.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Treffer Testregionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe136c3ba9ab4babfc1150ae4c3eee878cb42327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215197"
---
# <a name="hit-testing-regions"></a>Treffer Testregionen

Eine Anwendung führt Treffer Tests für Regionen durch, um die Koordinaten der aktuellen Cursorposition zu bestimmen. Anschließend übergibt Sie diese Koordinaten sowie ein Handle, das den Bereich an die [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) -Funktion identifiziert. Die Cursor Koordinaten können abgerufen werden, indem die verschiedenen Maus Meldungen verarbeitet werden, z. b. [**WM \_ lbuttondown**](../inputdev/wm-lbuttondown.md) , [**WM \_ lbuttonup**](../inputdev/wm-lbuttonup.md) , [**WM \_ rbuttondown**](../inputdev/wm-rbuttondown.md) und [**WM \_ rbuttonup**](../inputdev/wm-rbuttonup.md). Der Rückgabewert für PtInRegion gibt an, ob die Cursorposition innerhalb des angegebenen Bereichs liegt.

 

 
