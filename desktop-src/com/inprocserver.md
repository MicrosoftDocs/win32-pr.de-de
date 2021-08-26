---
title: InprocServer
description: Gibt den Pfad zur Prozessserver-DLL an.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- InprocServer-Registrierungsschlüssel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b6cd1c7ab32733687292f01ddb48167c68243c62345fb17af3b6533a5cb454d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029890"
---
# <a name="inprocserver"></a>InprocServer

Gibt den Pfad zur Prozessserver-DLL an.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a>Hinweise

Der **InprocServer-Eintrag** ist bei einfügebaren Klassen relativ selten.

In-Process-Server werden derzeit mithilfe des **Registrierungseintrags InprocServer** registriert. Die 32-Bit- und 64-Bit-In-Process-Server sollten den [**Eintrag InprocServer32**](inprocserver32.md) verwenden. Wenn ein Container in der Registrierung nach einem Prozessserver sucht, hat die 16-Bit-Version Priorität mit einem 16-Bit-Container, und die 32-Bit-Version hat Priorität mit einem 32-Bit-Container.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Inprocserver32**](inprocserver32.md)
</dt> </dl>

 

 




