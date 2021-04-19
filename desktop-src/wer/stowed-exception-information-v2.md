---
title: STOWED_EXCEPTION_INFORMATION_V2 Struktur
description: Enthält Informationen zu gestaut-Ausnahme.
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- STOWED_EXCEPTION_INFORMATION_V2 Struktur Windows-Fehlerberichterstattung
- PSTOWED_EXCEPTION_INFORMATION_V2 Struktur Zeiger Windows-Fehlerberichterstattung
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_V2
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefd313f0edcc122708f141cd65418beaade03a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342872"
---
# <a name="stowed_exception_information_v2-structure"></a>Struktur der verstauten \_ Ausnahme \_ Informationen \_ v2

Enthält Informationen zu gestaut-Ausnahme.

## <a name="syntax"></a>Syntax


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_V2 {
  STOWED_EXCEPTION_INFORMATION_HEADER Header;
  HRESULT                             ResultCode;
  struct {
    DWORD ExceptionForm  :2;
    DWORD ThreadId  :30;
  };
  union {
    struct {
      PVOID ExceptionAddress;
      ULONG StackTraceWordSize;
      ULONG StackTraceWords;
      PVOID StackTrace;
    };
    struct {
      PWSTR ErrorText;
    };
  };
  ULONG                               NestedExceptionType;
  PVOID                               NestedException;
} STOWED_EXCEPTION_INFORMATION_V2, *PSTOWED_EXCEPTION_INFORMATION_V2;
```



## <a name="members"></a>Member

<dl> <dt>

**Header**
</dt> <dd>

Typ: **[ **\_ \_ \_ Header der Ausnahme Informationen**](stowed-exception-information-header.md)**

</dd> <dd>

Die Struktur der [**verstauten \_ Ausnahme \_ Informationen \_**](stowed-exception-information-header.md) , die Informationen für diese übergeordnete Struktur enthält.

</dd> <dt>

**ResultCode**
</dt> <dd>

Typ: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Der [**HRESULT**](/windows/desktop/WinProg/windows-data-types) -Code für die gestaut-Ausnahme.

</dd> <dt>

**Exceptionform**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Ein 2-Bit-Wert, der die Form der Ausnahme identifiziert.



| Wert                                                                                                                                                                                                                                                                  | Bedeutung                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> <dt>**Verstauaut \_ Ausnahme \_ Formular \_ Binär**</dt> <dt>0x01</dt> </dl> | Dieser Wert gibt an, dass die Form der Ausnahme binär ist.<br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> <dt>**Verstauaut \_ Ausnahme \_ Formular \_ Text**</dt> <dt>0x02</dt> </dl>       | Dieser Wert gibt an, dass die Form der Ausnahme Text ist.<br/>   |



 

</dd> <dt>

**ThreadID**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Ein 30-Bit-Wert, der den Thread identifiziert, der die Ausnahme ausgelöst hat. Der Wert wird nach rechts um 2 Bits verschoben, wenn er gespeichert wird. Um Sie wieder in eine gültige Thread-ID zu konvertieren, verschieben Sie den Wert nach links um 2. Beispiel:

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

(*unbenannte Struktur*)
</dt> <dd>

Die Member dieser Struktur sind nur gültig, wenn der **exceptionform** -Member auf die **\_ \_ \_ Binärdatei** mit dem Typ "Binary Exception" festgelegt ist.

<dl> <dt>

**ExceptionAddress**
</dt> <dd>

Typ: **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Ein Zeiger, der die Ausnahme Adresse enthält.

</dd> <dt>

**Stacktracewordsize**
</dt> <dd>

Typ: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Größe (in Bytes) der einzelnen Wörter in der Stapel Überwachung, auf die das **StackTrace** -Element zeigt. Dieser Wert wird für 32-Bit-Plattformen auf 4 und für 64-Bit-Plattformen auf 8 festgelegt.

</dd> <dt>

**Stacktracewords**
</dt> <dd>

Typ: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Anzahl der Wörter in der Stapel Überwachung, auf die das **StackTrace** -Element zeigt. Die Anzahl von Wörtern ist gleich der Anzahl der Elemente im Array.

</dd> <dt>

**StackTrace**
</dt> <dd>

Typ: **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Ein Zeiger auf einen Speicherblock, der die Stapel Überwachung enthält.

</dd> </dl> </dd> <dt>

(*unbenannte Struktur*)
</dt> <dd>

Der Member dieser Struktur ist nur gültig, wenn der **exceptionform** -Member auf den **\_ \_ Formular \_ Text "gestaut**" festgelegt ist.

<dl> <dt>

**ErrorText**
</dt> <dd>

Typ: **[ **pwstr**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Fehlertext der Ausnahme enthält.

</dd> </dl> </dd> <dt>

**"Netstedexceptiontype"**
</dt> <dd>

Typ: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Ein 32-Bit-Wert, der den Objekttyp angibt, auf den das **arstedexception** -Element verweist. Definieren Sie den Wert mit diesem Byte Swap Type-Definition-Makro, das Little-Endian annimmt:

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

Im folgenden finden Sie einige allgemeine Typdefinitionen:



| Wert                                                                                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> <dt>**Verstauaut \_ Ausnahme beim \_ \_ Typ " \_ keine**</dt> " <dt>(0x00000000)</dt> </dl>                                  | Dieser Wert gibt an, dass es kein Objekt für eine nicht-unter-Ausnahme gibt.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> <dt>**Verstauaut \_ Ausnahme beim \_ \_ Typ "Typ der \_ Win32**</dt> - <dt>verstaute \_ Ausnahme \_ \_ " ("W32E")</dt> . </dl>    | Dieser Wert gibt an, dass das Element " **arstedexception** " auf ein [**Ausnahme \_ Daten Satz**](/windows/desktop/api/winnt/ns-winnt-exception_record) Objekt verweist.<br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> <dt>**Verstauaut \_ vom Typ "Ausnahme beim \_ \_ Typ" \_ gestaut**</dt> <dt>" \_ \_ eingestaubte Ausnahme \_ (" STOW ")</dt> </dl> | Dieser Wert gibt an, dass das Element " **arstedexception** " auf ein anderes gestabgestktes Objekt zeigt. Das andere gestaut-Ausnahme Objekt kann ein **gestaut- \_ Ausnahme \_ Informations \_** Objekt oder eine andere Version mit einem gültigen **Header** Element sein, d. h. ein **Header** Element, das einen gültigen Header für eine [**verstaute \_ Ausnahme \_ \_**](stowed-exception-information-header.md)enthält.<br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> <dt>**Verstauaut \_ Typ der Ausnahme beim \_ \_ Typ " \_ CLR**</dt> -gestaut" mit Ausnahme des Typs <dt> \_ \_ \_ "Datei clr1"</dt> . </dl>          | Dieser Wert gibt an, dass das Element " **netstedexception** " auf ein "Datei clr1"-Ausnahme Objekt verweist.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> <dt>**Verstauaut \_ Typ der Ausnahme, die \_ \_ vom Typ " \_ Leo**</dt> -gestaut" ausgelöst wurde <dt> \_ \_ \_ ("LEO1")</dt> </dl>          | Dieser Wert gibt an, dass das Element " **netstedexception** " auf ein sprach Ausnahme Objekt verweist.<br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

**"Netstedexception"**
</dt> <dd>

Typ: **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Ein Zeiger auf einen Typ der Typ-Typ-Ausnahme. Der Objekttyp wird durch den Member " **netstedexceptiontype** " angegeben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**Verstauaut \_ Ausnahme \_ Informationen \_ v2** -und [**gestaut- \_ Ausnahme \_ Informations \_ Header**](stowed-exception-information-header.md) sind zurzeit nicht in einem Header definiert, der öffentlich verfügbar ist, sodass Sie Sie im Quellcode definieren müssen, bevor Sie Sie verwenden.

Die Struktur der **verstauten \_ Ausnahme \_ Informationen \_ v1** ist mit dieser Struktur identisch, außer Sie enthält nicht die Member " **netstedexceptiontype** " und " **netstedexception** ".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                         |
| Header<br/>                   | <dl> <dt>None</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ausnahme \_ Daten Satz**](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[**Header für verstaute \_ Ausnahme \_ Informationen \_**](stowed-exception-information-header.md)
</dt> </dl>

 

