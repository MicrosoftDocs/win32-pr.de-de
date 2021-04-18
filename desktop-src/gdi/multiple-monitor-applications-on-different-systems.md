---
description: Damit die Anwendung mit mehreren Monitoren sowohl auf Systemen mit als auch ohne Unterstützung mehrerer Monitore funktioniert, verknüpfen Sie Ihre Anwendung mit "multimon. h".
ms.assetid: 8667305e-ca76-49cb-878e-07814431e6db
title: Mehrere Monitor Anwendungen auf verschiedenen Systemen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5d470861136ac9362d986b8647c86abee7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978528"
---
# <a name="multiple-monitor-applications-on-different-systems"></a>Mehrere Monitor Anwendungen auf verschiedenen Systemen

Damit die Anwendung mit mehreren Monitoren sowohl auf Systemen mit als auch ohne Unterstützung mehrerer Monitore funktioniert, verknüpfen Sie Ihre Anwendung mit "multimon. h". Sie müssen auch \_ multitimon- \_ Stub für die Kompilierung in genau einer C-Datei definieren. Wenn das System mehrere Monitore nicht unterstützt, werden Standardwerte von " [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) " zurückgegeben, und die Funktionen mehrerer Monitore fungieren so, als ob nur eine Anzeige vorhanden ist. Auf mehreren Überwachungssystemen funktioniert die Anwendung normal.

Da negative Koordinaten problemlos in einem Multimonitor-System ausgeführt werden können, sollten Sie Koordinaten, die in lParam verpackt sind, mithilfe der Makros **get \_ X \_ LPARAM** und **get \_ Y \_ LPARAM** abrufen.

Verwenden Sie keine negativen Koordinaten oder Koordinaten, die größer als SM \_ cxscreen und SM \_ cyscreen sind, um ein Fenster auszublenden. Windows, die diese Grenzwerte zum Ausblenden verwenden, werden möglicherweise auf einem anderen Monitor angezeigt. Verwenden Sie diese Grenzwerte auch nicht, um ein Fenster sichtbar zu machen, da dies dazu führen kann, dass ein Fenster an den primären Monitor angedostet wird. Es empfiehlt sich, vorhandene Anwendungen auf diese Probleme zu überprüfen. Sie können jedoch Probleme in vorhandenen Anwendungen minimieren, indem Sie die Anwendung auf dem primären Monitor ausführen oder den primären Monitor in der oberen linken Ecke des virtuellen Bildschirms aufbewahren.

Beachten Sie, dass SM \_ cxmaxtrack und SM \_ cymaxtrack für den Desktop und nicht nur für einen Monitor definiert sind. Windows, das diese Grenzen verwendet, muss möglicherweise neu definiert werden.

Ein übergeordnetes oder verwandtes Fenster ist möglicherweise nicht auf dem gleichen Monitor wie ein untergeordnetes Fenster. Zum Auffinden des Monitors eines Fensters sollten Anwendungen die [**monitorfromwindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) -Funktion verwenden.

Um einen Bildschirmschoner auf allen Monitoren anzuzeigen, verknüpfen Sie mit der aktuellen Version von SCRNSAVE. lib. Andernfalls wird der Bildschirmschoner möglicherweise nur auf dem primären Monitor angezeigt, und die anderen Monitore bleiben unverändert. Mit der aktuellen Datei "Scrnsave. lib" verknüpfte Bildschirmschoner funktionieren sowohl für einzelne als auch für mehrere Monitorsysteme. Um für jeden Monitor einen anderen Bildschirmschoner zu verwenden, verwenden Sie die Funktionen mehrerer Monitore, um die einzelnen Monitore separat zu verarbeiten.

Eingabegeräte, die Koordinaten für das System in absoluten Koordinaten (z. b. Tablets) bereitzustellen, haben ihre Cursor Eingabe auf den primären Monitor beschränkt. Informationen zum Wechseln von Tablet-Eingaben zwischen Monitoren finden Sie in den Anweisungen des OEM.

Zum Zuordnen von Maus Eingaben, die in absoluten Koordinaten an den gesamten virtuellen Bildschirm gesendet werden, verwenden Sie die [**Eingabe**](/windows/win32/api/winuser/ns-winuser-input) Struktur mit mouseeventf \_ absolute und mouseeventf \_ virtualdesktop.

Die [**BitBLT**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) -Funktion funktioniert gut für mehrere Monitorsysteme. Die Funktionen [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt), [**plgblt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt), [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)und [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) schlagen jedoch fehl, wenn sich die Quell-und Zielgeräte Kontexte unterscheiden.

 

 
