---
title: " undef"
description: Die \undef-Direktive entfernt die aktuelle Definition des angegebenen Namens. Alle nachfolgenden Vorkommen des Namens werden ohne Ersetzung verarbeitet.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3adf208ecca3f130aefc99de8d2926028f25bcd46be46d42e4cbf92e708fa0b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473060"
---
# <a name="undef"></a>\#undef

Die **\# Undef-Direktive** entfernt die aktuelle Definition des angegebenen Namens. Alle nachfolgenden Vorkommen des Namens werden ohne Ersetzung verarbeitet.

``` syntax
#undef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Namen*
</dt> <dd>

Name, der entfernt werden soll. Dieser Wert ist eine beliebige Kombination aus Buchstaben, Ziffern und Interpunktion, die für den C/C++-Präprozessor gültig ist.

</dd> </dl>

## <a name="example"></a>Beispiel

In diesem Beispiel werden die Definitionen für die Namen ungleich null und USERCLASS entfernt:

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven](preprocessor-directives.md)
</dt> </dl>

 

 




