---
title: Lesen von Farbwerten aus dem Framebuffer
description: Beachten Sie bei der Verwendung von Funktionen, mit denen Farbwerte aus dem Framebuffer gelesen werden, die Unterschiede zwischen dem Lesen von RGBA-Werten und Farb Indexwerten auf echten Farb Geräten und auf palettenbasierten Geräten.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL unter Windows, Lesen von Farbwerten aus framebuffers
- Lesen von Farbwerten aus Framebuffers OpenGL
- Framebuffers, Lesen von Farbwerten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4df14690b68f7e93949d26ee50ac562ebd667be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709359"
---
# <a name="reading-color-values-from-the-framebuffer"></a>Lesen von Farbwerten aus dem Framebuffer

Beachten Sie bei der Verwendung von Funktionen, mit denen Farbwerte aus dem Framebuffer gelesen werden, die Unterschiede zwischen dem Lesen von RGBA-Werten und Farb Indexwerten auf echten Farb Geräten und auf palettenbasierten Geräten.

Auf einem echten Farbgerät:

-   RGBA-Werte sind auf den Kanal im Gerät beschränkt.
-   Farb Indexwerte werden im Framebuffer als RGBA-Werte gespeichert. Wenn Sie diese Werte verwenden, müssen Sie eine umgekehrte Übersetzung von RGBA zum logischen Palettenindex durchführen. Wenn zwei logische Indizes die gleichen RGBA-Werte aufweisen, kann der falsche Index zurückgegeben werden.

Auf einem palettenbasierten Gerät:

-   RGBA-Werte werden aus einem Index in der Systempalette gelesen. Der logische Index wird aus einer umgekehrten Tabelle abgerufen, und die RGBA-Komponenten werden extrahiert.
-   Farb Indexwerte werden von einem Index in die Systempalette gelesen, und eine umgekehrte Tabelle wird verwendet, um den Index für die logische Palette zu erhalten.

 

 




