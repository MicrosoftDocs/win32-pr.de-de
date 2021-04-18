---
title: Die Header Dateien
description: Die Schnittstellen Header Datei (Name. h) enthält Typdefinitionen und Funktions Deklarationen auf der Grundlage der Schnittstellen Definition in der aktuellen IDL-Datei sowie alle Datentypen und Vorgänge, die in den in der \ include-Direktive enthaltenen Dateien deklariert werden.
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- Header Dateien (Mitte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ae80877b88d8061769b0d6bd56c13469427fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341257"
---
# <a name="the-header-files"></a>Die Header Dateien

Die Schnittstellen Header Datei (Name. h) enthält Typdefinitionen und Funktions Deklarationen, die auf der Schnittstellen Definition in der aktuellen IDL-Datei basieren, sowie alle Datentypen und Vorgänge, die in den in der include-Direktive enthaltenen Dateien deklariert werden \# . Datentypen aus den Dateien, die mit der Import-Anweisung importiert werden, werden nicht in die Header Datei repliziert. Stattdessen enthält die generierte Header Datei eine include-Zeile zu der aus der importierten Datei generierten H-Datei.

Fügen Sie diese Datei in die Quelldateien für die Proxy-dll und für Client Anwendungen ein, die die-Schnittstelle verwenden.

Der Standardname für eine Header Datei, die aus einer Datei erstellt wird. idl ist File. h. Der [**/Header**](-header.md) -Compilerschalter überschreibt den Standardnamen der Schnittstellen Header Datei.

 

 




