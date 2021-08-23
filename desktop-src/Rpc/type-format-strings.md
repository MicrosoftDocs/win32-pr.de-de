---
title: Typformatzeichenfolgen
description: Formatzeichen kennzeichnen Objekte, die für die NDR-Engine von Interesse sind.
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f4aa17494cbef0f3bcc232f89104e3502f94de4a3285a1da6cc0229af0fe26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011118"
---
# <a name="type-format-strings"></a>Typformatzeichenfolgen

Formatzeichen kennzeichnen Objekte, die für die NDR-Engine von Interesse sind. Es gibt ein Formatzeichen für jeden grundlegenden Typ, für verschiedene komplexe Typen und für Beschreibungen von Zeigern, Packen, Ausrichten und anderen verschiedenen Objekten. Bei zusammengesetzten Typen werden mehrere Kategorien von Strukturen und Arrays basierend auf ihren Leistungseigenschaften erkannt. Eine Formatzeichenfolge für jede Kategorie beginnt mit einem FC-Token, das die jeweilige Formatzeichenfolge identifiziert. Formatzeichen für Strukturen und Arraykategorien können die Infixes im Namen des führenden FC-Tokens teilen, das in der folgenden Tabelle gezeigt wird.



| Formatieren eines Zeichens | BESCHREIBUNG                                    |
|------------------|------------------------------------------------|
| C                | Gibt Konformitätsinformationen im Typ an. |
| V                | Gibt Varianzinformationen im Typ an.    |
| P                | Gibt an, dass Zeiger Teil des Typs sind.     |



 

FC \_ CSTRUCT und FC CARRAY identifizieren beispielsweise \_ die konforme Struktur bzw. die konformen Arraydeskriptoren.

Im Folgenden sind Formatzeichen mit besonderen Bedeutungen dargestellt.



| Formatieren eines Zeichens | BESCHREIBUNG                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| FC \_ PP           | Gibt den Anfang des Zeigerbeschreibungsabschnitts einer Struktur oder eines Arrays an. |



 

Formatzeichenfolgen des RPC-NDR-Typs werden in den folgenden Themen ausführlicher beschrieben:

-   [Einfache Typen](simple-types-tfs.md)
-   [Zeiger](pointers-tfs.md)
-   [Arrays](arrays-tfs.md)
-   [Zeichenfolgen](strings-tfs.md)
-   [Korrelationsdeskriptoren](correlation-descriptors-tfs.md)
-   [Strukturen](structures-tfs.md)
-   [Zeigerlayout](pointer-layout-tfs.md)
-   [Unions](unions-tfs.md)
-   [Übertragen \_ als und Darstellen \_ als](transmit-as-and-represent-as-tfs.md)
-   [Benutzer-Marshalling](user-marshal-tfs.md)

 

 




