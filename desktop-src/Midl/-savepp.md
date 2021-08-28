---
title: /savePP-Switch
description: Wenn die /savePP-Direktive angegeben wird, löscht der MIDL-Compiler die Ausgabe des C/C++-Präprozessors nicht.
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- /savePP switch MIDL
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c574d1032d9e392973478bc1df1e22cde6a49145b6f4775d928aac0b35e6988b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067480"
---
# <a name="savepp-switch"></a>/savePP-Switch

Wenn die **/savePP-Direktive** angegeben wird, löscht der MIDL-Compiler die Ausgabe des C/C++-Präprozessors nicht.

``` syntax
midl /savePP
```

## <a name="switch-options"></a>Switch-Optionen

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Mit diesem Schalter können Entwickler erkennen, was vom MIDL-Compiler analysiert wird, und ist für das Debuggen nützlich. Die Ausgabe des Präprozessors wird in eine oder mehrere temporäre Dateien in dem Verzeichnis geschrieben, das durch die TEMP-Umgebungsvariable angegeben wird. Der Name der Ausgabedatei bzw. der Dateien folgt der Namenskonvention MID \* .tmp. Beachten Sie, dass eine einzelne Kompilierung mehrere vorverarbeitete Eingabestreams generieren kann. Dies liegt daran, dass der Import einer IDL-Datei im Gegensatz zur Verwendung von **\# include** eine separate Präprozessorversion verursacht.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[/no \_ cpp, /nocpp](-no-cpp-nocpp.md)
</dt> </dl>

 

 




