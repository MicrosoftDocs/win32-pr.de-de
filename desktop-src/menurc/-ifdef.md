---
title: " ifdef"
description: Die \ ifdef-Direktive steuert die bedingte Kompilierung der Ressourcen Datei, indem der angegebene Name überprüft wird.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38170fb2140f8405a86529c0899c1e4d4e93c026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388343"
---
# <a name="ifdef"></a>\#ifdef

Die **\# ifdef** -Direktive steuert die bedingte Kompilierung der Ressourcen Datei, indem der angegebene Name überprüft wird. Wenn der Name mithilfe einer **\# define** -Direktive oder mithilfe der Befehlszeilenoption **/d** mit dem Ressourcen Compiler definiert wurde, weist **\# ifdef** den Compiler an, mit der Anweisung unmittelbar nach der **\# ifdef** -Direktive fortzufahren. Wenn der Name nicht definiert wurde, weist **\# ifdef** den Compiler an, alle Anweisungen bis zur nächsten **\# EndIf** -Direktive zu überspringen.

``` syntax
#ifdef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Benennen*
</dt> <dd>

Der Name, der von der Direktive geprüft werden soll.

</dd> </dl>

## <a name="example"></a>Beispiel

In diesem Beispiel wird die [**Bitmap**](bitmap-resource.md) -Anweisung nur kompiliert, wenn DEBUG definiert ist:

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven](preprocessor-directives.md)
</dt> </dl>

 

 




