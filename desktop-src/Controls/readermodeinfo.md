---
title: Readermodumfo-Struktur
description: Enthält Informationen, die zum Initialisieren der doreadermode-Funktion erforderlich sind.
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- Readermodeingefo-Struktur Windows-Steuerelemente
- Preadermodeingefo-Struktur Zeiger-Windows-Steuerelemente
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dacf0fc59ef62447ca12b7a470689e13967d687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477853"
---
# <a name="readermodeinfo-structure"></a>Readermodumfo-Struktur

\[**Readermodeinfo** wird durch Windows XP mit Service Pack 2 (SP2) unterstützt. Dies wird in nachfolgenden Versionen möglicherweise nicht unterstützt.\]

Enthält Informationen, die zum Initialisieren der [**doreadermode**](doreadermode.md) -Funktion erforderlich sind.

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

**CBSIZE**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Erforderlich. Die Größe der-Struktur in Bytes. Legen Sie diesen Parameter auf **sizeof (readermode)** fest, bevor Sie " [**doreadermode**](doreadermode.md)" aufrufen.

</dd> <dt>

**HWND**
</dt> <dd>

Typ: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Erforderlich. Das Handle des Fensters, das für den Lesemodus verwendet werden soll.

</dd> <dt>

**fFlags**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Flags, mit denen die Funktionalität des Fensters "Lesemodus" angepasst wird. Dieser Parameter kann 0 sein. andernfalls ein oder mehrere der folgenden Werte.



| Wert                                                                                                                                                                                                                                  | Bedeutung                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <dt>**RMF \_ NULL**</dt> <dt>0x01</dt> </dl>             | Legt den Cursor in der Mitte des Bereichs fest, der in der **Volksrepublik China** angegeben ist. Wenn dieses Flag nicht angegeben wird, bleibt die Cursorposition unverändert.<br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <dt>**RMF \_ Verticalonly**</dt> <dt>0x02</dt> </dl>       | Ermöglicht nur das vertikale Scrollen.<br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <dt>**RMF \_ Horizontalonly**</dt> <dt>0x04</dt> </dl> | Ermöglicht nur horizontales Scrollen.<br/>                                                                                                     |



 

</dd> <dt>

**PRC**
</dt> <dd>

Typ: **lprect**

</dd> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die den scrollbereich im Fenster "Lesemodus" angibt. Wenn dieser Member **null** ist, wird das gesamte Fenster als scrollbereich verwendet.

</dd> <dt>

**pfnscroll**
</dt> <dd>

Typ: **pfnreaderscroll**

</dd> <dd>

Ein Zeiger auf eine Anwendungs definierte [*readerscroll*](readerscroll.md) -Rückruffunktion, mit der die Anwendung benachrichtigt wird, dass das Fenster in einer bestimmten Richtung gescrollt werden muss.

</dd> <dt>

**fFlags**
</dt> <dd>

Typ: **pfnreadertranslatedispatch**

</dd> <dd>

Ein Zeiger auf eine Anwendungs definierte [*translatedispatch*](translatedispatch.md) -Rückruffunktion, die verwendet wird, um die erste Benachrichtigung über alle an das Fenster des Lesemodus gesendeten Nachrichten zu erhalten.

</dd> <dt>

**lParam**
</dt> <dd>

Typ: **[ **LPARAM**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Zusätzliche Informationen, die von der Anwendung benötigt werden, die vom Aufrufer in der [*readerscroll*](readerscroll.md) -Rückruffunktion gelesen werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur ist in keinem öffentlichen Header deklariert. Um es zu verwenden, müssen Sie die oben gezeigte Deklaration in ihren eigenen Header einschließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista, Windows Vista \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>          |



 

