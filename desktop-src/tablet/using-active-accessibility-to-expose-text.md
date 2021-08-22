---
description: Übersicht über die Verwendung der aktiven Barrierefreiheit zum Verfügbar machen von Text.
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: Verwenden von Active Accessibility zum Verfügbar machen von Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 247d78149b82d15eb7c2dbd4ac2b2463d53c5d454dcb7877906197661de36ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334790"
---
# <a name="using-active-accessibility-to-expose-text"></a>Verwenden von Active Accessibility zum Verfügbar machen von Text

Anwendungen können Microsoft Active Accessibility verwenden, um Text verfügbar zu machen. Die [**IAccessible-Schnittstelle,**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) die von früheren Versionen von Active Accessibility definiert wurde, ist jedoch nicht für das Verfügbarmachen großer Mengen von Rich Text optimiert. Höhere Versionen definieren Schnittstellen, die für das Verfügbarmachen großer Mengen von Text- und Textattributen optimiert sind.

Um große Mengen an Text verfügbar zu machen, erstellen Sie separate Component Object Model (COM)-Objekte, die [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible)oder untergeordnete Elemente unterstützen, um jede Ausführung von Text darzustellen. Eine Ausführung ist eine Zeile oder ein Teil einer Zeile, die die gleiche Formatierung hat.

Active Accessibility macht nur den Text und seine Position verfügbar, verfügt aber nicht über einen Mechanismus zum Verfügbarmachen der Formatierung des Texts. Trotz dieser Einschränkungen verwenden einige Programme Active Accessibility, um Text verfügbar zu machen. Microsoft Internet Explorer und Microsoft Visual Studio verwenden beispielsweise Active Accessibility, um große Mengen an Text verfügbar zu machen.

Weitere Informationen zum Verfügbarmachen von Text mit Active Accessibility finden Sie unter [Barrierefreiheit.](../accessibility/accessibility.md)

 

 
