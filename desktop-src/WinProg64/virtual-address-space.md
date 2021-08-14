---
title: Virtueller Adressraum (Programmierhandbuch für 64-Bit-Windows)
description: Standardmäßig verfügen 64-Bit-Microsoft Windows-basierte Anwendungen über einen Adressraum im Benutzermodus von mehreren Terabytes.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- 64-Bit-Windows-Programmierhandbuch 64-Bit-Windows Programmierung, virtueller Adressraum
- 64-Bit-Windows-Programmierung des virtuellen Adressraums
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2e673befb66c45501558effb37f3d04ee1a99199010f8cca89abb2cb31c6d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113370"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a>Virtueller Adressraum (Programmierhandbuch für 64-Bit-Windows)

Standardmäßig verfügen 64-Bit-Microsoft Windows-basierte Anwendungen über einen Adressraum im Benutzermodus von mehreren Terabytes. Genaue Werte finden Sie unter [Arbeitsspeicherlimits für Windows und Windows Serverversionen.](/windows/desktop/Memory/memory-limits-for-windows-releases) Anwendungen können jedoch angeben, dass das System den gesamten Arbeitsspeicher für die Anwendung unter 2 GIGABYTE zuordnen soll. Dieses Feature ist für 64-Bit-Anwendungen vorteilhaft, wenn die folgenden Bedingungen zutreffen:

-   Ein Adressraum von 2 GB ist ausreichend.
-   Der Code enthält viele Warnungen zum Abschneiden von Zeigern.
-   Zeiger und ganze Zahlen werden frei gemischt.
-   Der Code weist Polymorphie mit 32-Bit-Datentypen auf.

Alle Zeiger sind immer noch 64-Bit-Zeiger, aber das System stellt sicher, dass jede Speicherbelegung unterhalb des Grenzwerts von 2 GB erfolgt, sodass keine signifikanten Daten verloren gehen, wenn die Anwendung einen Zeiger abschneidet. Zeiger können auf 32-Bit-Werte abgeschnitten und dann durch Vorzeichenerweiterung oder 0 -Erweiterung auf 64-Bit-Werte erweitert werden.

Um diese Speicherbeschränkung anzugeben, verwenden Sie die Linkeroption **/LARGEADDRESSAWARE:NO.** Beachten Sie, dass **/LARGEADDRESSAWARE:NO** für eine ARM64-Binärdatei ignoriert wird. Beachten Sie jedoch, dass probleme auftreten können, wenn Sie diese Option verwenden. Wenn Sie eine DLL erstellen, die diese Option verwendet, und die DLL von einer Anwendung aufgerufen wird, die diese Option nicht verwendet, kann die DLL einen 64-Bit-Zeiger abschneiden, dessen obere 32 Bits von Bedeutung sind. Dies kann zu Anwendungsfehlern ohne Warnung führen.

 

 
