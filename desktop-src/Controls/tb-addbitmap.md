---
title: TB_ADDBITMAP Meldung (kommstrg. h)
description: Fügt der Liste der für eine Symbolleiste verfügbaren Schaltflächen Bilder mindestens ein Bild hinzu.
ms.assetid: 9040ab84-a5f3-4e4b-bc90-590b2ceeaa5a
keywords:
- Windows-Steuerelemente für TB_ADDBITMAP Meldung
topic_type:
- apiref
api_name:
- TB_ADDBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d83cba4b4dec9b490a3e8f41db9cc7721dd23b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743969"
---
# <a name="tb_addbitmap-message"></a>TB \_ AddBitmap-Meldung

Fügt der Liste der für eine Symbolleiste verfügbaren Schaltflächen Bilder mindestens ein Bild hinzu.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzahl von Schaltflächen Bildern in der Bitmap. Wenn *LPARAM* eine System definierte Bitmap angibt, wird dieser Parameter ignoriert.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**tbaddbitmap**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) -Struktur, die den Bezeichner einer Bitmapressource enthält, und das Handle für die Modul Instanz mit der ausführbaren Datei, die die Bitmap-Ressource enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des ersten neuen Bilds zurück, wenn erfolgreich, andernfalls-1.

## <a name="remarks"></a>Bemerkungen

Wenn die Symbolleiste mit [**der Funktion "**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) -Funktion" erstellt wurde, müssen Sie vor dem Senden von **TB \_ AddBitmap** die [**TB- \_ buttonstructsize**](tb-buttonstructsize.md) -Nachricht an die Symbolleiste senden.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Bitmap aus einer Ressource (IDB \_ bitmap1) erstellt, wobei die Hintergrundfarbe (in diesem Fall schwarz) der Vordergrundfarbe der System Schaltfläche zugeordnet und der Symbolleiste hinzugefügt wird.


```C++
DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &colorMap, 1);
TBADDBITMAP tb;
tb.hInst = NULL;
tb.nID = (UINT_PTR)hbm;

// hWndToolbar is the window handle of the toolbar.
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was 
// created by using CreateWindowEx.
int index = SendMessage (hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tb);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

