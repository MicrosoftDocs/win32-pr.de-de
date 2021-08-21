---
title: TB_LOADIMAGES-Nachricht (Commctrl.h)
description: Lädt systemdefinierte Schaltflächenbilder in die Bildliste eines Symbolleistensteuerelements.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- TB_LOADIMAGES Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: df2cfae5e1658dec2652eb68cae4283dd0df697ad055434f1290cc0da7c2b485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168196"
---
# <a name="tb_loadimages-message"></a>TB \_ LOADIMAGES-Nachricht

Lädt systemdefinierte Schaltflächenbilder in die Bildliste eines Symbolleistensteuerelements.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Bezeichner einer systemdefiniert Schaltflächenbildliste. Dieser Parameter kann auf einen der folgenden Werte festgelegt werden.



| Wert                                                                                                                                                                                | Bedeutung                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <dt>**IDB \_ HIST \_ LARGE \_ COLOR**</dt> </dl> | Windows Explorerbitmaps in großer Größe.<br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <dt>**KLEINE \_ \_ \_ IDB HIST-FARBE**</dt> </dl> | Windows Explorerbitmaps in kleiner Größe.<br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <dt>**GROßE \_ \_ \_ IDB STD-FARBE**</dt> </dl>    | Standardbitmaps in großer Größe.<br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <dt>**KLEINE \_ \_ \_ IDB STD-FARBE**</dt> </dl>    | Standardbitmaps in kleiner Größe.<br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <dt>**IDB \_ VIEW \_ LARGE \_ COLOR**</dt> </dl> | Zeigen Sie Bitmaps in großer Größe an.<br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <dt>**IDB \_ VIEW SMALL COLOR \_ (IDB-ANSICHT, KLEINE \_ FARBE)**</dt> </dl> | Zeigen Sie Bitmaps in kleiner Größe an.<br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <dt>**IDB \_ HIST \_ NORMAL**</dt> </dl>                 | Windows Explorer-Reiseschaltflächen und Favoritenbitmaps im normalen Zustand.<br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <dt>**IDB \_ HIST \_ HOT**</dt> </dl>                          | Windows Explorer-Reiseschaltflächen und Favoritenbitmaps im heißen Zustand.<br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <dt>**IDB \_ HIST \_ DISABLED**</dt> </dl>           | Windows Explorer-Reiseschaltflächen und Favoritenbitmaps im deaktivierten Zustand.<br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <dt>**IDB \_ HIST \_ GEDRÜCKT**</dt> </dl>              | Windows Explorer-Reiseschaltflächen und Favoritenbitmaps im gedrückten Zustand.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Instanzhandle. Dieser Parameter muss auf HINST \_ COMMCTRL festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anzahl der Bilder in der Bildliste. Gibt 0 (null) zurück, wenn die Symbolleiste keine Bildliste enthält oder die vorhandene Bildliste leer ist.

## <a name="remarks"></a>Hinweise

Sie müssen die richtigen Imageindexwerte verwenden, wenn Sie [**TBBUTTON-Strukturen**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) vorbereiten, bevor Sie die [**\_ TB-ADDBUTTONS-Nachricht**](tb-addbuttons.md) senden. Eine Liste der Bildindexwerte für diese voreingestellten Bitmaps finden Sie unter [Symbolleiste Standardschaltfläche Bildindexwerte](toolbar-standard-button-image-index-values.md).

## <a name="examples"></a>Beispiele

Der folgende Beispielcode lädt die standardmäßigen kleinen Farbbilder des Systems.


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TB \_ ADDBITMAP**](tb-addbitmap.md)
</dt> </dl>

 

 





