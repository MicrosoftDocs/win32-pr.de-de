---
description: Das Style-Attribut gibt das Linien Muster an, das angezeigt wird, wenn ein bestimmter kosmetischer oder geometrischer Stift verwendet wird. Es gibt acht vordefinierte Stift Stile. Die folgende Abbildung zeigt die sieben dieser Stile, die vom System definiert werden.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Stift Stil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447839627f97d7662fdef35bd7088ef7b0dcba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959304"
---
# <a name="pen-style"></a>Stift Stil

Das Style-Attribut gibt das Linien Muster an, das angezeigt wird, wenn ein bestimmter kosmetischer oder geometrischer Stift verwendet wird. Es gibt acht vordefinierte Stift Stile. Die folgende Abbildung zeigt die sieben dieser Stile, die vom System definiert werden.

![Abbildung, die sieben Zeilen anzeigt, die jeweils mit einem anderen vordefinierten Stil gezeichnet werden](images/cspen-01.png)

Die innere Frame-Formatvorlage ist mit dem Stil für optische Stifte identisch. Sie funktioniert jedoch anders, wenn Sie mit einem geometrischen Stift verwendet wird. Wenn der geometrische Stift breiter als ein einzelnes Pixel ist und eine Zeichnungs Funktion den Stift verwendet, um einen Rahmen um ein ausgefülltes Objekt zu zeichnen, zeichnet das System den Rahmen im Frame des Objekts. Mithilfe der inneren Frame-Stil kann eine Anwendung sicherstellen, dass ein Objekt vollständig innerhalb der angegebenen Dimensionen angezeigt wird, unabhängig von der geometrischen Stift Breite.

Zusätzlich zu den sieben vom System definierten Stilen gibt es einen achten Stil, bei dem es sich um einen definierten Benutzer (oder eine Anwendung) handelt. Ein benutzerdefinierter Stil generiert Zeilen mit einer angepassten Reihe von Bindestrichen und Punkten.

Verwenden Sie die Funktion " [**kreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen)", " [**kreatepenindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)" oder " [**extkreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) ", um einen Stift zu erstellen, der über die System definierten Stile verfügt. Verwenden Sie die **extkreatepen** -Funktion, um einen Stift mit einem benutzerdefinierten Stil zu erstellen.

 

 



