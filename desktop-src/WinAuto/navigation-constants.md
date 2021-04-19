---
title: Navigations Konstanten (Oleacc. h)
description: In diesem Thema werden die Konstanten Werte beschrieben, die in Oleacc. h definiert sind, die die räumliche Richtung (oben, unten, Links und rechts) oder die logische (erste untergeordnete, letzte, nächste und vorherige) Richtung angeben, die beobachtet wird, wenn Clients IAccessible accNavigate verwenden, um von einem Benutzeroberflächen Element zu einem anderen innerhalb desselben Containers zu navigieren.
ms.assetid: 5859a7a3-bcd3-443e-8ff0-4952f4639517
topic_type:
- apiref
api_name:
- NAVDIR_DOWN
- NAVDIR_FIRSTCHILD
- NAVDIR_LASTCHILD
- NAVDIR_LEFT
- NAVDIR_NEXT
- NAVDIR_PREVIOUS
- NAVDIR_RIGHT
- NAVDIR_UP
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de5f4eaa3fc7fb24583e49bdd14acb9633b2bd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352960"
---
# <a name="navigation-constants"></a>Navigations Konstanten

In diesem Thema werden die Konstanten Werte beschrieben, die in Oleacc. h definiert sind, die die *räumliche* Richtung (oben, unten, Links und rechts) oder die *logische* (erste untergeordnete, letzte, nächste und vorherige) Richtung angeben, die beobachtet wird, wenn Clients [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) verwenden, um innerhalb desselben Containers von einem Benutzeroberflächen Element zu einem anderen zu navigieren. Weitere Informationen finden Sie unter [Objekt Navigations Eigenschaften und-Methoden](object-navigation-properties-and-methods.md).

Die Microsoft Active Accessibility-Navigations Konstanten lauten wie folgt:



| Konstante                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <dt>**navDir \_ nach unten**</dt> </dl>                   | Navigieren Sie zu dem neben geordneten Objekt, das sich unterhalb des Start Objekts befindet.<br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <dt>**navDir, \_ FirstChild**</dt> </dl> | Navigieren Sie zum ersten untergeordneten Element dieses Objekts. Wenn dieses Flag verwendet wird, muss der **LVAL** -Member des *varstart* -Parameters "childID Self" lauten \_ .<br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <dt>**navDir \_ LastChild**</dt> </dl>    | Navigieren Sie zum letzten untergeordneten Element dieses Objekts. Wenn Sie dieses Flag verwenden, muss das **LVAL** -Element des *varstart* -Parameters "childID Self" lauten \_ .<br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <dt>**navDir \_ Links**</dt> </dl>                   | Navigieren Sie zu dem neben geordneten Objekt, das sich auf der linken Seite des Start Objekts befindet.<br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <dt>**nächste navDir \_**</dt> </dl>                   | Navigieren Sie zum nächsten logischen Objekt. im Allgemeinen ist es ein gleich geordnetes Element des Start Objekts.<br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <dt>**früher navDir \_**</dt> </dl>       | Navigieren Sie zum vorherigen logischen Objekt. im Allgemeinen ist es ein gleich geordnetes Element des Start Objekts.<br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <dt>**navDir \_ right**</dt> </dl>                | Navigieren Sie zu dem neben geordneten Objekt, das sich auf der rechten Seite des Start Objekts befindet.<br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <dt>**navDir nach \_ oben**</dt> </dl>                         | Navigieren Sie zu dem neben geordneten Objekt, das sich oberhalb des Anfangs Objekts befindet.<br/>                                                                  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Oleacc. h</dt> </dl> |



 

 





