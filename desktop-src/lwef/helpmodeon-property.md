---
title: HelpModeOn-Eigenschaft
description: HelpModeOn-Eigenschaft
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 489de1893e96bf2d4cc38ef9e788a726db8b9fd4dfbdc9ae3cd1b60f9bc02f91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962740"
---
# <a name="helpmodeon-property"></a>HelpModeOn-Eigenschaft

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob der kontextsensitive Hilfemodus für das Zeichen aktiviert ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). HelpModeOn_ *  \[  =  *boolean*\]



| Teil      | BESCHREIBUNG                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der an gibt, ob der kontextsensitive Hilfemodus aktiviert ist. **True** Der Hilfemodus ist aktiviert. <br/> **Der Hilfemodus** FALSE (Standard) ist deaktiviert.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie diese Eigenschaft auf **True** festlegen, ändert sich der Mauszeiger in das kontextsensitive Hilfebild, wenn er über das Zeichen oder über das Popupmenü für das Zeichen verschoben wird. Wenn der Benutzer auf das Zeichen klickt oder das Zeichen zieht oder auf ein Element im Popupmenü des Zeichens klickt, löst der Server das [**HelpComplete-Ereignis**](helpcomplete-event.md) aus und beendet den Hilfemodus.

Im Hilfemodus sendet der Server [](click-event.md)die Click-, [**DragStart-,**](dragstart-event.md) [**DragComplete-**](dragcomplete-event.md)und [**Command-Ereignisse**](command-event.md) nur, wenn Sie die [**AutoPopupMenu-Eigenschaft**](autopopupmenu-property.md) auf **True festlegen.** In diesem Fall sendet der Server das **Click-Ereignis** (beendet den Hilfemodus nicht), sondern nur für die rechte Maustaste, damit Sie das Popupmenü anzeigen können.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**HelpComplete-Ereignis**](helpcomplete-event.md)


 

 





