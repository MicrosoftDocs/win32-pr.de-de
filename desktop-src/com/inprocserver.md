---
title: InprocServer
description: Gibt den Pfad zur Prozess internen Server-DLL an.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- InprocServer-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5682693d711f734bbc60def8a711f11e2bad0ef9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947703"
---
# <a name="inprocserver"></a>InprocServer

Gibt den Pfad zur Prozess internen Server-DLL an.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a>Bemerkungen

Der **InprocServer** -Eintrag ist für einfügbar-Klassen relativ selten.

Prozess interne Server werden zurzeit mit dem Registrierungs Eintrag **InprocServer** registriert. Die 32-Bit-und 64-Bit-in-Process-Server sollten den [**InProcServer32**](inprocserver32.md) -Eintrag verwenden. Wenn ein Container die Registrierung nach einem in-Process-Server durchsucht, hat die 16-Bit-Version eine Priorität mit einem 16-Bit-Container, und die 32-Bit-Version hat eine Priorität mit einem 32-Bit-Container.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**InprocServer32**](inprocserver32.md)
</dt> </dl>

 

 




