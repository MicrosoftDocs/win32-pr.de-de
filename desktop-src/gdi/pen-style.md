---
description: Das style-Attribut gibt das Linienmuster an, das angezeigt wird, wenn ein bestimmter geometrischer Stift verwendet wird. Es gibt acht vordefinierte Stiftstile. Die folgende Abbildung zeigt die sieben dieser Stile, die vom System definiert werden.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Stiftstil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42cc82510c58d36cec76039488ecc13c826609a0870b929f18d82282a87ba8cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666510"
---
# <a name="pen-style"></a>Stiftstil

Das style-Attribut gibt das Linienmuster an, das angezeigt wird, wenn ein bestimmter geometrischer Stift verwendet wird. Es gibt acht vordefinierte Stiftstile. Die folgende Abbildung zeigt die sieben dieser Stile, die vom System definiert werden.

![Abbildung mit sieben Zeilen, die jeweils mit einem anderen vordefinierten Stil gezeichnet werden](images/cspen-01.png)

Der Stil innerhalb des Rahmens ist identisch mit dem solid-Stil für optische Stifte. Sie funktioniert jedoch anders, wenn sie mit einem geometrischen Stift verwendet wird. Wenn der geometrische Stift breiter als ein einzelnes Pixel ist und eine Zeichnungsfunktion den Stift verwendet, um einen Rahmen um ein gefülltes Objekt zu zeichnen, zeichnet das System den Rahmen innerhalb des Rahmens des Objekts. Mithilfe des Innerhalbrahmenstils kann eine Anwendung sicherstellen, dass ein Objekt unabhängig von der geometrischen Stiftbreite vollständig innerhalb der angegebenen Abmessungen angezeigt wird.

Zusätzlich zu den sieben vom System definierten Stilen gibt es einen achten Stil, der vom Benutzer (oder der Anwendung) definiert wird. Ein benutzerdefinierter Stil generiert Linien mit einer benutzerdefinierten Reihe von Bindestrichen und Punkten.

Verwenden Sie die Funktion [**CreatePen,**](/windows/desktop/api/Wingdi/nf-wingdi-createpen) [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)oder [**ExtCreatePen,**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) um einen Stift mit den systemdefinierte Formatvorlagen zu erstellen. Verwenden Sie die **ExtCreatePen-Funktion,** um einen Stift mit einem benutzerdefinierten Stil zu erstellen.

 

 



