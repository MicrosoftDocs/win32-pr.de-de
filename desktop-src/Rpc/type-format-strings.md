---
title: Typformatzeichenfolgen
description: Formatierungszeichen bezeichnen Objekte, die für die NDR-Engine von Interesse sind.
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618d857e487f86e2d28ed18300d82e94b76e3a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037326"
---
# <a name="type-format-strings"></a>Typformatzeichenfolgen

Formatierungszeichen bezeichnen Objekte, die für die NDR-Engine von Interesse sind. Es gibt ein Formatzeichen für jeden Basistyp, für verschiedene komplexe Typen und für Beschreibungen von Zeigern, packen, Ausrichtungen und anderen verschiedenen Objekten. Für Verbund Typen werden verschiedene Kategorien von Strukturen und Arrays basierend auf Ihren Leistungseigenschaften erkannt. Eine Format Zeichenfolge für jede Kategorie beginnt mit einem FC-Token, das die jeweilige Format Zeichenfolge identifiziert. Format Zeichen für Strukturen und Array Kategorien können die in-Fixes in den Namen des führenden FC-Tokens freigeben, das in der folgenden Tabelle gezeigt wird.



| Zeichen formatieren | BESCHREIBUNG                                    |
|------------------|------------------------------------------------|
| C                | Gibt Konformitäts Informationen im Typ an. |
| V                | Gibt Varianz Informationen im Typ an.    |
| P                | Gibt an, dass Zeiger ein Teil des Typs sind.     |



 

Beispielsweise identifizieren FC \_ cstruct und FC \_ CArray die konforme Struktur bzw. die konformen Array Deskriptoren.

Im folgenden sind Formatzeichen mit besonderer Bedeutung aufgeführt.



| Zeichen formatieren | BESCHREIBUNG                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| FC- \_ PP           | Gibt den Anfang des Zeiger Beschreibungs Abschnitts einer Struktur oder eines Arrays an. |



 

Die Format Zeichenfolgen für den RPC-NDR-Typ werden in den folgenden Themen ausführlicher beschrieben:

-   [Einfache Typen](simple-types-tfs.md)
-   [Zeiger](pointers-tfs.md)
-   [Arrays](arrays-tfs.md)
-   [Zeichenfolgen](strings-tfs.md)
-   [Korrelations Deskriptoren](correlation-descriptors-tfs.md)
-   [Strukturen](structures-tfs.md)
-   [Zeiger Layout](pointer-layout-tfs.md)
-   [Unions](unions-tfs.md)
-   [Übertragen \_ als und Darstellung \_ als](transmit-as-and-represent-as-tfs.md)
-   [Benutzer Mars Hallen](user-marshal-tfs.md)

 

 




