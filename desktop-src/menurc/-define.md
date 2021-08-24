---
title: " define"
description: Die \define-Direktive weist den angegebenen Wert dem angegebenen Namen zu. Alle nachfolgenden Vorkommen des Namens werden durch den Wert ersetzt.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8e8f99dc592eefb1fb79201883e8a32837633814b79d7819e84d283709a46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826050"
---
# <a name="define"></a>\#Definieren

Die **\# define-Direktive** weist den angegebenen Wert dem angegebenen Namen zu. Alle nachfolgenden Vorkommen des Namens werden durch den Wert ersetzt.

``` syntax
#define name value
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Namen*
</dt> <dd>

Der name, der definiert werden soll. Dieser Wert ist eine beliebige Kombination aus Buchstaben, Ziffern und Interpunktion, die für den C/C++-Präprozessor gültig ist.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Wert*
</dt> <dd>

Ganze Zahl, Zeichenfolge oder Textzeile.

</dd> </dl>

## <a name="example"></a>Beispiel

In diesem Beispiel werden den Namen NONZERO und USERCLASS Werte zugewiesen:

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven](preprocessor-directives.md)
</dt> </dl>

 

 




