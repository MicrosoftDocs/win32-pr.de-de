---
description: Wird an eine Anwendung gesendet, wenn der IME den Kompositions Status als Ergebnis einer Tastatureingabe ändert. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: WM_IME_COMPOSITION Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960924"
---
# <a name="wm_ime_composition-message"></a>WM \_ IME- \_ Kompositions Nachricht

Wird an eine Anwendung gesendet, wenn der IME den Kompositions Status als Ergebnis einer Tastatureingabe ändert. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,     
  WM_IME_COMPOSITION,   
  WPARAM wParam,
  LPARAM lParam          
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Ein Handle für Fenster.

</dd> <dt>

*wParam* 
</dt> <dd>

DBCS-Zeichen, das die letzte Änderung an der Kompositions Zeichenfolge darstellt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Wert, der angibt, wie die Kompositions Zeichenfolge oder das Zeichen Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen. Weitere Informationen zu diesen Werten finden Sie unter [IME-Kompositions Zeichen folgen Werte](ime-composition-string-values.md).

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

**GCS- \_ compattr**
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

**GCS- \_ compclause**
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

**GCS- \_ compreadstr**
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

**GCS- \_ compreadattr**
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

**GCS- \_ compreadclause**
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

**GCS \_ compstr**
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

**GCS- \_ Cursor**
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

**GCS \_ Delta Start**
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

**GCS- \_ resultclause**
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

**GCS- \_ resultreadclause**
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

**GCS- \_ resultreadstr**
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

**GCS- \_ ResultStr**
</dt> </dl>

Der *LPARAM* -Parameter kann auch einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <dt>**CS- \_ insertchar**</dt> </dl>    | Fügen Sie das *wParam* -Kompositions Zeichen an der aktuellen Einfügemarke ein. Eine Anwendung sollte das Kompositions Zeichen anzeigen, wenn diese Nachricht verarbeitet wird.<br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <dt>**CS \_ nomovecaret**</dt> </dl> | Verschieben Sie die Position der Einfügemarke nicht als Ergebnis der Verarbeitung der Nachricht. Wenn ein IME z. b. eine Kombination aus CS \_ insertchar und CS \_ nomovecaret angibt, sollte die Anwendung das angegebene Zeichen an der aktuellen Position der Einfügemarke einfügen, aber die Einfügemarke nicht an die nächste Position verschieben. Diese Zeichenfolge wird durch eine nachfolgende WM \_ IME- \_ Kompositions Nachricht mit GCS \_ ResultStr ersetzt.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung sollte diese Nachricht verarbeiten, wenn Sie selbst Kompositions Zeichen anzeigt. Andernfalls sollte die Nachricht an das IME-Fenster gesendet werden.

Wenn die Anwendung ein IME-Fenster erstellt hat, sollte diese Meldung an dieses Fenster übergeben werden. Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  -Funktion verarbeitet diese Nachricht, indem Sie Sie an das IME-Standardfenster übergibt. Das IME-Fenster verarbeitet diese Nachricht, indem seine Darstellung basierend auf dem angegebenen Änderungsflag aktualisiert wird. Eine Anwendung kann " [**immgetcompositionstring**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) " aufrufen, um den neuen Kompositions Status abzurufen.

Wenn keiner der GCS \_ -Werte festgelegt wird, gibt die Meldung an, dass die aktuelle Komposition abgebrochen wurde, und Anwendungen, die die Kompositions Zeichenfolge zeichnen, sollten die Zeichenfolge löschen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                                                      |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen); </dt> <dt>Imm. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Eingabemethoden-Manager-Meldungen](input-method-manager-messages.md)
</dt> <dt>

[**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
