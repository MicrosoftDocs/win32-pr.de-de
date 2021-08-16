---
title: " ifndef"
description: Die \ifndef-Direktive steuert die bedingte Kompilierung der Ressourcendatei durch Überprüfen des angegebenen Namens.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23728acabc0ca0179c544a66657a2d1b8343d5eae24556018e0e65025420bfba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472986"
---
# <a name="ifndef"></a>\#ifndef

Die **\# ifndef-Direktive** steuert die bedingte Kompilierung der Ressourcendatei durch Überprüfen des angegebenen Namens. Wenn der Name nicht definiert wurde oder seine Definition mithilfe der **\# Undef-Direktive** entfernt wurde, weist **\# ifndef** den Compiler an, die Verarbeitung von Anweisungen bis zur nächsten **\# endif-,** **\# else-** oder **\# elif-Direktive** fortzusetzen und dann nach der **\# endif-Direktive** zur Anweisung zu springen. Wenn der Name definiert ist, weist **\# ifndef** den Compiler an, zur nächsten **\# endif-,** **\# else-** oder **\# elif-Direktive** zu springen.

``` syntax
#ifndef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Namen*
</dt> <dd>

Name, der von der -Anweisung überprüft werden soll.

</dd> </dl>

## <a name="example"></a>Beispiel

In diesem Beispiel wird die [**BITMAP-Anweisung**](bitmap-resource.md) nur kompiliert, wenn Optimize nicht definiert ist:

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven](preprocessor-directives.md)
</dt> </dl>

 

 




