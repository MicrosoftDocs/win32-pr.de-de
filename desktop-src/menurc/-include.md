---
title: " include"
description: Die \include-Anweisung bewirkt, dass der Ressourcencompiler die im Filename-Parameter angegebene Datei verarbeitet.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bf5d6fa40e45073ca7ccb5f97dd3ddb0d13dfdfced965d5c83332183da421e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599719"
---
# <a name="-include"></a>'include'

Die **\# include-Anweisung** bewirkt, dass der Ressourcencompiler die im *Filename-Parameter* angegebene Datei verarbeitet. Diese Datei sollte eine Headerdatei sein, die die in der Ressourcendefinitionsdatei verwendeten Konstanten definiert. Die Datei kann Einzel-Byte-, Doppel-Byte- oder Unicode-Zeichen verwenden.

``` syntax
#include filename
```

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Dateiname*
</dt> <dd>

Name der datei, die eingeschlossen werden soll. Wenn sich die Datei im aktuellen Verzeichnis befindet, muss die Zeichenfolge in doppelte Anführungszeichen eingeschlossen werden. Wenn sich die Datei in dem von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnis befindet, muss die Zeichenfolge in Kleiner-als- und Größer-als-Zeichen (<>) eingeschlossen werden. Sie müssen einen vollständigen Pfad angeben, der in doppelte Anführungszeichen (") eingeschlossen ist, wenn sich die Datei nicht im aktuellen Verzeichnis oder in dem von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnis befindet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie die folgende Anweisung in der Headerdatei, um -Anweisungen zu umleiten, die von einem C-Compiler, aber nicht von RC kompiliert werden können:

``` syntax
#ifndef RC_INVOKED
```

Auf diese Weise können Sie die gleichen Includedateien in Ihren C- und RC-Dateien verwenden.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die Headerdateien Windows.h und MyDefs.h beim Kompilieren der Ressourcendefinitionsdatei verarbeitet:

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven](preprocessor-directives.md)
</dt> </dl>

 

 




