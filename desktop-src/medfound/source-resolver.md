---
description: Quellresolver
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Quellresolver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a844893b0348546d4fd174b0b24405812efcef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344379"
---
# <a name="source-resolver"></a>Quellresolver

Der Source Resolver nimmt einen URL oder Bytedatenstrom und erstellt die entsprechende Medienquelle für den Inhalt. Der Source Resolver ist das Standardverfahren, nach dem Anwendungen Medienquellen erstellen.

Intern verwendet der quellresolver *Handlerobjekte* :

-   *Schema Handler* nehmen eine URL an und erstellen eine Medienquelle oder einen Bytestream.
-   *Byte Datenstrom Handler* nehmen einen Bytestream an und erstellen eine Medienquelle.

Sie können einen benutzerdefinierten Handler implementieren und ihn der Registrierung hinzufügen. Schema Handler werden über das URL-Schema registriert, und Byte Datenstrom Handler werden durch die Dateinamenerweiterung oder den MIME-Typ registriert.

Dieses Thema enthält folgende Abschnitte:

-   [Verwenden des quellresolvers](using-the-source-resolver.md)
-   [Konfigurieren einer Medienquelle](configuring-a-media-source.md)
-   [Schema Handler und Byte-Stream Handler](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienquellen](media-sources.md)
</dt> </dl>

 

 



