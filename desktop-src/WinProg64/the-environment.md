---
title: Die Umgebung
description: Entwickler, die an Anwendungen für 64-Bit-Windows arbeiten, finden die Entwicklungsumgebung praktisch identisch mit der Entwicklungsumgebung für 32-Bit-Windows.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- Entwicklungsumgebung 64-Bit-Windows-Programmierung
- Umgebung 64-Bit-Windows-Programmierung
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Entwicklungsumgebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ea1bdacbb478eaa0abcf46d04c3d772540f26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036631"
---
# <a name="the-environment"></a>Die Umgebung

Entwickler, die an Anwendungen für 64-Bit-Windows arbeiten, finden die Entwicklungsumgebung praktisch identisch mit der Entwicklungsumgebung für 32-Bit-Windows. Die vorhandenen APIs wurden bei Bedarf geändert, damit Sie die Genauigkeit der Plattform widerspiegeln können, auf der Sie ausgeführt werden. Das Ergebnis ist Einfachheit und eine kurze Lernkurve für den Entwickler – das Schreiben von Code für 64-Bit-Windows ist genauso wie das Schreiben von Code für 32-Bit-Windows.

Die Windows-Header Dateien unterstützen neue Datentypen, mit denen Zeiger und Zeiger zugeordnete Variablen die Genauigkeit der Plattform widerspiegeln können. Dies bedeutet, dass Entwickler eine einzelne quellbasis kompilieren können, um nativ 32 auf Windows-oder 64-Bit-Windows-Fenstern auszuführen. Diese Strategie reduziert die Kosten für die Entwicklung von Anwendungen, die 64-Bit-Hardware nutzen, wie z. b. AMD Opteron oder Athlon64-Prozessoren oder Intel Itanium-Prozessoren.

Wenn Sie die neuen Datentyp Konventionen so schnell wie möglich übernehmen, müssen Sie mehr Zeit für die Bereitstellung Ihrer 64 Anwendungen bereitstellen. Wenn Sie den Code ändern, sollten Sie die Daten Definitionen gleichzeitig ändern. Testen Sie die Anwendung auf 32-Bit-Fenstern, führen Sie Sie über den 64-Bit-Compiler aus (beschrieben in [den Tools](the-tools.md)), und die Anwendung kann getestet werden, wenn Sie über die entsprechende 64-Bit-Hardware verfügen.

 

 




