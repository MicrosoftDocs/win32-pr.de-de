---
description: Eine sprach Kennung ist eine standardmäßige internationale numerische Abkürzung für die Sprache in einem Land oder einer geografischen Region.
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: Sprachen-IDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e3e8f88a64d49d04402c0e72a3946bcddc41e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349031"
---
# <a name="language-identifiers"></a>Sprachen-IDs

Eine sprach Kennung ist eine standardmäßige internationale numerische Abkürzung für die [Sprache](locales-and-languages.md) in einem Land oder einer geografischen Region. Jede Sprache verfügt über einen eindeutigen sprach Bezeichner (Datentyp-langid), einen 16-Bit-Wert, der aus einer primär Sprachen-ID und einer unter Sprachen-ID besteht. Ausführliche Informationen zu sprach Bezeichnern finden Sie unter [sprach Bezeichner-Konstanten und-](language-identifier-constants-and-strings.md)Zeichen folgen.

Eine Sprach-ID wird mit dem [**-Makro makelangid**](/windows/desktop/api/Winnt/nf-winnt-makelangid) erstellt. In der folgenden Abbildung wird das Format der Bits in einem sprach Bezeichner dargestellt.

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

Im folgenden sind vordefinierte sprach Bezeichner aufgeführt:

-   LANG \_ System \_ Standard. Die Standardsprache des Betriebssystems.
-   LANG \_ Benutzer \_ Standard. Sprache des aktuellen Benutzers.

Die Anwendung kann die aktuellen sprach Bezeichner mithilfe der [mehrsprachigen Benutzeroberflächen](multilingual-user-interface.md) Funktionen abrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gebiets Schemas und Sprachen](locales-and-languages.md)
</dt> <dt>

[Sprach Bezeichner-Konstanten und Zeichen folgen](language-identifier-constants-and-strings.md)
</dt> <dt>

[Multilingual User Interface](multilingual-user-interface.md)
</dt> <dt>

[**Makelangid**](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



