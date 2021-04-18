---
title: " undef"
description: Mit der Anweisung \ undef wird die aktuelle Definition des angegebenen Namens entfernt. Alle nachfolgenden Vorkommen des Namens werden ohne Ersetzung verarbeitet.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338388"
---
# <a name="undef"></a>\#undef

Mit der **\# undef** -Direktive wird die aktuelle Definition des angegebenen Namens entfernt. Alle nachfolgenden Vorkommen des Namens werden ohne Ersetzung verarbeitet.

``` syntax
#undef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Benennen*
</dt> <dd>

Der Name, der entfernt werden soll. Dieser Wert ist eine beliebige Kombination aus Buchstaben, Ziffern und Interpunktions Zeichen, die für den C/C++-Präprozessor gültig ist.

</dd> </dl>

## <a name="example"></a>Beispiel

In diesem Beispiel werden die Definitionen für die Namen "ungleich NULL" und "userclass" entfernt:

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven](preprocessor-directives.md)
</dt> </dl>

 

 




