---
title: Die Umgebung
description: Entwickler, die an Anwendungen für 64-Bit-Windows arbeiten, finden die Entwicklungsumgebung praktisch identisch mit der Entwicklungsumgebung für 32-Bit-Windows.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- 64-Bit-Windows-Programmierung in der Entwicklungsumgebung
- Umgebungs-64-Bit-Windows-Programmierung
- 64-Bit-Windows-Programmierhandbuch 64-Bit-Windows Programmierung, Entwicklungsumgebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69580d6537c832abaf51b20a553c4e4e788a6013bdfc14a8002f60de9872da62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734130"
---
# <a name="the-environment"></a>Die Umgebung

Entwickler, die an Anwendungen für 64-Bit-Windows arbeiten, finden die Entwicklungsumgebung praktisch identisch mit der Entwicklungsumgebung für 32-Bit-Windows. Die vorhandenen APIs wurden bei Bedarf geändert, damit sie die Genauigkeit der Plattform widerspiegeln können, auf der sie ausgeführt werden. Das Ergebnis ist Einfachheit und eine kurze Lernkurve für den Entwickler. Das Schreiben von Code für 64-Bit-Windows entspricht dem Schreiben von Code für 32-Bit-Windows.

Die Windows Headerdateien unterstützen neue Datentypen, die es Zeigern und Zeigern zugeordneten Variablen ermöglichen, die Genauigkeit der Plattform widerzuspiegeln. Dies bedeutet, dass Entwickler eine einzelne Quellbasis kompilieren können, um nativ auf 32-Bit-Windows oder 64-Bit-Windows ausgeführt zu werden. Diese Strategie reduziert die Kosten für die Entwicklung von Anwendungen, die 64-Bit-Hardware nutzen, z. B. AMD Opteron- oder Entladeprozessoren oder Intel Itanium-Prozessoren.

Wenn Sie die neuen Datentypkonventionen so bald wie möglich übernehmen, haben Sie mehr Zeit, Ihre Anwendungen 64-Bit bereit zu machen. Wenn Sie Ihren Code ändern, sollten Sie die Datendefinitionen gleichzeitig ändern. Testen Sie die Anwendung auf 32-Bit-Windows, führen Sie sie über den 64-Bit-Compiler aus (beschrieben in [Den Tools),](the-tools.md)und die Anwendung kann getestet werden, wenn Sie über die entsprechende 64-Bit-Hardware verfügen.

 

 




