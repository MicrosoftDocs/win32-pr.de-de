---
title: CDM_GETSPEC Meldung (kommdlg. h)
description: Ruft den Dateinamen (ohne den Pfad) der aktuell ausgewählten Datei in einem Dialogfeld "Öffnen" oder "Speichern unter" im Explorer-Format ab.
ms.assetid: 22a67c92-bd24-4cba-bef8-291d241e6ec8
keywords:
- Dialog Felder CDM_GETSPEC Meldung
topic_type:
- apiref
api_name:
- CDM_GETSPEC
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2732bf2a8c581439a40538445853531b57cfc77a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102779"
---
# <a name="cdm_getspec-message"></a>CDM- \_ getSpec-Nachricht

\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt. Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]

Ruft den Dateinamen (ohne den Pfad) der aktuell ausgewählten Datei in einem Dialogfeld " **Öffnen** " oder "Speichern unter" im Explorer-Format **ab** . Das Dialogfeld muss mit dem **ofn- \_ Explorer** -Flag erstellt worden sein. andernfalls schlägt die Meldung fehl.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETSPEC             (CDM_FIRST + 0x0000)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Größe des *LPARAM* -Puffers in Zeichen.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf den Puffer, der den Dateinamen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert die Größe (in Zeichen) der Dateiname-Zeichenfolge, einschließlich des abschließenden NULL-Zeichens. Dies ist entweder die Anzahl von Bytes oder Zeichen, die in den Puffer kopiert werden, oder die erforderliche Puffergröße, wenn der Puffer zu klein ist.

Wenn ein Fehler auftritt, ist der Rückgabewert kleiner als 0 (null).

## <a name="remarks"></a>Bemerkungen

Das entsprechende Makro lautet wie folgt:

``` syntax
int CommDlg_OpenSave_GetSpec(hwnd, lparam, wparam); 
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommdlg. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

