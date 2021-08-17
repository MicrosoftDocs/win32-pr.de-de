---
title: Up-Down-Steuerelementstile (CommCtrl.h)
description: In diesem Abschnitt werden die Stile aufgelistet, die beim Erstellen von Up-Down-Steuerelementen verwendet werden.
ms.assetid: d35198cb-6a5b-485e-a914-1b2ede53462f
topic_type:
- apiref
api_name:
- UDS_ALIGNLEFT
- UDS_ALIGNRIGHT
- UDS_ARROWKEYS
- UDS_AUTOBUDDY
- UDS_HORZ
- UDS_HOTTRACK
- UDS_NOTHOUSANDS
- UDS_SETBUDDYINT
- UDS_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809ab4ce2c4d8670363dc7f0751ae4a3756ee7b4e5dc9b75c79986c3a56d359d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957699"
---
# <a name="up-down-control-styles"></a>Up-Down-Steuerelementstile

In diesem Abschnitt werden die Stile aufgelistet, die beim Erstellen von Up-Down-Steuerelementen verwendet werden.



| Konstante                                                                                                                                                            | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UDS_ALIGNLEFT"></span><span id="uds_alignleft"></span><dl> <dt>**UDS \_ ALIGNLEFT**</dt> </dl>       | Positioniert das Nach-unten-Steuerelement neben dem linken Rand des Fensters . Das Fenster "fenster" wird nach rechts verschoben, und seine Breite wird verringert, um die Breite des Auf-Ab-Steuerelements aufzunehmen.<br/>                                                                                                                                                                                                   |
| <span id="UDS_ALIGNRIGHT"></span><span id="uds_alignright"></span><dl> <dt>**UDS \_ ALIGNRIGHT**</dt> </dl>    | Positioniert das Steuerelement nach oben neben dem rechten Rand des Fensters . Die Breite des Fensters wird verringert, um die Breite des Nach-unten-Steuerelements aufzunehmen.<br/>                                                                                                                                                                                                                          |
| <span id="UDS_ARROWKEYS"></span><span id="uds_arrowkeys"></span><dl> <dt>**UDS \_ ARROWKEYS**</dt> </dl>       | Bewirkt, dass das Nach-unten-Steuerelement die Position erhöht und dekrementiert, wenn die NACH-OBEN-TASTE und DIE NACH-UNTEN-TASTE gedrückt werden.<br/>                                                                                                                                                                                                                                                                          |
| <span id="UDS_AUTOBUDDY"></span><span id="uds_autobuddy"></span><dl> <dt>**UDS \_ AUTOBUDDY**</dt> </dl>       | Wählt automatisch das vorherige Fenster in der Z-Reihenfolge als Fenster des Auf-Ab-Steuerelements aus.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="UDS_HORZ"></span><span id="uds_horz"></span><dl> <dt>**UDS \_ HORZ**</dt> </dl>                      | Bewirkt, dass die Pfeile des Steuerelements nach oben nach links und rechts anstatt nach oben und unten zeigen.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="UDS_HOTTRACK"></span><span id="uds_hottrack"></span><dl> <dt>**UDS \_ HOTTRACK**</dt> </dl>          | Bewirkt, dass das -Steuerelement ein "heißes Nachverfolgungsverhalten" aufweist. Das heißt, sie hebt den NACH-OBEN- und DEN NACH-UNTEN-PFEIL auf dem Steuerelement hervor, wenn der Zeiger über sie verläuft. Für diesen Stil ist Windows 98 oder Windows 2000 erforderlich. Wenn das System Windows 95 oder Windows NT 4.0 ausgeführt wird, wird das Flag ignoriert. Um zu überprüfen, ob hot tracking aktiviert ist, rufen [**Sie SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)auf. <br/> |
| <span id="UDS_NOTHOUSANDS"></span><span id="uds_nothousands"></span><dl> <dt>**UDS \_ NOTHOUSANDS**</dt> </dl> | Fügt kein Tausendertrennzeichen zwischen allen drei Dezimalstellen ein. <br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="UDS_SETBUDDYINT"></span><span id="uds_setbuddyint"></span><dl> <dt>**UDS \_ SETBUDDYINT**</dt> </dl> | Bewirkt, dass das Up-Down-Steuerelement den Text des Fensters "fenster" (mithilfe der [**WM \_ SETTEXT-Meldung)**](/windows/desktop/winmsg/wm-settext) einfügt, wenn sich die Position ändert. Der Text besteht aus der Position, die als Dezimal- oder Hexadezimalzeichenfolge formatiert ist.<br/>                                                                                                                                                             |
| <span id="UDS_WRAP"></span><span id="uds_wrap"></span><dl> <dt>**UDS \_ WRAP**</dt> </dl>                      | Bewirkt, dass die Position "umbrochen" wird, wenn sie über das Ende oder den Anfang des Bereichs hinaus erhöht oder dekrementiert wird.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

