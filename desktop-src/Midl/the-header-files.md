---
title: Headerdateien
description: Die Schnittstellenheaderdatei (Name.h) enthält Typdefinitionen und Funktionsdeklarationen basierend auf der Schnittstellendefinition in der aktuellen IDL-Datei sowie alle Datentypen und Vorgänge, die in den dateien deklariert sind, die in der \include-Direktive enthalten sind.
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- Headerdateien MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac9bc5e8b5edd091450af670fd51d251326029f13e1f88a6d5a9116faa5b4447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013518"
---
# <a name="the-header-files"></a>Headerdateien

Die Schnittstellenheaderdatei (Name.h) enthält Typdefinitionen und Funktionsdeklarationen basierend auf der Schnittstellendefinition in der aktuellen IDL-Datei sowie alle Datentypen und Vorgänge, die in den in der include-Direktive enthaltenen Dateien deklariert \# sind. Datentypen aus den Dateien, die mit der import-Direktive importiert wurden, werden nicht in die Headerdatei repliziert. Stattdessen enthält die generierte Headerdatei eine Includezeile zur H-Datei, die aus der importierten Datei generiert wurde.

Schließen Sie diese Datei in die Quelldateien für die Proxy-DLL und für Clientanwendungen ein, die die -Schnittstelle verwenden.

Der Standardname für eine Headerdatei, die aus file.idl generiert wird, ist File.h. Der [**MIDL-Compilerschalter /header**](-header.md) überschreibt den Standardnamen der Schnittstellenheaderdatei.

 

 




