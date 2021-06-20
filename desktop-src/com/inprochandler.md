---
title: InprocHandler
description: InprocHandler gibt an, ob eine Anwendung einen benutzerdefinierten Handler im HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID verwendet.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- InprocHandler-Registrierungsschlüssel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aea1ca0d5eb5dec58a36578d268d7020a963a95e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404733"
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

Dies ist ein **REG \_ SZ-Wert,** der den benutzerdefinierten Handler angibt, der von der Anwendung verwendet wird. Wenn kein benutzerdefinierter Handler verwendet wird, sollte der Eintrag auf Ole32.dll.

Wenn ein Container in der Registrierung nach einem benutzerdefinierten Handler sucht, hat die 16-Bit-Version Priorität mit einem 16-Bit-Container, und die 32-Bit-Version hat Priorität mit einem 32-Bit-Container.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**InprocHandler32**](inprochandler32.md)
</dt> </dl>

 

 




