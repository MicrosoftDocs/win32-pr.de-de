---
title: Navigationskonstanten (Oleacc.h)
description: In diesem Thema werden die in oleacc.h definierten konstanten Werte beschrieben, die die räumliche Richtung (nach oben, unten, links und rechts) oder die logische Richtung (erstes untergeordnetes Element, letztes, nächstes und vorheriges Element) angeben, die beobachtet wird, wenn Clients IAccessible accNavigate verwenden, um von einem Benutzeroberflächenelement zu einem anderen innerhalb desselben Containers zu navigieren.
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
ms.openlocfilehash: b3e5c3a39c1b628ea03d1e036265ba7787e15bb70ce550e06b43b8efcd02c14a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998170"
---
# <a name="navigation-constants"></a>Navigationskonstanten

In diesem Thema werden die in oleacc.h definierten konstanten Werte beschrieben, die die *räumliche* Richtung (nach oben, unten, links und rechts) oder *die logische* Richtung (erstes untergeordnetes Element, letztes, nächstes und vorheriges Element) angeben, die beobachtet wird, wenn Clients [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) verwenden, um innerhalb desselben Containers von einem Benutzeroberflächenelement zu einem anderen zu navigieren. Weitere Informationen finden Sie unter Eigenschaften und Methoden der [Objektnavigation.](object-navigation-properties-and-methods.md)

Die Microsoft Active Accessibility Navigationskonstanten sind wie folgt:



| Konstante                                                                                                                                                                  | Beschreibung                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <dt>**NAVDIR \_ DOWN**</dt> </dl>                   | Navigieren Sie zu dem nebengeordneten Objekt, das sich unterhalb des Startobjekts befindet.<br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <dt>**NAVDIR \_ FIRSTCHILD**</dt> </dl> | Navigieren Sie zum ersten untergeordneten Element dieses Objekts. Wenn dieses Flag verwendet wird, muss der **lVal-Member** des *varStart-Parameters* CHILDID \_ SELF sein.<br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <dt>**NAVDIR \_ LASTCHILD**</dt> </dl>    | Navigieren Sie zum letzten untergeordneten Element dieses Objekts. Bei Verwendung dieses Flags muss der **lVal-Member** des *varStart-Parameters* CHILDID \_ SELF sein.<br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <dt>**NAVDIR \_ LEFT**</dt> </dl>                   | Navigieren Sie zu dem nebengeordneten Objekt, das sich links vom Startobjekt befindet.<br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <dt>**NAVDIR \_ NEXT**</dt> </dl>                   | Navigieren Sie zum nächsten logischen Objekt. im Allgemeinen handelt es sich um ein gleichgeordnetes Objekt des Startobjekts.<br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <dt>**NAVDIR \_ PREVIOUS**</dt> </dl>       | Navigieren Sie zum vorherigen logischen Objekt. im Allgemeinen handelt es sich um ein gleichgeordnetes Objekt des Startobjekts.<br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <dt>**NAVDIR \_ RIGHT**</dt> </dl>                | Navigieren Sie zu dem nebengeordneten Objekt, das sich rechts neben dem Startobjekt befindet.<br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <dt>**NAVDIR \_ UP**</dt> </dl>                         | Navigieren Sie zu dem nebengeordneten Objekt, das sich oberhalb des Startobjekts befindet.<br/>                                                                  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Oleacc.h</dt> </dl> |



 

 





