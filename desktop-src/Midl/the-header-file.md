---
title: Die Headerdatei
description: Die Headerdatei enthält Definitionen aller Datentypen und Vorgänge, die in der IDL-Datei deklariert sind, sowie alle Datentypen und Vorgänge, die in den Dateien deklariert sind, die in der \include-Direktive enthalten sind.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL und RPC MIDL, Schnittstellen, Headerdatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd107bbf741f3259ac474d03a3ec1eba5c4ab8217df3ff6afa5ef45e7b4945a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582130"
---
# <a name="the-header-file"></a>Die Headerdatei

Die Headerdatei enthält Definitionen aller Datentypen und Vorgänge, die in der IDL-Datei deklariert sind, sowie alle Datentypen und Vorgänge, die in den Dateien deklariert sind, die in der \# include-Direktive enthalten sind. Datentypen aus den mit der Importdirektive importierten Dateien werden nicht in die Headerdatei repliziert. Stattdessen enthält die generierte Headerdatei eine Includezeile zur H-Datei, die aus der importierten Datei generiert wurde. Die Headerdatei muss von allen Anwendungsmodulen eingeschlossen werden, die die definierten Vorgänge aufrufen, die definierten Vorgänge implementieren oder die definierten Typen bearbeiten.

Die MIDL-Compilerschalter [**/header**](-header.md) und [**/out**](-out.md) wirken sich auf die Headerdatei aus.

 

 




