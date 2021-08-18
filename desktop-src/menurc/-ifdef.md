---
title: " Ifdef"
description: Die \ifdef-Direktive steuert die bedingte Kompilierung der Ressourcendatei durch Überprüfen des angegebenen Namens.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e834dc84d54e1d6f7725008b8bcf28f4ed49fc3fe45f36fb291ddc397d30eb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034478"
---
# <a name="ifdef"></a>\#Ifdef

Die **\# ifdef-Direktive** steuert die bedingte Kompilierung der Ressourcendatei durch Überprüfen des angegebenen Namens. Wenn der Name mithilfe einer **\# define-Direktive** oder der Befehlszeilenoption **/d** mit dem Ressourcencompiler definiert wurde, weist **\# ifdef** den Compiler an, direkt nach der **\# ifdef-Direktive** mit der Anweisung fortzufahren. Wenn der Name nicht definiert wurde, weist **\# ifdef** den Compiler an, alle Anweisungen bis zur nächsten **\# endif-Direktive** zu überspringen.

``` syntax
#ifdef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Namen*
</dt> <dd>

Name, der von der -Anweisung überprüft werden soll.

</dd> </dl>

## <a name="example"></a>Beispiel

In diesem Beispiel wird die [**BITMAP-Anweisung**](bitmap-resource.md) nur kompiliert, wenn Debug definiert ist:

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven](preprocessor-directives.md)
</dt> </dl>

 

 




