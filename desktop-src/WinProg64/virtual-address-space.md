---
title: Virtueller Adressraum (Programmier Handbuch für 64-Bit-Windows)
description: Standardmäßig haben 64-Bit-Microsoft Windows-basierte Anwendungen einen Adressraum im Benutzermodus von mehreren Terabytes.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, virtueller Adressraum
- virtueller Adressraum 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e4aa6eb67ebf931d1152b3a1101df2757e899b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039910"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a>Virtueller Adressraum (Programmier Handbuch für 64-Bit-Windows)

Standardmäßig haben 64-Bit-Microsoft Windows-basierte Anwendungen einen Adressraum im Benutzermodus von mehreren Terabytes. Genaue Werte finden Sie unter Arbeits [Speicher Grenzwerte für Windows-und Windows Server-Releases](/windows/desktop/Memory/memory-limits-for-windows-releases). Anwendungen können jedoch angeben, dass das System den gesamten Arbeitsspeicher für die Anwendung unterhalb von 2 Gigabyte zuordnen soll. Diese Funktion ist für 64-Bit-Anwendungen vorteilhaft, wenn die folgenden Bedingungen zutreffen:

-   Ein 2-GB-Adressraum ist ausreichend.
-   Der Code weist viele Warnungen für das Abschneiden von Zeigern auf.
-   Zeiger und ganze Zahlen sind frei gemischt.
-   Der Code weist Polymorphie mithilfe von 32-Bit-Datentypen auf.

Alle Zeiger sind immer noch 64-Bit-Zeiger, aber das System stellt sicher, dass jede Speicher Belegung unter dem Grenzwert von 2 GB liegt, sodass, wenn die Anwendung einen Zeiger abschneidet, keine signifikanten Daten verloren gehen. Zeiger können auf 32-Bit-Werte gekürzt und dann auf 64-Bit-Werte durch Vorzeichen Erweiterung oder NULL erweitert werden.

Um diese Speicherbeschränkung anzugeben, verwenden Sie die Option **/LARGEADDRESSAWARE: No** Linker. Beachten Sie, dass **/LARGEADDRESSAWARE: No** für eine ARM64-Binärdatei ignoriert wird. Beachten Sie jedoch, dass Probleme auftreten können, wenn Sie diese Option verwenden. Wenn Sie eine DLL erstellen, die diese Option verwendet, und die dll von einer Anwendung aufgerufen wird, die diese Option nicht verwendet, kann die dll einen 64-Bit-Zeiger abschneiden, dessen obere 32 Bits wichtig sind. Dies kann zu einem Anwendungsfehler führen, ohne dass eine Warnung vorliegt.

 

 
