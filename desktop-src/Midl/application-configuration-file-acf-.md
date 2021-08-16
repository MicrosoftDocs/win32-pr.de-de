---
title: Anwendungskonfigurationsdatei (Application Configuration File, ACF)
description: Es kann Aspekte Ihrer verteilten Anwendung geben, die sich auf eine Komponente auswirken, aber nichts mit einer anderen zu tun haben.
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- ACF MIDL
- Microsoft Interface Definition Language MIDL , beschrieben, Anwendungskonfigurationsdatei
- Anwendungskonfigurationsdatei MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56158267a11125a825442b4db98224d292fdfc309f79cb1562818dee9c08aa23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808342"
---
# <a name="application-configuration-file-acf"></a>Anwendungskonfigurationsdatei (Application Configuration File, ACF)

Es kann Aspekte Ihrer verteilten Anwendung geben, die sich auf eine Komponente auswirken, aber nichts mit einer anderen zu tun haben. Beispielsweise kann ein Objekt eine große, komplexe Datenstruktur enthalten und den Inhalt dieser Datenstruktur an ein anderes Objekt übergeben. Das genaue Layout dieser Datenstruktur kann für die empfangende Anwendung bedeutungslos sein. Darüber hinaus kann die -Struktur Datentypen enthalten, die der MIDL-Compiler nicht erkennt und keinen Marshalling- und Unmarshalingcode generieren kann.

Clientanwendungen verwenden möglicherweise dieselbe Schnittstelle, werden aber auf verschiedenen Plattformen ausgeführt. sie benötigen möglicherweise jeweils einen eigenen Satz von Marshallingroutinen. Schließlich benötigen einzelne Clients möglicherweise nicht immer den gleichen Satz von Funktionen. Es ist ineffizient, Stubcode für Funktionen zu generieren, die nie in einer bestimmten Clientanwendung implementiert werden.

Indem Sie diese lokalen Aspekte Ihrer Schnittstelle in einer Anwendungskonfigurationsdatei (Application Configuration File, ACF) definieren, können Sie die Unterschiede zwischen den Clientschnittstellen von ihrer Netzwerkdarstellung trennen, sodass der Server Daten in einem konsistenten Format senden und empfangen kann, und Ihren Stubcode kompakter und effizienter gestalten.

Struktur und Syntax einer ACF-Schnittstellendefinition sind identisch mit der IDL-Definition:

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

Standardmäßig muss der Name der ACF-Schnittstelle mit dem Namen in der IDL-Definition übereinstimmen. Wenn Sie jedoch die MIDL-Compileroption [**/acf**](-acf.md) verwenden, um explizit einen ACF-Dateinamen anzugeben, müssen die Schnittstellennamen nicht übereinstimmen. Dieses Feature ermöglicht es mehreren Schnittstellen, eine einzelne ACF-Spezifikation gemeinsam zu nutzen.

 

 




