---
title: InprocHandler32
description: InprocHandler32 gibt an, ob eine Anwendung einen benutzerdefinierten Handler im HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID verwendet.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- InprocHandler32-Registrierungsschlüssel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73a8b2577a554b0bb8b5ba5a851e630edbf90a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406003"
---
# <a name="inprochandler32"></a>InprocHandler32

Gibt an, ob eine Anwendung einen benutzerdefinierten Handler verwendet.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **REG \_ SZ-Wert,** der den benutzerdefinierten Handler angibt, der von der Anwendung verwendet wird. Wenn kein benutzerdefinierter Handler verwendet wird, sollte der Eintrag auf Ole32.dll.

Wenn ein Container in der Registrierung nach einem benutzerdefinierten Handler sucht, hat die 16-Bit-Version Priorität mit einem 16-Bit-Container, und die 32-Bit-Version hat Priorität mit einem 32-Bit-Container.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**InprocHandler**](inprochandler.md)
</dt> </dl>

 

 




