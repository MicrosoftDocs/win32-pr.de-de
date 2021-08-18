---
description: Damit Ihre Anwendung mit mehreren Monitorawares sowohl auf Systemen mit als auch ohne Unterstützung mehrerer Monitore funktioniert, verknüpfen Sie Ihre Anwendung mit Multimon.h.
ms.assetid: 8667305e-ca76-49cb-878e-07814431e6db
title: Mehrere Monitoranwendungen auf unterschiedlichen Systemen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c597261063f49b6e6856576e3528698291348afb2b8478d854a824b92d2cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037718"
---
# <a name="multiple-monitor-applications-on-different-systems"></a>Mehrere Monitoranwendungen auf unterschiedlichen Systemen

Damit Ihre Anwendung mit mehreren Monitorawares sowohl auf Systemen mit als auch ohne Unterstützung mehrerer Monitore funktioniert, verknüpfen Sie Ihre Anwendung mit Multimon.h. Außerdem müssen Sie COMPILE \_ MULTIMON \_ STUBS in genau einer C-Datei definieren. Wenn das System nicht mehrere Monitore unterstützt, gibt dies Standardwerte von [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) zurück, und die verschiedenen Monitorfunktionen fungieren so, als ob nur eine Anzeige zur Verfügung steht. Auf mehreren Überwachungssystemen funktioniert Ihre Anwendung normal.

Da negative Koordinaten in einem System mit mehreren Monitoren leicht vorkommen können, sollten Sie koordinaten, die im lParam gepackt sind, mithilfe der **Get \_ X \_ LPARAM-** und **GET \_ Y \_ LPARAM-Makros** abrufen.

Verwenden Sie keine negativen Koordinaten oder Koordinaten, die größer als SM CXSCREEN und \_ SM \_ CYSCREEN sind, um ein Fenster auszublenden. Windows, die diese Grenzwerte zum Ausblenden verwenden, werden möglicherweise auf einem anderen Monitor angezeigt. Verwenden Sie diese Grenzwerte nicht, um ein Fenster sichtbar zu halten, da dies dazu führen kann, dass ein Fenster am primären Monitor angezeigt wird. Es ist am besten, vorhandene Anwendungen für diese Probleme erneut zu verwenden. Sie können jedoch Probleme in vorhandenen Anwendungen minimieren, indem Sie die Anwendung auf dem primären Monitor ausführen oder den primären Monitor in der oberen linken Ecke des virtuellen Bildschirms befingen.

Beachten Sie, dass SM \_ CXMAXTRACK und SM CYMAXTRACK nicht nur für einen Monitor, sondern für den \_ Desktop definiert sind. Windows verwendung dieser Grenzwerte müssen möglicherweise neu definiert werden.

Ein übergeordnetes oder verwandtes Fenster ist möglicherweise nicht auf demselben Monitor wie ein untergeordnetes Fenster. Um den Monitor eines Fensters zu suchen, sollten Anwendungen die [**MonitorFromWindow-Funktion**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) verwenden.

Damit ein Bildschirmschoner auf allen Monitoren angezeigt wird, verknüpfen Sie die Datei mit der neuesten Version von "Scrnsave.lib". Andernfalls wird der Bildschirmschoner möglicherweise nur auf dem primären Monitor angezeigt, und die anderen Monitore bleiben unverändert. Bildschirmschoner, die mit der neuesten Datei "Scrnsave.lib" verknüpft sind, funktionieren sowohl auf einzel- als auch auf mehreren Überwachungssystemen. Um einen anderen Bildschirmschoner auf jedem Monitor zu verwenden, verwenden Sie die verschiedenen Monitorfunktionen, um jeden Monitor separat zu verarbeiten.

Eingabegeräte, die Koordinaten in absoluten Koordinaten an das System liefern, z. B. Tablets, haben ihre Cursoreingabe auf den primären Monitor beschränkt. Informationen zum Wechseln der Tableteingabe zwischen Monitoren finden Sie in den Anweisungen des OEM.

Verwenden Sie die [**INPUT-Struktur**](/windows/win32/api/winuser/ns-winuser-input) mit \_ MOUSEEVENTF ABSOLUTE und MOUSEEVENTF VIRTUALDESKTOP, um Mauseingaben, die in absoluten Koordinaten gesendet werden, dem gesamten virtuellen Bildschirm \_ zu zuordnen.

Die [**BitBlt-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) funktioniert gut für mehrere Überwachungssysteme. Die Funktionen [**MaskBlt,**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt) [**PlgBlt,**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)und [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) können jedoch nicht verwendet werden, wenn sich die Quell- und Zielgerätekontexte unterscheiden.

 

 
