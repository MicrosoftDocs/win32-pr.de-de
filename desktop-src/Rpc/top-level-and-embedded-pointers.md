---
title: Top-Level und eingebettete Zeiger
description: Um zu verstehen, wie Zeiger und die zugehörigen Datenelemente in Microsoft RPC zugeordnet werden, müssen Sie zwischen Zeigern der obersten Ebene und eingebetteten Zeigern unterscheiden.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84fcecdb70c67d7c99b4bbd3753c244a87cd07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471676"
---
# <a name="top-level-and-embedded-pointers"></a>Top-Level und eingebettete Zeiger

Um zu verstehen, wie Zeiger und die zugehörigen Datenelemente in Microsoft RPC zugeordnet werden, müssen Sie zwischen *Zeigern der obersten Ebene* und *eingebetteten Zeigern* unterscheiden. Es ist auch hilfreich, auf den Satz aller Zeiger zu verweisen, die keine Zeiger auf oberster Ebene sind.

*Zeiger der obersten Ebene* sind solche, die als Parameternamen in Funktionsprototypen angegeben werden. Zeiger der obersten Ebene und ihre Verweise werden immer auf dem Server zugewiesen.

*Eingebettete Zeiger* sind Zeiger, die in Datenstrukturen wie Arrays, Strukturen und Unions eingebettet sind. Wenn eingebettete Zeiger nur Ausgaben in einen Puffer schreiben und bei Eingaben NULL sind, kann die Serveranwendung ihre Werte in einen nicht-NULL-Wert ändern. In diesem Fall weisen die clientstubdaten neuen Arbeitsspeicher für diese Daten zu.

Wenn der eingebettete Zeiger auf dem Client vor dem-Befehl nicht NULL ist, wird der Client bei der Rückgabe keinen Arbeitsspeicher zuordnen. Stattdessen versuchen die stubvorgänge, den dem eingebetteten Zeiger zugeordneten Arbeitsspeicher auf dem Client zu schreiben, der diesem Zeiger zugeordnet ist, wobei die bereits vorhandenen Daten überschrieben werden.

> [!Note]  
> Für Daten, die aus einem Puffer gelesen oder geschrieben werden und der die Puffergröße nicht angibt, muss die Ausgabe Länge kleiner oder gleich der Eingabe Länge sein. Eine RPC-Ausnahme wird ausgelöst, wenn ein Überlauf erkannt wird. Für Zeichen folgen Daten wird die Ausgabe Länge durch die Überprüfung der Länge der Eingabe Zeichenfolge bestimmt. Daher dürfen Ausgabe Zeichenfolgen die Länge von Eingabe Zeichenfolgen nicht überschreiten Die Best Practices-Anleitung besteht darin, dies zu vermeiden, indem Sie immer einen Größen spezifischen Parameter einschließen, um die Größe des Puffers anzugeben.

 

Eingebettete schreibgeschützte Zeiger werden unter [Kombinieren von Zeiger-und direktionalen Attributen](combining-pointer-and-directional-attributes.md)erläutert.

Der Begriff *nontop-Level-Zeiger* bezieht sich auf alle Zeiger, die nicht als Parameternamen im Funktionsprototyp angegeben werden, einschließlich eingebetteter Zeiger und mehrerer Ebenen von gruppierten Zeigern.

 

 




