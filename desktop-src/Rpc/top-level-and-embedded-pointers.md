---
title: Top-Level und eingebettete Zeiger
description: Um zu verstehen, wie Zeiger und die zugehörigen Datenelemente in Microsoft RPC zugeordnet werden, müssen Sie zwischen Zeigern der obersten Ebene und eingebetteten Zeigern unterscheiden.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28fab18cfb345587f4c152f6890d94c5177e5bd9344e542592c33e462915beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011268"
---
# <a name="top-level-and-embedded-pointers"></a>Top-Level und eingebettete Zeiger

Um zu verstehen, wie Zeiger und die zugehörigen Datenelemente  in Microsoft RPC zugeordnet werden, müssen Sie zwischen Zeigern der obersten Ebene und eingebetteten *Zeigern unterscheiden.* Es ist auch hilfreich, auf den Satz aller Zeiger zu verweisen, die keine Zeiger der obersten Ebene sind.

*Zeiger der obersten Ebene sind zeiger,* die als Namen von Parametern in Funktionsprototypen angegeben werden. Zeiger der obersten Ebene und ihre Referenz werden immer auf dem Server zugeordnet.

*Eingebettete Zeiger sind* Zeiger, die in Datenstrukturen wie Arrays, Strukturen und Unions eingebettet sind. Wenn eingebettete Zeiger nur die Ausgabe in einen Puffer schreiben und bei der Eingabe NULL sind, kann die Serveranwendung ihre Werte in nicht NULL ändern. In diesem Fall weisen die Clientstubs neuen Arbeitsspeicher für diese Daten zu.

Wenn der eingebettete Zeiger vor dem Aufruf auf dem Client nicht NULL ist, weisen die Stubs dem Client bei der Rückgabe keinen Arbeitsspeicher zu. Stattdessen versuchen die Stubs, den Speicher, der dem eingebetteten Zeiger zugeordnet ist, in den vorhandenen Arbeitsspeicher auf dem Client zu schreiben, der diesem Zeiger zugeordnet ist, und überschreiben die bereits vorhandenen Daten.

> [!Note]  
> Für Daten, die aus einem Puffer gelesen oder in einen Puffer geschrieben werden und die die Puffergröße nicht angeben, muss die Ausgabelänge kleiner oder gleich der Eingabelänge sein. Eine RPC-Ausnahme wird ausgelöst, wenn ein Überlauf erkannt wird. Bei Zeichenfolgendaten wird die Ausgabelänge durch Überprüfen der Länge der Eingabezeichenfolge bestimmt. Daher dürfen Ausgabezeichenfolgen die Länge von Eingabezeichenfolgen nicht überschreiten. Die bewährte Methode besteht in der Vermeidung, indem immer ein von der Größe angegebener Parameter zur Angabe der Puffergröße verwendet wird.

 

Eingebettete Zeiger mit Schreibzugriff werden unter [Kombinieren von Zeigern und direktionalen Attributen erläutert.](combining-pointer-and-directional-attributes.md)

Der Begriff Zeiger auf *Nicht-Topebene* bezieht sich auf alle Zeiger, die nicht als Parameternamen im Funktionsprototyp angegeben sind, einschließlich eingebetteter Zeiger und mehrerer Ebenen geschachtelter Zeiger.

 

 




