---
title: ORPC_DBG_BUFFER Struktur
description: Die ORPC \_ dbg- \_ Puffer Struktur ist das Puffer Format, das zum Mars Hallen von RPC-Daten an die Methoden der iorpcdebugnotify-Schnittstelle verwendet wird.
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- COM für ORPC_DBG_BUFFER Struktur
- PORPC_DBG_BUFFER Struktur Zeiger com
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
ms.openlocfilehash: 4dc42251b928207a2b009a18c1d88e94dcf1492a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341786"
---
# <a name="orpc_dbg_buffer-structure"></a>ORPC \_ dbg- \_ Puffer Struktur

Die **ORPC \_ dbg- \_ Puffer** Struktur ist das Puffer Format, das zum Mars Hallen von RPC-Daten an die Methoden der [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle verwendet wird.

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

**alwaysorbisweilen**
</dt> <dd>

Ein Wert, der das Erzeugen des Debuggers steuert. **alwaysorsometimes** kann einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <dt>**ORPC \_ \_Immer**</dt> <dt>0x00000000</dt> Debuggen </dl>                              | Wenn diese Einstellung festgelegt ist, wird die Client-oder Server Benachrichtigung für den Empfänger immer von com erhoben.<br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <dt>**ORPC \_ Debuggen, \_ Wenn der \_ Hook \_ aktiviert ist**</dt> <dt>0x00000001</dt> </dl> | Wenn festgelegt, wird von com nur die Client-oder Server Benachrichtigung für den Empfänger ausgegeben, wenn das com-Debuggen aktiviert wurde, indem [**dlldebugobjectrpchook**](dlldebugobjectrpchook.md) in diesem Prozess aufgerufen wird, wobei **ftrace** auf **true** festgelegt ist. <br/> |



 

</dd> <dt>

**verMajor**
</dt> <dd>

Die Hauptversionsnummer der Datenformat Spezifikation.

</dd> <dt>

**verMinor**
</dt> <dd>

Die neben Versionsnummer der Datenformat Spezifikation.

</dd> <dt>

**cbremaineing**
</dt> <dd>

Die Anzahl von Bytes (einschließlich **cbremaineing**), die in dieser-Struktur befolgt werden.

</dd> <dt>

**guidsemantic**
</dt> <dd>

Eine GUID, die bestimmt, welche Member der Union unten vorhanden sind. **guidsemantic** kann einen der folgenden Werte annehmen:



| Wert                                                                                                           | Bedeutung                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>9cade560-8F 43-101A-b07b-00dd01113f 11</dt> </dl> | Bestimmt, ob ein Einzelschritt vom Debugger ausgeführt werden soll. Im folgenden ist nur das **fstoponotherside** -Member der Union vorhanden.<br/>                                             |
| <dl> <dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt> </dl> | Bestimmt, ob die an den Empfänger gemarshallte RPC-Daten und debugopcodes übermittelt werden. Alle Member der Union sind unten mit Ausnahme von **fstoponotherside** enthalten.<br/> |



 

</dd> <dt>

**"f"**
</dt> <dd>

**True** gibt an, dass der Debugger einen Einzelschritt durchläuft und den Server ausführen und die Ausführung fortsetzen soll, sobald die andere Seite erreicht ist. Andernfalls wird ein Einzelschritt nicht durchgeführt, und die Debugger-Ausführung wird auf der anderen Seite angehalten.

</dd> <dt>

**wdebuggingopcode**
</dt> <dd>

Ein Wert, mit dem eine Reihe von Vorgängen angegeben werden kann. **wdebuggingopcode** kann einen der folgenden Werte annehmen:



| Wert                                                                             | Bedeutung                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x0000</dt> </dl> | Keine Operation.<br/>                                                                             |
| <dl> <dt>0x0001</dt> </dl> | Wenn der Wert festgelegt ist, ist die Semantik mit einem Schritt mit **fstoponotherside** identisch, wenn auf **true** festgelegt.<br/> |



 

</dd> <dt>

**cblock**
</dt> <dd>

Auffüllung. Darf nicht verwendet werden.

</dd> <dt>

**padding**
</dt> <dd>

Auffüllung. Darf nicht verwendet werden.

</dd> <dt>

**betrieben**
</dt> <dd>

Die Größe in Bytes der Daten in **rgbData**.

</dd> <dt>

**guidextent**
</dt> <dd>

Eine **GUID** , die den Typ der Daten in **rgbData** bestimmt. " **guidextent** " kann einen der folgenden Werte annehmen:



| Wert                                                                                                           | Bedeutung                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>53199051-57eb-11CE-a964-00aa006c3706</dt> </dl> | **rgbData** ist ein marshallte Schnittstellen Zeiger.<br/> |



 

</dd> <dt>

**rgbData**
</dt> <dd>

Ein **Byte** Puffer, der verwendet wird, um RPC-Daten zwischen den Client-und serverbuggern zu übergeben. Der Inhalt von **rgbData** wird durch die **GUID** in " **guidextent**" bestimmt.



| Wert für "guidextent"                     | rgbData-Inhalt                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 53199051-57eb-11CE-a964-00aa006c3706 | Ein gemarshallte Schnittstellen Zeiger, der sich aus dem Aufruf von [**comarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)ergibt. Der Marshalling-Zeiger wird mithilfe von " [**count**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)" in den entsprechenden Schnittstellen Zeiger konvertiert. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Member dieser Struktur haben eine 1-Byte-Ausrichtung und werden immer in Little-Endian-Byte Reihenfolge übertragen.

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

[**ORPC-init-Argumente \_ \_**](orpc-init-args.md)
</dt> <dt>

[**Dlldebugobjectrpchook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**Iorpcdebug-Benachrichtigung**](iorpcdebugnotify.md)
</dt> </dl>

 

 





