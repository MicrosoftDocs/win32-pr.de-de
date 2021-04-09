---
description: 'Direct3D-Anwendungen können in einem von zwei Modi ausgeführt werden: Vollbild oder Fenster.'
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: Fenster-vs-Full-Screen Modus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf51c641446d3f54ceb37c9cc1ac629604f68400
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123848"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a>Fenster-vs-Full-Screen Modus (Direct3D 9)

Direct3D-Anwendungen können in einem von zwei Modi ausgeführt werden: Vollbild oder Fenster.

Der Vollbildmodus bedeutet, dass das Fenster, in dem die Anwendung ausgeführt wird, den gesamten Desktop abdeckt und alle ausgeführten Anwendungen (einschließlich Ihrer Entwicklungsumgebung) verbirgt. Spiele werden in der Regel standardmäßig auf den Vollbildmodus festgestellt, um den Benutzer vollständig in das Spiel zu eintauchen Eine Anwendung, die im Fenstermodus ausgeführt wird, teilt den Desktop mit allen laufenden Anwendungen. Code Unterschiede zwischen dem Vollbildmodus und dem Fenstermodus sind sehr gering.

Da eine Anwendung, die im Vollbildmodus ausgeführt wird, den Bildschirm übernimmt, erfordert das Debuggen der Anwendung entweder einen separaten Monitor oder einen Remote Debugger. Verwenden Sie das [System Steuerungs Tool DirectX](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) , um das Debuggen mit mehreren Monitoren zu aktivieren. Ein Vorteil einer Anwendung im Windowed-Modus besteht darin, dass Sie den Code in einem Debugger ohne mehrere Monitore oder einen Remote Debugger schrittweise durchlaufen können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 



