---
title: Helpmudeon (Eigenschaft)
description: Helpmudeon (Eigenschaft)
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43662469c6461e92186a92daddb505b851f8740a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710925"
---
# <a name="helpmodeon-property"></a>Helpmudeon (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob der kontextabhängige Hilfe Modus für das Zeichen eingeschaltet ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. ***Zeichen ("*** Merkmal-ID * * *"). Helpmodeon* *  \[  =  *booleschen*\]



| Teil      | BESCHREIBUNG                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der angibt, ob der kontextabhängige Hilfe Modus auf ON festgelegt ist. **True** Der Hilfe Modus ist "on". <br/> **False** (Standard) der Hilfe Modus ist off.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Eigenschaft auf **true** festlegen, ändert sich der Mauszeiger in das kontextabhängige Hilfe Bild, wenn es über das Zeichen oder über das Popup Menü für das Zeichen verschoben wird. Wenn der Benutzer auf das Zeichen klickt oder zieht oder auf ein Element im Popupmenü des Zeichens klickt, löst der Server das [**helpcomplete**](helpcomplete-event.md) -Ereignis aus und beendet den Hilfe Modus.

Im Hilfe Modus sendet der Server die Ereignisse [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**dragcomplete**](dragcomplete-event.md)und [**Command**](command-event.md) nicht, es sei denn, Sie legen die Eigenschaft [**autopopupmenu**](autopopupmenu-property.md) auf **true** fest. In diesem Fall sendet der Server das **Click** -Ereignis (der Hilfe Modus wird nicht beendet), sondern nur für die Rechte Maustaste, damit Sie das Popup Menü anzeigen können.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Helpcomplete-Ereignis**](helpcomplete-event.md)


 

 





