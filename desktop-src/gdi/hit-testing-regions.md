---
description: Eine Anwendung führt Treffertests für Bereiche durch, um die Koordinaten der aktuellen Cursorposition zu bestimmen.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Treffertestbereiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5734ffb886bd2978d3ee0b49773d752d4abf43a4d98dc060f3dfaf2956e3084a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760976"
---
# <a name="hit-testing-regions"></a>Treffertestbereiche

Eine Anwendung führt Treffertests für Bereiche durch, um die Koordinaten der aktuellen Cursorposition zu bestimmen. Anschließend werden diese Koordinaten sowie ein Handle zur Identifizierung des Bereichs an die [**PtInRegion-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) übergeben. Die Cursorkoordinaten können abgerufen werden, indem die verschiedenen Mausmeldungen wie [**WM \_ LBUTTONDOWN,**](../inputdev/wm-lbuttondown.md) [**WM \_ LBUTTONUP,**](../inputdev/wm-lbuttonup.md) [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) und [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md)verarbeitet werden. Der Rückgabewert für PtInRegion gibt an, ob sich die Cursorposition innerhalb des angegebenen Bereichs befindet.

 

 
