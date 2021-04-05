---
title: Die Header Datei
description: Die Header Datei enthält Definitionen aller Datentypen und Vorgänge, die in der IDL-Datei deklariert sind, sowie alle Datentypen und Vorgänge, die in den in der \ include-Direktive enthaltenen Dateien deklariert werden.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- Mittel l-und RPC-Mittell, Schnittstellen, Header Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61331d8bb72d322987c13d02b04632c95424e755
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037297"
---
# <a name="the-header-file"></a>Die Header Datei

Die Header Datei enthält Definitionen aller Datentypen und Vorgänge, die in der IDL-Datei deklariert sind, sowie alle Datentypen und Vorgänge, die in den in der include-Direktive enthaltenen Dateien deklariert werden \# . Datentypen aus den Dateien, die mit der Import-Anweisung importiert werden, werden nicht in die Header Datei repliziert. Stattdessen enthält die generierte Header Datei eine include-Zeile zur H-Datei, die aus der importierten Datei generiert wurde. Die Header Datei muss von allen Anwendungsmodulen eingeschlossen werden, die die definierten Vorgänge aufzurufen, die definierten Vorgänge implementieren oder die definierten Typen bearbeiten.

Die Mittel-Compilerschalter [**/Header**](-header.md) und [**/out**](-out.md) wirken sich auf die Header Datei aus.

 

 




