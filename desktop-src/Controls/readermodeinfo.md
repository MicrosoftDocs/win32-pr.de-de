---
title: READERMODEINFO-Struktur
description: Enthält Informationen, die zum Initialisieren der DoReaderMode-Funktion erforderlich sind.
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- READERMODEINFO-Struktur Windows Controls
- PREADERMODEINFO-Strukturzeiger Windows-Steuerelemente
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 510dc7a763d50b42f06b2510e609e0bc7c3c6f31fa1f4c08393964cef75487fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169120"
---
# <a name="readermodeinfo-structure"></a>READERMODEINFO-Struktur

\[**READERMODEINFO** wird über Windows XP mit Service Pack 2 (SP2) unterstützt. In nachfolgenden Versionen wird sie möglicherweise nicht unterstützt.\]

Enthält Informationen, die zum Initialisieren der [**DoReaderMode-Funktion**](doreadermode.md) erforderlich sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagReaderModeInfo {
  UINT                       cbSize;
  HWND                       hwnd;
  DWORD                      fFlags;
  LPRECT                     prc;
  PFNREADERSCROLL            pfnScroll;
  PFNREADERTRANSLATEDISPATCH fFlags;
  LPARAM                     lParam;
} READERMODEINFO, *PREADERMODEINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**cbSize**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Erforderlich. Die Größe der -Struktur in Bytes. Legen Sie diesen Parameter auf **sizeof(READERMODE)** fest, bevor Sie [**DoReaderMode**](doreadermode.md)aufrufen.

</dd> <dt>

**Hwnd**
</dt> <dd>

Typ: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Erforderlich. Das Handle des Fensters, das für den Readermodus verwendet werden soll.

</dd> <dt>

**fFlags**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Flags, die die Funktionalität des Readermodusfensters anpassen. Dieser Parameter kann 0 sein. andernfalls einer oder mehrere der folgenden Werte.



| Wert                                                                                                                                                                                                                                  | Bedeutung                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <dt>**RMF \_ ZEROCURSOR**</dt> <dt>0x01</dt> </dl>             | Legt den Cursor in der Mitte des in **prc** angegebenen Bereichs fest. Wenn dieses Flag nicht angegeben ist, bleibt die Cursorposition unverändert.<br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <dt>**RMF \_ VERTICALONLY-0x02**</dt> <dt></dt> </dl>       | Lässt nur vertikales Scrollen zu.<br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <dt>**RMF \_ HORIZONTALONLY-0x04**</dt> <dt></dt> </dl> | Ermöglicht nur horizontales Scrollen.<br/>                                                                                                     |



 

</dd> <dt>

**Vr china**
</dt> <dd>

Typ: **LPRECT**

</dd> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die den Bildlaufbereich im Readermodusfenster angibt. Wenn dieser Member **NULL** ist, wird das gesamte Fenster als Bildlaufbereich verwendet.

</dd> <dt>

**pfnScroll**
</dt> <dd>

Typ: **PFNREADERSCROLL**

</dd> <dd>

Ein Zeiger auf eine anwendungsdefinierte [*ReaderScroll-Rückruffunktion, mit*](readerscroll.md) der die Anwendung benachrichtigt wird, dass das Fenster in einer bestimmten Richtung gescrollt werden muss.

</dd> <dt>

**fFlags**
</dt> <dd>

Typ: **PFNREADERTRANSLATEDISPATCH**

</dd> <dd>

Ein Zeiger auf eine anwendungsdefinierte [*TranslateDispatch-Rückruffunktion, die*](translatedispatch.md) verwendet wird, um die erste Benachrichtigung über alle Nachrichten zu erhalten, die an das Readermodusfenster gesendet werden.

</dd> <dt>

**lParam**
</dt> <dd>

Typ: **[ **LPARAM**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Zusätzliche Informationen, die von der Anwendung benötigt werden und vom Aufrufer in der [*Rückruffunktion ReaderScroll*](readerscroll.md) gelesen werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird in keinem öffentlichen Header deklariert. Um sie zu verwenden, müssen Sie die oben gezeigte Deklaration in Ihren eigenen Header einfügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, nur Windows \[ Vista-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>          |



 

