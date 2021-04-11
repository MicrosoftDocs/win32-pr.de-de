---
title: Translatedispatch-Rückruffunktion
description: Wird vom Client der doreadermode-Funktion zum Abfangen und expliziten verarbeiten von Windows-Meldungen verwendet, die für den scrollbereich des Fensters "Lesemodus" bestimmt sind. Dies ist eine Anwendungs definierte Rückruffunktion.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- Windows-Steuerelemente für translatedispatch-Rückruf Funktionen
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
ms.openlocfilehash: 1230ed1e65f8d739f9a0a05e4788eb919c45c4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949767"
---
# <a name="translatedispatch-callback-function"></a>Translatedispatch-Rückruffunktion

\[*Translatedispatch* ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Wird vom Client der [**doreadermode**](doreadermode.md) -Funktion zum Abfangen und expliziten verarbeiten von Windows-Meldungen verwendet, die für den scrollbereich des Fensters "Lesemodus" bestimmt sind. Dies ist eine Anwendungs definierte Rückruffunktion.

## <a name="syntax"></a>Syntax


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpmsg* \[ in\]
</dt> <dd>

Typ: * Konstante *[**msg**](/windows/win32/api/winuser/ns-winuser-msg) \** _

Ein Zeiger auf eine [_ *msg* *](/windows/win32/api/winuser/ns-winuser-msg) -Struktur, die die abgefangene Meldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

**True** , wenn die Meldung von dieser Funktion behandelt wurde. andernfalls **false**. Wenn der Wert **false** ist, wird die Nachricht von der Standard Implementierung des Lesemodus verarbeitet. Diese Implementierung behandelt die Mausbewegung und Schaltflächen sowie Tastendruck.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista, Windows Vista \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>          |



 

