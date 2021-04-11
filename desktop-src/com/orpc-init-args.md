---
title: ORPC_INIT_ARGS Struktur
description: Die ORPC \_ Init \_ args-Struktur enthält Informationen, die zum Initialisieren des Remote Debuggens mithilfe der iorpcdebugnotify-Schnittstelle verwendet werden.
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- COM für ORPC_INIT_ARGS Struktur
- LPORPC_INIT_ARGS Struktur Zeiger com
topic_type:
- apiref
api_name:
- ORPC_INIT_ARGS
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7dca0209f745d5034bde2da852829b99d7dcb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103255"
---
# <a name="orpc_init_args-structure"></a>ORPC \_ Init \_ args-Struktur

Die **ORPC \_ Init \_ args** -Struktur enthält Informationen, die zum Initialisieren des Remote Debuggens mithilfe der [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct ORPC_INIT_ARGS {
  IOrpcDebugNotify *lpIntfOrpcDebug;
  void             *pvPSN;
  DWORD            *dwReserved1;
  DWORD            *dwReserved2;
} ORPC_INIT_ARGS, *LPORPC_INIT_ARGS;
```



## <a name="members"></a>Member

<dl> <dt>

**lpintforpcdebug**
</dt> <dd>

Ein Zeiger auf die [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle, die von in-Process-Debuggern verwendet werden soll. Wenn der Debugger nicht in-Process oder ein Macintosh-System ist, muss dieses Feld **null** sein.

</dd> <dt>

**pvpsn**
</dt> <dd>

Ein Zeiger auf die Macintosh-Prozess Seriennummer des zu debuggenden Prozesses. Wenn die zu debuggende Komponente kein Macintosh-System ist, muss dieses Feld **null** sein.

</dd> <dt>

**dwReserved1**
</dt> <dd>

Reserviert. Muss den Wert 0 (null) haben.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Reserviert. Muss den Wert 0 (null) haben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>N/V</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ORPC \_ dbg \_ alle**](orpc-dbg-all.md)
</dt> <dt>

[**ORPC \_ dbg- \_ Puffer**](orpc-dbg-buffer.md)
</dt> <dt>

[**Dlldebugobjectrpchook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**Iorpcdebug-Benachrichtigung**](iorpcdebugnotify.md)
</dt> </dl>

 

 





