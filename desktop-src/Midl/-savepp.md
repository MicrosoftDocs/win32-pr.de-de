---
title: /savePP-Schalter
description: Wenn die/savePP-Direktive angegeben wird, löscht der mittlerer l-Compiler nicht die Ausgabe des C/C++-Präprozessors.
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- /savePP-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d3ab7032768cacfab6415548a09def453ab4f9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038007"
---
# <a name="savepp-switch"></a>/savePP-Schalter

Wenn die **/savePP** -Direktive angegeben wird, löscht der mittlerer l-Compiler nicht die Ausgabe des C/C++-Präprozessors.

``` syntax
midl /savePP
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Mithilfe dieses Schalters können Entwickler erkennen, was vom Mittelwert Compiler analysiert wird, und sind für das Debuggen nützlich. Die Ausgabe des Präprozessors wird in eine oder mehrere temporäre Dateien in dem Verzeichnis geschrieben, das von der TEMP-Umgebungsvariablen angegeben wird. Der Name der Ausgabedatei (oder Dateien) folgt einer Benennungs Konvention von Mid \* . tmp. Beachten Sie, dass bei einer einzelnen Kompilierung mehrere vorverarbeitete Eingabedaten Ströme generiert werden können. Dies liegt daran, dass das Importieren einer IDL-Datei im Gegensatz zur Verwendung von **\# include** eine separate präprozessorlaufzeit bewirkt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/cpp- \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ Opt**](-cpp-opt.md)
</dt> <dt>

[/No \_ cpp,/nocpp](-no-cpp-nocpp.md)
</dt> </dl>

 

 




