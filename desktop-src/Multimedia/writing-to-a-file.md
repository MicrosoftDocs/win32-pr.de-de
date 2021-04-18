---
title: Schreiben in eine Datei
description: Schreiben in eine Datei
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- Avifileschreitedata-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9a6b9a399d8581909c99da615e32ef4487cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340634"
---
# <a name="writing-to-a-file"></a>Schreiben in eine Datei

Sie können zusätzliche Informationen in eine Datei schreiben, die mit Schreibberechtigungen geöffnet wurde, indem Sie die [**avifilewrite tedata**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) -Funktion verwenden. Diese Funktion kopiert die Informationen aus einem von der Anwendung bereitgestellten Puffer und platziert Sie in einem oder mehreren Blöcken in der Datei. Der "Info"-Block ist ein gängiger Riff-Block-Typ, in dem die Funktion ergänzende Informationen speichert. Eine Beschreibung der Riff-Dateien und der zugehörigen Datenblöcke finden Sie unter [Dienst Format Dienste für den Ressourcenaustausch](resource-interchange-file-format-services.md).

 

 




