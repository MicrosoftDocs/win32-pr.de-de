---
title: CDM_GETFOLDERIDLIST (Commdlg.h)
description: Ruft die Adresse der Elementbezeichnerliste ab, die dem Ordner entspricht, der derzeit im Dialogfeld Öffnen oder Speichern im Explorer-Stil geöffnet ist.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- CDM_GETFOLDERIDLIST-Dialogfelder
topic_type:
- apiref
api_name:
- CDM_GETFOLDERIDLIST
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f6a753cf53bdd2cde53a0e3df973457b50b8ed326a7d7ee50c05dc24f1d0a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786192"
---
# <a name="cdm_getfolderidlist-message"></a>CDM \_ GETFOLDERIDLIST-Nachricht

\[Ab Windows Vista wurden **die** allgemeinen  Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](../shell/common-file-dialog.md) Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]

Ruft die Adresse der Elementbezeichnerliste ab, die  dem Ordner entspricht, der derzeit im Dialogfeld Öffnen oder Speichern **im** Explorer-Stil geöffnet ist. Das Dialogfeld muss mit dem **\_ OFN-EXPLORER-Flag** erstellt worden sein. Andernfalls schlägt die Meldung fehl.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Größe des *lParam-Puffers* in Bytes.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf den Puffer, der die Liste der Elementbezeichner empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, entspricht der Rückgabewert der Größe der Liste der Elementbezeichner in Bytes. Dies ist entweder die Anzahl der in den Puffer kopierten Bytes oder die erforderliche Puffergröße, wenn der Puffer zu klein ist.

Wenn ein Fehler auftritt, ist der Rückgabewert kleiner als 0 (null).

## <a name="remarks"></a>Hinweise

Das entsprechende Makro lautet wie folgt:

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Commdlg.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

