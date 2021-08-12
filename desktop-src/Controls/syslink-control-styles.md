---
title: SysLink-Steuerelementstile (CommCtrl.h)
description: Beim Erstellen von SysLink-Steuerelementen werden die folgenden Stilkonstanten verwendet.
ms.assetid: e9a8c99b-86c4-4385-ae20-b2b78a07b491
topic_type:
- apiref
api_name:
- LWS_TRANSPARENT
- LWS_IGNORERETURN
- LWS_NOPREFIX
- LWS_USEVISUALSTYLE
- LWS_USECUSTOMTEXT
- LWS_RIGHT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3707a4e7b59811a99cb23ca4ebdbfc8bc2d285c2e8780502241beebb2f7485d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670547"
---
# <a name="syslink-control-styles"></a>SysLink-Steuerelementstile

Beim Erstellen von SysLink-Steuerelementen werden die folgenden Stilkonstanten verwendet.



| Konstante                                                                                                                                                                        | Beschreibung                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LWS_TRANSPARENT"></span><span id="lws_transparent"></span><dl> <dt>**LWS \_ TRANSPARENT**</dt> </dl>             | Der Hintergrundmischungsmodus ist transparent. <br/>                                                                                                                       |
| <span id="LWS_IGNORERETURN_"></span><span id="lws_ignorereturn_"></span><dl> <dt>**LWS \_ IGNORERETURN**</dt> </dl>       | Wenn der Link den Tastaturfokus besitzt und der Benutzer die EINGABETASTE drückt, wird die Tastatureingabe vom Steuerelement ignoriert und an das Hostdialogfeld übergeben.<br/>                        |
| <span id="LWS_NOPREFIX"></span><span id="lws_noprefix"></span><dl> <dt>**LWS \_ NOPREFIX**</dt> </dl>                      | **Windows Vista**. Wenn der Text ein ampersand enthält, wird er als Literalzeichen und nicht als Präfix für eine Tastenkombination behandelt.<br/>                           |
| <span id="LWS_USEVISUALSTYLE_"></span><span id="lws_usevisualstyle_"></span><dl> <dt>**LWS \_ USEVISUALSTYLE**</dt> </dl> | **Windows Vista**. Der Link wird im aktuellen visuellen Stil angezeigt.<br/>                                                                                          |
| <span id="LWS_USECUSTOMTEXT"></span><span id="lws_usecustomtext"></span><dl> <dt>**LWS \_ USECUSTOMTEXT**</dt> </dl>       | **Windows Vista**. Beim Zeichnen des Steuerelements wird eine [ \_ NM CUSTOMTEXT-Benachrichtigung](nm-customtext.md) gesendet, damit die Anwendung Text dynamisch bereitstellen kann.<br/> |
| <span id="LWS_RIGHT"></span><span id="lws_right"></span><dl> <dt>**LWS \_ RIGHT**</dt> </dl>                               | **Windows Vista**. Der Text ist rechtsverrechtigent.<br/>                                                                                                                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





