---
title: TB_SETIMAGELIST Meldung (kommstrg. h)
description: Legt die Bildliste fest, die die Symbolleiste zum Anzeigen von Schaltflächen verwendet, die sich in Ihrem Standardzustand befinden.
ms.assetid: 432ffdfc-bb63-4405-90da-9392910fdbb6
keywords:
- Windows-Steuerelemente für TB_SETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TB_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0b7ad631e8b56824ae65a2b262c5478611e75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346515"
---
# <a name="tb_setimagelist-message"></a>TB \_ SetImageList-Meldung

Legt die Bildliste fest, die die Symbolleiste zum Anzeigen von Schaltflächen verwendet, die sich in Ihrem Standardzustand befinden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[Version 5,80.](common-control-versions.md) Der Index der Liste. Wenn Sie nur eine Bildliste oder eine frühere Version der allgemeinen Steuerelemente verwenden, legen Sie *wParam* auf NULL fest. Weitere Informationen zur Verwendung mehrerer Bildlisten finden Sie unter "Hinweise".

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für die festzulegende Bildliste. Wenn dieser Parameter **null** ist, werden keine Bilder in den Schaltflächen angezeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die Bildliste zurück, die zuvor zum Anzeigen von Schaltflächen in Ihrem Standardzustand verwendet wurde, oder **null** , wenn zuvor keine Bildliste festgelegt wurde.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Anwendung ist dafür verantwortlich, die Bildliste freizugeben, nachdem die Symbolleiste zerstört wurde.

 

Die **TB- \_ SetImageList** -Nachricht kann nicht mit [**TB \_ AddBitmap**](tb-addbitmap.md)kombiniert werden. Sie kann auch nicht mit Symbolleisten verwendet werden, die mit " [**kreatetoolbarex**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)" erstellt wurden, wodurch " **TB \_ AddBitmap** " intern aufgerufen wird. Wenn Sie eine Symbolleiste mit " **kreatetoolbarex** " erstellen oder zum Hinzufügen von Bildern " **TB \_ AddBitmap** " verwenden, wird die Bildliste von der Symbolleiste intern verwaltet. Der Versuch, ihn mit **TB \_ SetImageList** zu ändern, hat unvorhersehbare Konsequenzen.

Bei [Version 5,80](common-control-versions.md) oder höher der allgemeinen Steuerelemente müssen Schaltflächen Bilder nicht aus derselben Bildliste stammen. So verwenden Sie mehrere Bildlisten für Ihre Symbolleisten-Schaltflächen Bilder:

1.  Aktivieren Sie mehrere Bildlisten, indem Sie das Symbolleisten-Steuerelement eine [**ccm- \_ setVersion**](ccm-setversion.md) -Nachricht mit *wParam* (Versionsnummer) an 5 senden.
2.  Senden Sie für jede Bildliste, die Sie verwenden möchten, das Symbolleisten-Steuerelement eine **TB- \_ SetImageList** -Nachricht. Legen Sie *wParam* auf einen von der Anwendung definierten *wParam* -Wert fest, der verwendet wird, um die Liste zu identifizieren. Legen Sie *LPARAM* auf das HIMAGELIST-Handle der Liste fest.
3.  Legen Sie für jede Schaltfläche den **ibitmap** -Member der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur der Schaltfläche auf makelong (*iIndex*, *iimageid*) fest. Der *iimageid* -Wert ist die ID der entsprechenden Bildliste, die in Schritt 2 definiert wurde. Der *iIndex* -Wert ist der Index des jeweiligen Bilds in dieser Liste.
4.  Fügen Sie die Schaltflächen hinzu, indem Sie das Symbolleisten-Steuerelement an eine [**TB- \_ AddButtons**](tb-addbuttons.md)

Im folgenden Code Fragment wird veranschaulicht, wie einer Symbolleiste mit Bildern aus drei verschiedenen Bildlisten fünf Schaltflächen hinzugefügt werden. Die Unterstützung für mehrere Bildlisten wird mit einer [**ccm- \_ setVersion**](ccm-setversion.md) -Nachricht aktiviert. Anschließend werden die Bildlisten und die zugewiesenen IDs 0-2 festgelegt. Den Schaltflächen werden Bilder aus den Bildlisten wie folgt zugewiesen:

-   Die Schaltfläche 0 ist aus der Bildliste NULL (ahim \[ 0 \] ) mit dem Index 1.
-   Schaltfläche 1 ist von der Bildliste 1 (ahim \[ 1 \] ) mit dem Index 1.
-   Schaltfläche 2 basiert auf der Bildliste 2 (ahim \[ 2 \] ) mit einem Index von 1.
-   Schaltfläche 3 ist von Image List Zero (ahim \[ 0 \] ) mit einem Index von 2.
-   Schaltfläche 4 basiert auf der Bildliste 1 (ahim \[ 1 \] ) mit einem Index von 3.

Zum Schluss werden dem Symbolleisten-Steuerelement mit einer [**TB- \_ AddButtons**](tb-addbuttons.md) -Meldung die Schaltflächen hinzugefügt.


```
//Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 2, (LPARAM)ahiml[2]);

    // Create the five buttons
    TBBUTTON rgtb[5];
    
    //... initialize the TBBUTTON structures as usual ...
    
    //Assign images to each button
    rgtb[0].iBitmap = MAKELONG(1, 0);
    rgtb[1].iBitmap = MAKELONG(1, 1);
    rgtb[2].iBitmap = MAKELONG(1, 2);
    rgtb[3].iBitmap = MAKELONG(2, 0);
    rgtb[4].iBitmap = MAKELONG(3, 1);

    // Add the five buttons to the toolbar control
    SendMessage(hwndTB, TB_ADDBUTTONS, 5, (LPARAM)(&rgtb);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Makelong**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))
</dt> </dl>

 

