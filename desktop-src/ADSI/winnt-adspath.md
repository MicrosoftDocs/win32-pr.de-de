---
title: WinNT ADsPath
description: Dieses Thema enthält Beispiele für Zeichenfolgen, die für WinNT ADsPath verwendet werden.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- WinNT-Dienstanbieter ADSI , WinNT ADsPath
- ADsPath ADSI , WinNT, description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4971209a516d9e0c759e892322c99db1807a4bf88e771281299af30abc47d47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838370"
---
# <a name="winnt-adspath"></a>WinNT ADsPath

Die ADsPath-Zeichenfolge für den ADSI WinNT-Anbieter kann eine der folgenden Formen haben:


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



Der Domänenname kann entweder ein NETBIOS-Name oder ein DNS-Name sein.

Der Server ist der Name eines bestimmten Servers innerhalb der Domäne.

Der Pfad ist der Pfad von für das Objekt, z. B. "printserver1/printer2".

Der Objektname ist der Name eines bestimmten Objekts.

Die Objektklasse ist der Klassenname des benannten Objekts. Ein Beispiel für diese Verwendung wäre "WinNT://MyServer/JeffSmith,user". Das Angeben eines Klassennamens kann die Leistung des Bindungsvorgang verbessern.

 

 




