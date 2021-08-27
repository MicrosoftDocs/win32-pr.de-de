---
title: TranslateDispatch-Rückruffunktion
description: Wird vom Client der DoReaderMode-Funktion zum Abfangen und expliziten Verarbeiten von Windows-Nachrichten verwendet, die für den Bildlaufbereich des Readermodusfensters vorgesehen sind. Dies ist eine anwendungsdefinierte Rückruffunktion.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- TranslateDispatch-Rückruffunktion Windows Controls
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08f726c3f56579260e96a882f1123d035df37cb3f7f71fd0ecbc47d41672359c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060530"
---
# <a name="translatedispatch-callback-function"></a>TranslateDispatch-Rückruffunktion

\[*TranslateDispatch* ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Wird vom Client der [**DoReaderMode-Funktion**](doreadermode.md) verwendet, um alle Windows-Meldungen abzufangen und explizit zu verarbeiten, die für den Scrollbereich des Readermodusfensters vorgesehen sind. Dies ist eine anwendungsdefinierte Rückruffunktion.

## <a name="syntax"></a>Syntax


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpmsg* \[ In\]
</dt> <dd>

Typ: **const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) \***

Ein Zeiger auf eine [**MSG-Struktur,**](/windows/win32/api/winuser/ns-winuser-msg) die die abgefangene Nachricht enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE,** wenn die Nachricht von dieser Funktion verarbeitet wurde; Andernfalls **FALSE**. **False** gibt an, dass die Nachricht von der Implementierung des Standardlesemodus behandelt wird. Diese Implementierung behandelt Mausbewegungen und Schaltflächen sowie Tastendrucke.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Implementierung dieser Funktion beschrieben.


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, nur Windows \[ Vista-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>          |



 

