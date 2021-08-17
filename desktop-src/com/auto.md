---
title: Automatisch
description: Bestimmt, ob der Debugger automatisch gestartet wird, wenn eine COM RPC-Benachrichtigung gesendet wird.
ms.assetid: e05ae7cb-79d1-4543-aef3-9397548c2030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 030cab43fe0ac4a67551920479b9c36f3d1ff33f2ba2854647fcf209cfe694e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737222"
---
# <a name="auto"></a>Automatisch

Bestimmt, ob der Debugger automatisch gestartet wird, wenn eine COM RPC-Benachrichtigung gesendet wird.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\DebugObjectRPCEnabled\AeDebug
   Auto = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ WORD-Wert.**



| Wert | Beschreibung                    |
|-------|--------------------------------|
| 1     | Debugger automatisch starten. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> </dl>

 

 




