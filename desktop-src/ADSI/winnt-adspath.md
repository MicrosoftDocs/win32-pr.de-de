---
title: WinNT ADsPath
description: Dieses Thema enthält Beispiele für Zeichen folgen, die für den WinNT ADsPath verwendet werden.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- WinNT-Dienstanbieter ADSI, WinNT ADsPath
- ADsPath ADSI, WinNT, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea2c3db1b5234fb07045d921858766a105c4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947318"
---
# <a name="winnt-adspath"></a>WinNT ADsPath

Die ADsPath-Zeichenfolge für den ADSI WinNT-Anbieter kann eine der folgenden Formen aufweisen:


```C++
WinNT:
WinNT://<domain name>
WinNT://<domain name>/<server>
WinNT://<domain name>/<path>
WinNT://<domain name>/<object name>
WinNT://<domain name>/<object name>,<object class>
WinNT://<server>
WinNT://<server>/<object name>
WinNT://<server>/<object name>,<object class>
```



Der Domänen Name kann entweder ein NetBIOS-Name oder ein DNS-Name sein.

Der Server ist der Name eines bestimmten Servers innerhalb der Domäne.

Der Pfad ist der Pfad für ein Objekt, z. b. "printserver1/printer2".

Der Objektname ist der Name eines bestimmten Objekts.

Die Objektklasse ist der Klassenname des benannten Objekts. Ein Beispiel für diese Verwendung wäre "Winnt://MyServer/JeffSmith,User". Die Angabe eines Klassen namens kann die Leistung des Bindungs Vorgangs verbessern.

 

 




