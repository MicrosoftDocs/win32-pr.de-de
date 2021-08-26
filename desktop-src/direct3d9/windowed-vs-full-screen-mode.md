---
description: 'Direct3D-Anwendungen können in einem der beiden Modi ausgeführt werden: im Vollbildmodus oder im Fenstermodus.'
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: Fenster- und Full-Screen Modus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a845c464e6c402c46cc4aff09196ccfde65ad90371187045b0c14c41315a9f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025750"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a>Fenster- und Full-Screen Modus (Direct3D 9)

Direct3D-Anwendungen können in einem der beiden Modi ausgeführt werden: im Vollbildmodus oder im Fenstermodus.

Vollbildmodus bedeutet, dass das Fenster, in dem die Anwendung ausgeführt wird, den gesamten Desktop abdeckt und alle ausgeführten Anwendungen (einschließlich Ihrer Entwicklungsumgebung) ausblenden. Spiele verwenden in der Regel den Vollbildmodus, um den Benutzer vollständig im Spiel zu beeindrucken, indem alle ausgeführten Anwendungen verborgen werden. Eine Anwendung, die im Fenstermodus ausgeführt wird, teilt den Desktop mit allen ausgeführten Anwendungen. Die Codeunterschiede zwischen Vollbildmodus und Fenstermodus sind sehr klein.

Da eine Anwendung, die im Vollbildmodus ausgeführt wird, den Bildschirm übernimmt, erfordert das Debuggen der Anwendung entweder einen separaten Monitor oder die Verwendung eines Remotedebuggers. Verwenden Sie [das DirectX Systemsteuerung Tool, um](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) das Debuggen mehrerer Monitore zu aktivieren. Ein Vorteil einer Anwendung im Fenstermodus ist, dass Sie den Code in einem Debugger ohne mehrere Monitore oder einen Remotedebugger schrittweise ausführen können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 



