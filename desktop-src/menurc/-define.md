---
title: " define"
description: Die Anweisung \ define weist den angegebenen Wert dem angegebenen Namen zu. Alle nachfolgenden Vorkommen des Namens werden durch den-Wert ersetzt.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711951"
---
# <a name="define"></a>\#definieren

Die **\# define** -Direktive weist den angegebenen Wert dem angegebenen Namen zu. Alle nachfolgenden Vorkommen des Namens werden durch den-Wert ersetzt.

``` syntax
#define name value
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Benennen*
</dt> <dd>

Name, der definiert werden soll. Dieser Wert ist eine beliebige Kombination aus Buchstaben, Ziffern und Interpunktions Zeichen, die für den C/C++-Präprozessor gültig ist.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Wert*
</dt> <dd>

Eine ganze Zahl, eine Zeichenfolge oder eine Textzeile.

</dd> </dl>

## <a name="example"></a>Beispiel

In diesem Beispiel werden den Namen "Nonzero" und "userclass" Werte zugewiesen:

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven](preprocessor-directives.md)
</dt> </dl>

 

 




