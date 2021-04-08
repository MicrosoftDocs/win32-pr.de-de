---
title: Typen von Bindungs Handles
description: Bindungs Handles können automatisch, implizit oder explizit sein.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a09b858dfc677d06cf5885dc7a5f7a6ba599eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037324"
---
# <a name="types-of-binding-handles"></a>Typen von Bindungs Handles

Bindungs Handles können automatisch, implizit oder explizit sein. Sie unterscheiden sich in der Steuerungs Menge, die die Anwendung über den Bindungsprozess verfügt. Wie der Name bereits vermuten lässt, verarbeitet die automatische Bindung die automatisierte Bindung. Die Client-und Server Anwendungen benötigen keinen Code, um den Bindungsprozess zu verarbeiten. Mit impliziten Bindungs Handles können Client Programme das Bindungs handle konfigurieren, bevor die Bindung stattfindet. Nachdem der Client eine Bindung eingerichtet hat, verarbeitet die RPC-Lauf Zeit Bibliothek den Rest. Explizite Bindungs Handles verschieben die gesamte Kontrolle über den Bindungsprozess in den Quellcode des Clients und der Serverprogramme. Mit diesem Steuerelement kommt es zu erhöhter Komplexität. Die Anwendung muss RPC-Funktionen zum Verwalten der Bindung abrufen. Dies geschieht nicht automatisch. Es werden explizite Bindungs Handles empfohlen.

Im folgenden Diagramm werden die Unterschiede zwischen automatischen, impliziten und expliziten Bindungs Handles veranschaulicht.

![Unterschiede zwischen automatischen, impliziten und expliziten Bindungs Handles](images/bhand.png)

Außerdem ist jedes Bindungs handle entweder primitiv oder Benutzer definiert. In den folgenden Themen wird jeder Typ von Bindungs handle erläutert:

-   [Automatische Bindungs Handles](automatic-binding-handles.md)
-   [Implizite Bindungs Handles](implicit-binding-handles.md)
-   [Explizite Bindungs Handles](explicit-binding-handles.md)
-   [Primitive und benutzerdefinierte Bindungs Handles](primitive-and-custom-binding-handles.md)

 

 




