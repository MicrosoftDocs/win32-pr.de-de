---
title: ORPC_DBG_BUFFER-Struktur
description: Die ORPC DBG BUFFER-Struktur ist das Pufferformat, das zum Marshallen von RPC-Daten zu den Methoden der \_ \_ IOrpcDebugNotify-Schnittstelle verwendet wird.
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- ORPC_DBG_BUFFER-Struktur COM
- PORPC_DBG_BUFFER Strukturzeiger COM
topic_type:
- apiref
api_name:
- ORPC_DBG_BUFFER
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb1f83cfcbe673cd2d5701e57ae1e94d4e04b59b845cd9ec7b617077da24bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310256"
---
# <a name="orpc_dbg_buffer-structure"></a>ORPC \_ DBG \_ BUFFER-Struktur

Die **ORPC \_ DBG \_ BUFFER-Struktur** ist das Pufferformat, das zum Marshallen von RPC-Daten zu den Methoden der [**IOrpcDebugNotify-Schnittstelle verwendet**](iorpcdebugnotify.md) wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _ORPC_DBG_BUFFER {
  DWORD alwaysOrSometimes;
  BYTE  verMajor;
  BYTE  verMinor;
  DWORD cbRemaining;
  GUID  guidSemantic;
  union {
    BOOL   fStopOnOtherSide;
    USHORT wDebuggingOpCode;
    USHORT cExtent;
    BYTE   padding[2];
    struct {
      ULONG cb;
      GUID  guidExtent;
      BYTE  *rgbData;
    };
  };
} ORPC_DBG_BUFFER, *PORPC_DBG_BUFFER;
```



## <a name="members"></a>Member

<dl> <dt>

**alwaysOrSometimes**
</dt> <dd>

Ein -Wert, der das Debugger-Spawning steuert. **alwaysOrSometimes** kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <dt>**ORPC \_ DEBUGGEN \_ VON ALWAYS**</dt> <dt>0X00000000</dt> </dl>                              | Wenn festgelegt, gibt COM immer die Client- oder Serverbenachrichtigung auf dem Empfänger aus.<br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <dt>**ORPC \_ \_DEBUGGEN, WENN \_ HOOK \_ AKTIVIERT**</dt> <dt>0X00000001</dt> </dl> | Wenn festgelegt, gibt COM nur dann die Client- oder Serverbenachrichtigung auf dem Empfänger aus, wenn das COM-Debuggen aktiviert wurde, indem [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) in diesem Prozess mit **fTrace** auf TRUE festgelegt **wird.** <br/> |



 

</dd> <dt>

**verMajor**
</dt> <dd>

Die Hauptversionsnummer der Datenformatspezifikation.

</dd> <dt>

**verMinor**
</dt> <dd>

Die Nebenversionsnummer der Datenformatspezifikation.

</dd> <dt>

**cbRemaining**
</dt> <dd>

Die Anzahl der Bytes, einschließlich **cbRemaining**, die in dieser Struktur folgen.

</dd> <dt>

**guidSemantic**
</dt> <dd>

Eine GUID, die bestimmt, welche Member der Union unten vorhanden sind. **guidSemantic** kann einen der folgenden Werte verwenden:



| Wert                                                                                                           | Bedeutung                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt> </dl> | Bestimmt, ob einzelne Einzelschritte vom Debugger ausgeführt werden sollen. Unten ist **nur das fStopOnOtherSide-Member** der Union vorhanden.<br/>                                             |
| <dl> <dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt> </dl> | Bestimmt, ob RPC-marshallte Daten und Debugopcodes an den Empfänger übergeben werden. Alle Member der Union sind unten mit Ausnahme von **fStopOnOtherSide vorhanden.**<br/> |



 

</dd> <dt>

**fStopOnOtherSide**
</dt> <dd>

True **gibt an,** dass ein einzelner Schritt vom Debugger ausgeführt wird, und er sollte den Server schrittweise beenden und die Ausführung fortsetzen, sobald die andere Seite erreicht ist. Andernfalls wird kein einzelner Einzelschritt ausgeführt, und die Debuggerausführung wird auf der anderen Seite beendet.

</dd> <dt>

**wDebuggingOpCode**
</dt> <dd>

Ein -Wert, der die Angabe einer Reihe von Vorgängen ermöglicht. **wDebuggingOpCode** kann einen der folgenden Werte verwenden:



| Wert                                                                             | Bedeutung                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x0000</dt> </dl> | Keine Operation.<br/>                                                                             |
| <dl> <dt>0x0001</dt> </dl> | Wenn festgelegt, ist die Einzelschrittsemantik mit **fStopOnOtherSide** identisch, wenn sie auf **TRUE festgelegt ist.**<br/> |



 

</dd> <dt>

**cExtent**
</dt> <dd>

Polsterung. Darf nicht verwendet werden.

</dd> <dt>

**padding**
</dt> <dd>

Polsterung. Darf nicht verwendet werden.

</dd> <dt>

**Cb**
</dt> <dd>

Die Größe der Daten in **rgbData** in Bytes.

</dd> <dt>

**guidExtent**
</dt> <dd>

Eine **GUID,** die den Datentyp in **rgbData bestimmt.** **guidExtent** kann einen der folgenden Werte verwenden:



| Wert                                                                                                           | Bedeutung                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>53199051-57EB-11ce-A964-00AA006C3706</dt> </dl> | **rgbData** ist ein marshallter Schnittstellenzeiger.<br/> |



 

</dd> <dt>

**rgbData**
</dt> <dd>

Ein **BYTE-Puffer,** der verwendet wird, um PER RPC marshallte COM-Daten zwischen client- und serverdebuggern zu übergeben. Der Inhalt von **rgbData** wird durch die **GUID** in **guidExtent bestimmt.**



| guidExtent-Wert                     | rgbData-Inhalte                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 53199051-57EB-11ce-A964-00AA006C3706 | Ein marshallter Schnittstellenzeiger, der sich aus dem Aufruf von [**CoMarshalInterface ergibt.**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) Der marshalled-Zeiger wird mithilfe von [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)in den entsprechenden Schnittstellenzeiger konvertiert. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Member dieser Struktur haben eine 1-Byte-Ausrichtung und werden immer in Little-Endian-Byte-Reihenfolge übertragen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>N/V</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





