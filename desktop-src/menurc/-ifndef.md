---
title: " ifndef"
description: Die \ ifndef-Direktive steuert die bedingte Kompilierung der Ressourcen Datei, indem der angegebene Name überprüft wird.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 984a969123ea68fd68b14c1b98354b8bc5205aba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341237"
---
# <a name="ifndef"></a>\#ifndef

Die **\# ifndef** -Direktive steuert die bedingte Kompilierung der Ressourcen Datei, indem der angegebene Name überprüft wird. Wenn der Name nicht definiert wurde oder seine Definition mithilfe der **\# undef** -Direktive entfernt wurde, weist **\# ifndef** den Compiler an, die Verarbeitung von Anweisungen bis zur nächsten **\# EndIf**-, **\# else**-oder **\# elif** -Direktive fortzusetzen und die Anweisung nach der **\# EndIf** -Direktive zu überspringen. Wenn der Name definiert ist, leitet **\# ifndef** den Compiler an, die nächste **\# EndIf**-, **\# else**-oder **\# elif** -Direktive zu überspringen.

``` syntax
#ifndef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Benennen*
</dt> <dd>

Der Name, der von der Direktive geprüft werden soll.

</dd> </dl>

## <a name="example"></a>Beispiel

In diesem Beispiel wird die [**Bitmap**](bitmap-resource.md) -Anweisung nur kompiliert, wenn die Optimierung nicht definiert ist:

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven](preprocessor-directives.md)
</dt> </dl>

 

 




