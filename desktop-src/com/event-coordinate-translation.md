---
title: Ereignis Koordinaten Übersetzung
description: Ereignis Koordinaten Übersetzung
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c40a742ead8fc8d7e431c1caa5210f0978168cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713218"
---
# <a name="event-coordinate-translation"></a>Ereignis Koordinaten Übersetzung

Die 96-Spezifikation für-Steuerelemente erfordert, dass die Koordinaten, die für Ereignisse, die von der-Steuer Elements ausgelöst werden, von HIMETRIC in als Punkt basiert Diese Änderung führt dazu, dass das Ereignis das Übergeben von Koordinaten in der Zeile mit den Eigenschaften und Methoden durchführt, sodass die Koordinaten Übersetzung nicht mehr für den Container zuständig ist. Dies löst bestimmte Kompatibilitätsprobleme aus, bei denen ein Steuerelement Ereignisse mithilfe einer Koordinaten Basis auslöst, die nicht erwartet wird. Dies sollte nur ein Problem sein, bei dem ein 96-Steuerelement Container ein älteres Pre-96-Steuerelement wie folgt gehostet:

-   Wenn ein älterer Pre-96-Container ein 96-Steuerelement hostet, stellt das Steuerelement die Ereignis Koordinaten als Punkte dar, sodass der Container keine Probleme verursacht, da der Container den Parametertyp erkennen sollte.
-   Wenn ein 96-Container ein Pre-96-Steuerelement hostet, stellt das Steuerelement den Container mit Koordinaten dar und erwartet, dass der Container eine beliebige Übersetzung benötigt. Allerdings erwartet der 96-Container, dass ein Steuerelement der 96-Steuerelement Spezifikation entspricht und seine Koordinaten als Punkte darstellen. Das-Steuerelement verwendet die [**transformcoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) -Methode auf der [**iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) -Schnittstelle, die vom Container bereitgestellt wird, auf die gleiche Weise wie für Eigenschaften und Methoden, um dies zu erreichen.

Daher muss der Benutzer eines 96-Containers, der vor 96-Steuerelementen gehostet wird, beachten, dass eine weitere Übersetzung der Koordinaten erforderlich ist, wenn Ereignisse ausgelöst werden.

 

 




