---
title: TB_LOADIMAGES Meldung (kommstrg. h)
description: Lädt System definierte Schaltflächen Bilder in die Bildliste eines Symbolleisten-Steuer Elements.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- Windows-Steuerelemente für TB_LOADIMAGES Meldung
topic_type:
- apiref
api_name:
- TB_LOADIMAGES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0ba6bf75855a0b81ac56438489d7eced3d589
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478090"
---
# <a name="tb_loadimages-message"></a>TB- \_ loadimages-Nachricht

Lädt System definierte Schaltflächen Bilder in die Bildliste eines Symbolleisten-Steuer Elements.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Bezeichner einer System definierten Schaltflächen Bildliste. Dieser Parameter kann auf einen der folgenden Werte festgelegt werden.



| Wert                                                                                                                                                                                | Bedeutung                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <dt>**hohe IDB- \_ \_ \_ Farbe**</dt> </dl> | Windows Explorer-Bitmaps in großem Umfang.<br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <dt>**IDB \_ Hist \_ Small \_ Color**</dt> </dl> | Windows Explorer-Bitmaps in kleiner Größe.<br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <dt>**\_ \_ hohe Farbe für IDB Std \_**</dt> </dl>    | Standard Bitmaps in großem Umfang.<br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <dt>**IDB \_ Std \_ Small- \_ Farbe**</dt> </dl>    | Standard Bitmaps in kleiner Größe.<br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <dt>**IDB- \_ Sicht \_ große \_ Farbe**</dt> </dl> | Anzeigen von Bitmaps in großem Umfang.<br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <dt>**IDB- \_ Sicht \_ kleine \_ Farbe**</dt> </dl> | Bitmaps in kleiner Größe anzeigen.<br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <dt>**IDB- \_ Hist \_ Normal**</dt> </dl>                 | Windows-Explorer-Fahrten Schaltflächen und Favoriten Bitmaps im normalen Zustand.<br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <dt>**IDB- \_ Hist- \_ Hot**</dt> </dl>                          | Windows-Explorer-Reise Schaltflächen und Favoriten Bitmaps im aktiven Zustand.<br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <dt>**IDB- \_ Hist \_ deaktiviert**</dt> </dl>           | Windows-Explorer-Reise Schaltflächen und Favoriten Bitmaps in deaktiviertem Zustand.<br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <dt>**IDB \_ Hist \_ gedrückt**</dt> </dl>              | Windows-Explorer-Fahrten Schaltflächen und Favoriten Bitmaps im gedrückten Zustand.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Instanzhandle. Dieser Parameter muss auf hInst kommctrl festgelegt werden \_ .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anzahl der Bilder in der Bildliste. Gibt 0 (null) zurück, wenn die Symbolleiste keine Bildliste aufweist oder wenn die vorhandene Bildliste leer ist.

## <a name="remarks"></a>Bemerkungen

Sie müssen die richtigen Bild Indexwerte verwenden, wenn Sie die [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Strukturen vor dem Senden der [**TB- \_ AddButtons**](tb-addbuttons.md) -Nachricht vorbereiten. Eine Liste der Bild Indexwerte für diese vordefinierten Bitmaps finden Sie unter [Indexwerte der Symbolleisten-Standard Schaltfläche](toolbar-standard-button-image-index-values.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispielcode werden die System Standard-Small Color-Bilder geladen.


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TB \_ AddBitmap**](tb-addbitmap.md)
</dt> </dl>

 

 





