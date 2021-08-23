---
title: TB_SETIMAGELIST Meldung (Commctrl.h)
description: Legt die Bildliste fest, mit der die Symbolleiste Schaltflächen anzeigt, die sich im Standardzustand befinden.
ms.assetid: 432ffdfc-bb63-4405-90da-9392910fdbb6
keywords:
- TB_SETIMAGELIST Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: e6a7110084f2abe39cbae51815d1e59972cb016ea267275f0481d21e1f8b908a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167460"
---
# <a name="tb_setimagelist-message"></a>TB \_ SETIMAGELIST-Nachricht

Legt die Bildliste fest, mit der die Symbolleiste Schaltflächen anzeigt, die sich im Standardzustand befinden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[Version 5.80.](common-control-versions.md) Der Index der Liste. Wenn Sie nur eine Bildliste oder eine frühere Version der allgemeinen Steuerelemente verwenden, legen Sie *wParam* auf 0 (null) fest. Ausführliche Informationen zur Verwendung mehrerer Bildlisten finden Sie unter Hinweise.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für die festzulegende Bildliste. Wenn dieser Parameter **NULL** ist, werden in den Schaltflächen keine Bilder angezeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die Bildliste zurück, die zuvor zum Anzeigen von Schaltflächen im Standardzustand verwendet wurde, oder **NULL,** wenn zuvor keine Bildliste festgelegt wurde.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Ihre Anwendung ist dafür verantwortlich, die Bildliste frei zu machen, nachdem die Symbolleiste zerstört wurde.

 

Die **TB \_ SETIMAGELIST-Nachricht** kann nicht mit [**TB \_ ADDBITMAP**](tb-addbitmap.md)kombiniert werden. Sie kann auch nicht mit Symbolleisten verwendet werden, die mit [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)erstellt wurden und **intern TB \_ ADDBITMAP** aufrufen. Wenn Sie eine Symbolleiste mit **CreateToolbarEx** erstellen oder **TB \_ ADDBITMAP** zum Hinzufügen von Bildern verwenden, verwaltet die Symbolleiste die Bildliste intern. Der Versuch, es mit **TB \_ SETIMAGELIST** zu ändern, hat unvorhersehbare Folgen.

Mit [Version 5.80](common-control-versions.md) oder höher der allgemeinen Steuerelemente müssen Schaltflächenbilder nicht aus derselben Bildliste stammen. So verwenden Sie mehrere Bildlisten für Ihre Symbolleisten-Schaltflächenbilder:

1.  Aktivieren Sie mehrere Bildlisten, indem Sie dem Symbolleistensteuerelement eine [**CCM \_ SETVERSION-Nachricht**](ccm-setversion.md) senden, bei der *wParam* (version number) auf 5 festgelegt ist.
2.  Senden Sie für jede Bildliste, die Sie verwenden möchten, eine **TB \_ SETIMAGELIST-Nachricht** an das Symbolleistensteuerelement. Legen Sie *wParam* auf einen anwendungsdefiniert *wParam-Wert* fest, der zum Identifizieren der Liste verwendet wird. Legen Sie *lParam* auf das HIMAGELIST-Handle der Liste fest.
3.  Legen Sie für jede Schaltfläche den **iBitmap-Member** der [**TBBUTTON-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) der Schaltfläche auf MAKELONG(*iIndex*, *iImageID*) fest. Der *iImageID-Wert* ist die ID der entsprechenden Bildliste, die in Schritt 2 definiert wurde. Der *iIndex-Wert* ist der Index des bestimmten Bilds innerhalb dieser Liste.
4.  Fügen Sie die Schaltflächen hinzu, indem Sie dem Symbolleisten-Steuerelement eine [**\_ TB-ADDBUTTONS-Nachricht**](tb-addbuttons.md) senden.

Das folgende Codefragment veranschaulicht das Hinzufügen von fünf Schaltflächen zu einer Symbolleiste mit Bildern aus drei verschiedenen Bildlisten. Die Unterstützung für mehrere Bildlisten ist mit einer [**CCM \_ SETVERSION-Meldung**](ccm-setversion.md) aktiviert. Die Bildlisten werden dann festgelegt und IDs von 0-2 zugewiesen. Den Schaltflächen werden Bilder aus den Bildlisten wie folgt zugewiesen:

-   Schaltfläche 0 stammt aus der Bildliste 0 (ahim \[ \] 0) mit dem Index 1.
-   Schaltfläche 1 stammt aus der Bildliste 1 (ahim \[ \] 1) mit dem Index 1.
-   Schaltfläche 2 stammt aus der Bildliste 2 (ahim \[ 2 \] ) mit einem Index von 1.
-   Schaltfläche 3 stammt aus der Bildliste 0 (ahim \[ 0 \] ) mit einem Index von 2.
-   Schaltfläche 4 stammt aus der Bildliste 1 (ahim \[ \] 1) mit einem Index von 3.

Schließlich werden die Schaltflächen dem Symbolleistensteuerelement mit einer [**\_ TB-ADDBUTTONS-Meldung**](tb-addbuttons.md) hinzugefügt.


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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))
</dt> </dl>

 

