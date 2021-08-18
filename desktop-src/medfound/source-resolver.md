---
description: Quelllöser
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Quelllöser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d90ac92cc9d30c5dfb46be60812fbe3156e0f26e396ed1bb9006752ae9db47bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034738"
---
# <a name="source-resolver"></a>Quelllöser

Der Source Resolver nimmt einen URL oder Bytedatenstrom und erstellt die entsprechende Medienquelle für den Inhalt. Der Source Resolver ist das Standardverfahren, nach dem Anwendungen Medienquellen erstellen.

Intern verwendet der Quellre resolver *Handlerobjekte:*

-   *Schemahandler* verwenden eine URL und erstellen eine Medienquelle oder einen Bytestream.
-   *Bytestreamhandler* nehmen einen Bytestream an und erstellen eine Medienquelle.

Sie können einen benutzerdefinierten Handler implementieren und ihn der Registrierung hinzufügen. Schemahandler werden nach URL-Schema registriert, und Bytestreamhandler werden nach Dateinamenerweiterung oder MIME-Typ registriert.

Dieses Thema enthält folgende Abschnitte:

-   [Verwenden des Quelllösers](using-the-source-resolver.md)
-   [Konfigurieren einer Medienquelle](configuring-a-media-source.md)
-   [Schemahandler und Byte-Stream Handler](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienquellen](media-sources.md)
</dt> </dl>

 

 



