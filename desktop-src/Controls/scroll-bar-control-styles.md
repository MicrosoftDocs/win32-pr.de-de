---
title: ScrollBar-Steuerelement Stile (Winuser. h)
description: Zum Erstellen eines Schiebe leisten-Steuer Elements mithilfe der Funktion "up Window" oder "deatewindowex" geben Sie die ScrollBar-Klasse, die entsprechenden Fenster Stil Konstanten und eine Kombination der folgenden Stile für ScrollBar-Steuerelemente an.
ms.assetid: 07195a95-eff8-4a47-926a-9d503fa7b299
topic_type:
- apiref
api_name:
- SBS_BOTTOMALIGN
- SBS_HORZ
- SBS_LEFTALIGN
- SBS_RIGHTALIGN
- SBS_SIZEBOX
- SBS_SIZEBOXBOTTOMRIGHTALIGN
- SBS_SIZEBOXTOPLEFTALIGN
- SBS_SIZEGRIP
- SBS_TOPALIGN
- SBS_VERT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc5de721fd4cc44867fca0dbe1b35dcaf58c6dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366682"
---
# <a name="scroll-bar-control-styles"></a>ScrollBar-Steuerelement Stile

Zum Erstellen eines Schiebe leisten-Steuer Elements mithilfe der Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**deatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " geben Sie die ScrollBar-Klasse, die entsprechenden Fenster Stil Konstanten und eine Kombination der folgenden Stile für ScrollBar-Steuerelemente an. Einige der Stile erstellen ein ScrollBar-Steuerelement, das eine Standardbreite oder-Höhe verwendet. Allerdings müssen Sie immer die x-und y-Koordinaten und die anderen Dimensionen der Bild Lauf Leiste angeben, wenn Sie "up **Window** " oder " **kreatewindowex**" aufrufen.



| Konstante                                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SBS_BOTTOMALIGN"></span><span id="sbs_bottomalign"></span><dl> <dt>**SSB- \_ bottomalign**</dt> </dl>                                     | Richtet den unteren Rand der Bild Lauf Leiste am unteren Rand des Rechtecks aus, das durch die Parameter " *x*", " *y*", " *nwidth*" und " *nheight* " der Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " definiert wird. Die Bild Lauf Leiste verfügt über die Standardhöhe für System Scrollleisten. Verwenden Sie diesen Stil mit dem SSB- \_ Horz-Stil.<br/>                      |
| <span id="SBS_HORZ"></span><span id="sbs_horz"></span><dl> <dt>**SSB \_ Horz**</dt> </dl>                                                          | Legt eine horizontale Schiebe Leiste fest. Wenn weder der SSB \_ bottomalign-noch der SSB- \_ TopAlign-Stil angegeben ist, enthält die Bild Lauf Leiste die Höhe, Breite und Position, die von den Parametern *x*, *y*, *nwidth* und *nheight* von " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" angegeben wird.<br/>                                                      |
| <span id="SBS_LEFTALIGN"></span><span id="sbs_leftalign"></span><dl> <dt>**SSB \_ leftalign**</dt> </dl>                                           | Richtet den linken Rand der Bild Lauf Leiste am linken Rand des Rechtecks aus, das durch die Parameter *x*, *y*, *nwidth* und *nheight* von " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" definiert wird. Die Bild Lauf Leiste verfügt über die Standardbreite für System Scrollleisten. Verwenden Sie diesen Stil mit dem SSB-Format " \_ Vert".<br/>                                    |
| <span id="SBS_RIGHTALIGN"></span><span id="sbs_rightalign"></span><dl> <dt>**SSB- \_ Rechte Ausrichtung**</dt> </dl>                                        | Richtet den rechten Rand der Bild Lauf Leiste an den rechten Rand des Rechtecks aus, das durch die Parameter *x*, *y*, *nwidth* und *nheight* von " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" definiert wird. Die Bild Lauf Leiste verfügt über die Standardbreite für System Scrollleisten. Verwenden Sie diesen Stil mit dem SSB-Format " \_ Vert".<br/>                                  |
| <span id="SBS_SIZEBOX"></span><span id="sbs_sizebox"></span><dl> <dt>**SSB \_ SizeBox**</dt> </dl>                                                 | Legt ein Größen Feld fest. Wenn Sie weder den SSB \_ sizeboxbottomrightalign noch den SSB \_ sizeboxtopleftalign-Stil angeben, enthält das Größen Feld die Höhe, Breite und Position, die von den Parametern *x*, *y*, *nwidth* und *nheight* von " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" angegeben wird. <br/>                                          |
| <span id="SBS_SIZEBOXBOTTOMRIGHTALIGN"></span><span id="sbs_sizeboxbottomrightalign"></span><dl> <dt>**SSB \_ sizeboxbottomrightalign**</dt> </dl> | Richtet die untere rechte Ecke des Felds Größe an der unteren rechten Ecke des Rechtecks aus, das durch die Parameter *x*, *y*, *nwidth* und *nheight* von " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" angegeben wird. Das Feld Größe hat die Standardgröße für die Felder Systemgröße. Verwenden Sie diesen Stil mit den Formaten SSB \_ SizeBox oder SSB \_ SizeGrip.<br/> |
| <span id="SBS_SIZEBOXTOPLEFTALIGN"></span><span id="sbs_sizeboxtopleftalign"></span><dl> <dt>**SSB \_ sizeboxtopleftalign**</dt> </dl>             | Richtet die linke obere Ecke des Felds Größe an der oberen linken Ecke des Rechtecks aus, das durch die Parameter *x*, *y*, *nwidth* und *nheight* von " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" angegeben wird. Das Feld Größe hat die Standardgröße für die Felder Systemgröße. Verwenden Sie diesen Stil mit den Formaten SSB \_ SizeBox oder SSB \_ SizeGrip.<br/>   |
| <span id="SBS_SIZEGRIP"></span><span id="sbs_sizegrip"></span><dl> <dt>**SSB- \_ SizeGrip**</dt> </dl>                                              | Wie SSB \_ SizeBox, aber mit einer erhöhten Kante. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="SBS_TOPALIGN"></span><span id="sbs_topalign"></span><dl> <dt>**SSB- \_ TopAlign**</dt> </dl>                                              | Richtet den oberen Rand der Bild Lauf Leiste am oberen Rand des Rechtecks aus, das durch die Parameter " *x*", " *y*", " *nwidth*" und " *nheight* " von " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" definiert wird. Die Bild Lauf Leiste verfügt über die Standardhöhe für System Scrollleisten. Verwenden Sie diesen Stil mit dem SSB- \_ Horz-Stil.<br/>                                     |
| <span id="SBS_VERT"></span><span id="sbs_vert"></span><dl> <dt>**SSB- \_ ververt**</dt> </dl>                                                          | Bezeichnet eine vertikale Schiebe Leiste. Wenn Sie weder die SSB- \_ Rechte Ausrichtung noch den SSB- \_ Stil "leftalign" angeben, weist die Bild Lauf Leiste die Höhe, Breite und Position auf, die durch die Parameter " *x*", " *y*", " *nwidth*" und " *nheight* " von " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)"<br/>                                                     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

