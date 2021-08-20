---
title: ReaderScroll-Rückruffunktion
description: Eine anwendungsdefinierte Rückruffunktion, die verwendet wird, wenn der Mauszeiger innerhalb des Teils des Readermodusfensters bewegt wird, der als aktiver Bildlaufbereich deklariert wurde.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- ReaderScroll-Rückruffunktion Windows Controls
topic_type:
- apiref
api_name:
- ReaderScroll
- PFNREADERSCROLL
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 554530e556161b4128199cda0a1a9d791f4f0ed75e8915c311d8945445486ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169110"
---
# <a name="readerscroll-callback-function"></a>ReaderScroll-Rückruffunktion

\[*ReaderScroll* ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Eine anwendungsdefinierte Rückruffunktion, die verwendet wird, wenn der Mauszeiger innerhalb des Teils des Readermodusfensters bewegt wird, der als aktiver Bildlaufbereich deklariert wurde.

## <a name="syntax"></a>Syntax


```C++
BOOL CALLBACK ReaderScroll(
  _In_ PREADERMODEINFO prmi,
  _In_ int             dx,
  _In_ int             dy
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*prmi* \[ In\]
</dt> <dd>

Typ: **PREADERMODEINFO**

Ein Zeiger auf die [**READERMODEINFO-Struktur,**](readermodeinfo.md) die an die [**DoReaderMode-Funktion**](doreadermode.md) übergeben wurde. Diese Struktur definiert das Readermodusfenster und den aktiven Bildlaufbereich.

</dd> <dt>

*dx* \[ in\]
</dt> <dd>

Typ: **int**

Der Abstand, in dem horizontal gescrollt werden soll. Wenn das RMF \_ VERTICALONLY-Flag in der [**READERMODEINFO-Struktur**](readermodeinfo.md) festgelegt ist, ist dieser Wert immer 0.

</dd> <dt>

*dy* \[ In\]
</dt> <dd>

Typ: **int**

Der Abstand, in dem vertikal gescrollt werden soll. Wenn das RMF \_ HORIZONTALONLY-Flag in der [**READERMODEINFO-Struktur**](readermodeinfo.md) festgelegt ist, ist dieser Wert immer 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

Diese Funktion sollte immer **TRUE** zurückgeben.

## <a name="remarks"></a>Hinweise

Wenn die Anwendung Benachrichtigungen von dieser Funktion empfängt, ist die Anwendung für das Scrollen des Readermodusfensters in die durch die *dx-* und *dy-Parameter* angegebene Richtung verantwortlich.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Implementierung dieser Funktion mithilfe einer benutzerdefinierten Funktion zum Durchführen des Bildlaufs beschrieben.


```C++
BOOL CALLBACK
ReaderScrollCallback(PREADERMODEINFO prmi, int dx, int dy)
{
    if (prmi == NULL) 
        return FALSE;

    // Call custom ScrollWindow method to scroll the window
    ScrollWindow(prmi->hwnd, dx, dy);
    
    return TRUE;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, nur Windows \[ Vista-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>          |



 

