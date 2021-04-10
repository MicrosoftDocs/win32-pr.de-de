---
description: In TSPI werden nicht transparente Handles verwendet, um auf die Datenstrukturen zu verweisen, die Linien, Telefone und Aufrufe darstellen.
ms.assetid: aa1742aa-6cd4-461a-ad92-972eefcf637f
title: Nicht transparente Handles und private Datenstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd8c7b911de5f85f84b56a8e25e28eb805c5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959103"
---
# <a name="opaque-handles-and-private-data-structures"></a>Nicht transparente Handles und private Datenstrukturen

In TSPI werden nicht transparente Handles verwendet, um auf die Datenstrukturen zu verweisen, die Linien, Telefone und Aufrufe darstellen. Diese werden als Parameter für die meisten Funktionen und Rückrufe angezeigt. Es gibt nur wenige Funktionen, die auf das Gerät mit einem Geräte Bezeichner anstelle eines opaken Handles verweisen. In einem solchen Fall bezieht sich der Verweis auf das Gerät selbst und nicht auf eine Datenstruktur. Funktionen, die auf diese Weise funktionieren, sind in der Regel jene, die zu frühen Initialisierungs Zeiten aufgerufen werden, bevor Datenstrukturen erstellt und nicht transparente Handles ausgetauscht werden.

Der Dienstanbieter muss entscheiden, wie diese Handles interpretiert werden sollen. Ein Dienstanbieter verwendet in der Regel den Zeiger auf seine Datenstruktur oder den Index in ein Array von Datenstrukturen als undurchsichtiges handle. Die einzige Einschränkung besteht darin, dass der Dienstanbieter den Wert 0 nicht als [hdrvline](hdrvline.md), hdrvcalloder [hdrvphone](hdrvphone.md)verwenden kann. Der Wert 0 oder **null** für ein Handle hat in einigen Vorgängen eine besondere Bedeutung.

 

 



