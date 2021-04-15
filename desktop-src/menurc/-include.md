---
title: " include"
description: Die \ include-Direktive bewirkt, dass der Ressourcen Compiler die im filename-Parameter angegebene Datei verarbeitet.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8d36f1d0ae24f3dc21d67eec57056872aabdbd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391466"
---
# <a name="-include"></a>darunter

Die **\# include** -Direktive bewirkt, dass der Ressourcen Compiler die im *filename* -Parameter angegebene Datei verarbeitet. Bei dieser Datei sollte es sich um eine Header Datei handeln, die die in der Ressourcen Definitionsdatei verwendeten Konstanten definiert. Die Datei kann Einzel Byte-, Doppelbyte-oder Unicode-Zeichen verwenden.

``` syntax
#include filename
```

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Einfügen*
</dt> <dd>

Der Name der einzuschließenden Datei. Wenn sich die Datei im aktuellen Verzeichnis befindet, muss die Zeichenfolge in doppelte Anführungszeichen eingeschlossen werden. Wenn sich die Datei in dem Verzeichnis befindet, das durch die include-Umgebungsvariable angegeben ist, muss die Zeichenfolge in eine kleiner-als-oder größer-als-Zeichen (<>) eingeschlossen werden. Sie müssen einen vollständigen Pfad in doppelte Anführungszeichen (") einschließen, wenn sich die Datei nicht im aktuellen Verzeichnis oder in dem Verzeichnis befindet, das in der INCLUDE-Umgebungsvariablen angegeben ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die folgende Anweisung in der Header Datei, um-Anweisungen zu umschließen, die von einem C-Compiler, aber nicht von RC kompiliert werden können:

``` syntax
#ifndef RC_INVOKED
```

Auf diese Weise können Sie die gleichen Include-Dateien in den c-und RC-Dateien verwenden.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die Header Dateien "Windows. h" und "mydefs. h" beim Kompilieren der Ressourcen Definitionsdatei verarbeitet:

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven](preprocessor-directives.md)
</dt> </dl>

 

 




