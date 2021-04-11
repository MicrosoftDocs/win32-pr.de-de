---
title: Readerscroll-Rückruffunktion
description: Eine von der Anwendung definierte Rückruffunktion, die verwendet wird, wenn der Mauszeiger in den Teil des lesemodusfensters verschoben wird, der als aktiver scrollbereich deklariert wurde.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- Windows-Steuerelemente für readerscroll-Rückruf Funktionen
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
ms.openlocfilehash: 0db5a80b84a30362e3bdbce45fe7485ad0dd6884
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949815"
---
# <a name="readerscroll-callback-function"></a>Readerscroll-Rückruffunktion

\[*Readerscroll* ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Eine von der Anwendung definierte Rückruffunktion, die verwendet wird, wenn der Mauszeiger in den Teil des lesemodusfensters verschoben wird, der als aktiver scrollbereich deklariert wurde.

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

*prmi* \[ in\]
</dt> <dd>

Typ: **preadermodeinfo**

Ein Zeiger auf die [**readermodumfo**](readermodeinfo.md) -Struktur, die an die [**doreadermode**](doreadermode.md) -Funktion weitergegeben wurde. Diese Struktur definiert das Fenster Lesemodus und den aktiven scrollbereich.

</dd> <dt>

*DX* \[ in\]
</dt> <dd>

Typ: **int**

Der Abstand, der horizontal durchlaufen werden soll. Wenn das RMF \_ verticalonly-Flag in der [**readermodeinfo**](readermodeinfo.md) -Struktur festgelegt ist, ist dieser Wert immer 0.

</dd> <dt>

*dy* \[ in\]
</dt> <dd>

Typ: **int**

Der Abstand, der vertikal durchlaufen werden soll. Wenn das RMF- \_ Flag horizontalonly in der [**readermodeinfo**](readermodeinfo.md) -Struktur festgelegt ist, ist dieser Wert immer 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Diese Funktion sollte immer **true** zurückgeben.

## <a name="remarks"></a>Bemerkungen

Wenn die Anwendung eine Benachrichtigung von dieser Funktion empfängt, ist die Anwendung dafür verantwortlich, das Fenster des Lesemodus in der durch die *DX* -und *dy* -Parameter angegebenen Richtung zu scrollen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Implementierung dieser Funktion mithilfe einer benutzerdefinierten Funktion für den Bildlauf dargestellt.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista, Windows Vista \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>          |



 

