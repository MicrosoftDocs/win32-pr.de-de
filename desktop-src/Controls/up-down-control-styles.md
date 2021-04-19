---
title: Up-Down Steuerelement Stile (kommctrl. h)
description: In diesem Abschnitt werden die Formate aufgelistet, die bei der Erstellung von auf-ab-Steuerelementen
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
ms.openlocfilehash: 9b27cd27123f4c1a071314fd20d1874e61b590d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359669"
---
# <a name="up-down-control-styles"></a>Up-Down Steuerelement Stile

In diesem Abschnitt werden die Formate aufgelistet, die bei der Erstellung von auf-ab-Steuerelementen



| Konstante                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UDS_ALIGNLEFT"></span><span id="uds_alignleft"></span><dl> <dt>**UDS \_ alignleft**</dt> </dl>       | Positioniert das auf-ab-Steuerelement neben dem linken Rand des Buddy-Fensters. Das Buddy-Fenster wird nach rechts verschoben, und seine Breite wird verringert, um die Breite des auf-ab-Steuer Elements anzupassen.<br/>                                                                                                                                                                                                   |
| <span id="UDS_ALIGNRIGHT"></span><span id="uds_alignright"></span><dl> <dt>**UDS- \_ AlignRight**</dt> </dl>    | Positioniert das auf-ab-Steuerelement neben dem rechten Rand des Buddy-Fensters. Die Breite des Buddy-Fensters wird verringert, um die Breite des auf-ab-Steuer Elements anzupassen.<br/>                                                                                                                                                                                                                          |
| <span id="UDS_ARROWKEYS"></span><span id="uds_arrowkeys"></span><dl> <dt>**UDS- \_ arrowkeys**</dt> </dl>       | Bewirkt, dass das auf-ab-Steuerelement die Position erhöht und dekretert, wenn die nach-oben-Taste und die nach-unten-Taste gedrückt werden.<br/>                                                                                                                                                                                                                                                                          |
| <span id="UDS_AUTOBUDDY"></span><span id="uds_autobuddy"></span><dl> <dt>**UDS- \_ autobuddy**</dt> </dl>       | Wählt automatisch das vorherige Fenster in der z-Reihenfolge als Buddy-Fenster des auf-ab-Steuer Elements aus.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="UDS_HORZ"></span><span id="uds_horz"></span><dl> <dt>**UDS- \_ Horz**</dt> </dl>                      | Bewirkt, dass die Pfeile des auf-ab-Steuer Elements auf die linke und die Rechte anstelle von nach oben und unten zeigen.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="UDS_HOTTRACK"></span><span id="uds_hottrack"></span><dl> <dt>**UDS- \_ HotTrack**</dt> </dl>          | Bewirkt, dass das-Steuerelement das Verhalten "Hot Tracking" aufweist. Das heißt, es hebt den Pfeil nach oben und den Pfeil nach unten auf dem Steuerelement hervor, wenn der Mauszeiger darüber übergeht. Dieser Stil erfordert Windows 98 oder Windows 2000. Wenn auf dem System Windows 95 oder Windows NT 4,0 ausgeführt wird, wird das Flag ignoriert. Um zu überprüfen, ob Hot Tracking aktiviert ist, aufrufen Sie [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/> |
| <span id="UDS_NOTHOUSANDS"></span><span id="uds_nothousands"></span><dl> <dt>**UDS ( \_ notausend)**</dt> </dl> | Fügt kein Tausender Trennzeichen zwischen allen drei Dezimalstellen ein. <br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="UDS_SETBUDDYINT"></span><span id="uds_setbuddyint"></span><dl> <dt>**UDS \_ setbuddyint**</dt> </dl> | Bewirkt, dass das auf-ab-Steuerelement den Text des Buddy-Fensters festlegt, wenn [**sich die Position \_**](/windows/desktop/winmsg/wm-settext) ändert. Der Text besteht aus der Position, die als Dezimal-oder hexadezimale Zeichenfolge formatiert ist.<br/>                                                                                                                                                             |
| <span id="UDS_WRAP"></span><span id="uds_wrap"></span><dl> <dt>**UDS- \_ Wrap**</dt> </dl>                      | Bewirkt, dass die Position "Wrap" ist, wenn Sie nach dem Ende oder dem Anfang des Bereichs erhöht oder dekrementiert wird.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

