---
title: InprocHandler
description: Gibt an, ob eine Anwendung einen benutzerdefinierten Handler verwendet.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- InprocHandler-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8c19089ece43496465351b44e9faa8793ba893
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388565"
---
# <a name="inprochandler"></a>InprocHandler

Gibt an, ob eine Anwendung einen benutzerdefinierten Handler verwendet.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert, der den benutzerdefinierten Handler angibt, der von der Anwendung verwendet wird. Wenn kein benutzerdefinierter Handler verwendet wird, sollte der Eintrag auf Ole32.dll festgelegt werden.

Wenn ein Container die Registrierung nach einem benutzerdefinierten Handler durchsucht, hat die 16-Bit-Version eine Priorität mit einem 16-Bit-Container, und die 32-Bit-Version hat eine Priorität mit einem 32-Bit-Container.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**InprocHandler32**](inprochandler32.md)
</dt> </dl>

 

 




