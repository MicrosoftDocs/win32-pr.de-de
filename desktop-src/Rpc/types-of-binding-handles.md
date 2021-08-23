---
title: Typen von Bindungshandles
description: Bindungshandles können automatisch, implizit oder explizit sein.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a3db77f01bf0228623efe9d3dca5fbeb023d97fbe00e5da4d4ba070f323ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011073"
---
# <a name="types-of-binding-handles"></a>Typen von Bindungshandles

Bindungshandles können automatisch, implizit oder explizit sein. Sie unterscheiden sich in der Kontrolle, die die Anwendung über den Bindungsprozess hat. Wie der Name schon sagt, automatisiert die automatische Bindung die Bindung. Die Client- und Serveranwendungen benötigen keinen Code, um den Bindungsprozess zu verarbeiten. Implizite Bindungshandles ermöglichen Clientprogrammen, das Bindungshandle zu konfigurieren, bevor die Bindung erfolgt. Nachdem der Client eine Bindung eingerichtet hat, verarbeitet die RPC-Laufzeitbibliothek den Rest. Explizite Bindungshandles verschieben die vollständige Kontrolle über den Bindungsprozess in den Quellcode des Clients und der Serverprogramme. Mit diesem Steuerelement erhöht sich die Komplexität. Ihre Anwendung muss RPC-Funktionen aufrufen, um die Bindung zu verwalten. Dies geschieht nicht automatisch. Explizite Bindungshandles werden empfohlen.

Das folgende Diagramm veranschaulicht die Unterschiede zwischen automatischen, impliziten und expliziten Bindungshandles.

![Unterschiede zwischen automatischen, impliziten und expliziten Bindungshandles](images/bhand.png)

Darüber hinaus ist jedes Bindungshandle entweder primitiv oder benutzerdefiniert. Die einzelnen Bindungshandletypen werden in den folgenden Themen erläutert:

-   [Automatische Bindungshandles](automatic-binding-handles.md)
-   [Implizite Bindungshandles](implicit-binding-handles.md)
-   [Explizite Bindungshandles](explicit-binding-handles.md)
-   [Primitive und benutzerdefinierte Bindungshandles](primitive-and-custom-binding-handles.md)

 

 




