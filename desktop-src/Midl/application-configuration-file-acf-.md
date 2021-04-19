---
title: Anwendungs Konfigurationsdatei (ACF)
description: Es gibt möglicherweise Aspekte ihrer verteilten Anwendung, die sich auf eine Komponente auswirken, aber nichts mit einem anderen tun müssen.
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- ACF-Mittell
- Microsoft Interface Definition Language mittlere, beschriebene Anwendungs Konfigurationsdatei
- Anwendungs Konfigurationsdatei-Mittel l
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9066e5641d6b71e68ba670984765661f1b9f6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341876"
---
# <a name="application-configuration-file-acf"></a>Anwendungs Konfigurationsdatei (ACF)

Es gibt möglicherweise Aspekte ihrer verteilten Anwendung, die sich auf eine Komponente auswirken, aber nichts mit einem anderen tun müssen. Ein-Objekt kann z. b. eine große, komplexe Datenstruktur enthalten und den Inhalt dieser Datenstruktur an ein anderes-Objekt übergeben. Das genaue Layout dieser Datenstruktur ist für die empfangende Anwendung möglicherweise bedeutungslos. Die Struktur kann auch Datentypen enthalten, die vom-compilercompiler nicht erkannt werden, und es kann kein Marshalling und kein Marshalling von Code generiert werden.

Client Anwendungen können die gleiche Schnittstelle verwenden, aber auf unterschiedlichen Plattformen ausgeführt werden. Sie benötigen möglicherweise jeweils einen eigenen Satz von Marshallingroutinen. Schließlich benötigen einzelne Clients möglicherweise nicht immer denselben Funktions Satz. Es ist ineffizient, Stub-Code für Funktionen zu generieren, die nie in einer bestimmten Client Anwendung implementiert werden.

Wenn Sie diese lokalen Aspekte Ihrer Schnittstelle in einer Anwendungs Konfigurationsdatei (ACF) definieren, können Sie die Unterschiede zwischen den Client Schnittstellen von ihrer Netzwerkdarstellung trennen, sodass der Serverdaten in einem konsistenten Format senden und empfangen und den Stub-Code kompakter und effizienter gestalten kann.

Die Struktur und die Syntax einer ACF-Schnittstellen Definition sind identisch mit der IDL-Definition:

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

Standardmäßig muss der Name der ACF-Schnittstelle mit dem Namen in der IDL-Definition identisch sein. Wenn Sie jedoch mit der kompil-Compileroption/ [**ACF**](-acf.md) einen ACF-Dateinamen explizit angeben, müssen die Schnittstellennamen nicht identisch sein. Diese Funktion ermöglicht es, dass mehrere Schnittstellen eine einzelne ACF-Spezifikation gemeinsam verwenden.

 

 




