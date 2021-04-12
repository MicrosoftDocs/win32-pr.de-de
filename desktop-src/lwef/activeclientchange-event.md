---
title: Activeclientchange-Ereignis
description: Activeclientchange-Ereignis
ms.assetid: 617b40e6-cafb-463e-8b36-2a12c468d3ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8137edd559d934fd1a478350cd1185885c7dc148
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206754"
---
# <a name="activeclientchange-event"></a>Activeclientchange-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt auf, wenn sich der aktive Client des Zeichens ändert.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Unter** geordneter *Agent.* Activeclientchange (ByVal- *Kenn Zeichnerkennung*, ByVal *aktiv* **)**



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Merkmal-ID* | Gibt die ID des Zeichens zurück, für das das Ereignis aufgetreten ist.                                                                                                                                                                                                      |
| *Aktiv*      | Ein boolescher Wert, der angibt, ob der Client aktiv oder nicht aktiv geworden ist. **True** Die Client Anwendung wurde zum aktiven Client des Zeichens. <br/> **False** Die Client Anwendung ist nicht mehr der aktive Client des Zeichens.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Wenn mehrere Client Anwendungen dasselbe Zeichen gemeinsam verwenden, empfängt der aktive Client des Zeichens Maus Eingaben (z. b. Click-oder Drag-Ereignisse der Microsoft-agentsteuerung). Wenn mehrere Zeichen angezeigt werden, empfängt der aktive Client des obersten Zeichens (auch als Input-Active Client bezeichnet) [Befehls](command-event.md) Ereignisse.

Wenn sich der aktive Client eines Zeichens ändert, übergibt dieses Ereignis die ID dieses Zeichens und **true** , wenn die Anwendung zum aktiven Client des Zeichens geworden ist, oder **false** , wenn es nicht mehr der aktive Client des Zeichens ist.

Eine Client Anwendung empfängt dieses Ereignis möglicherweise, wenn der Benutzer den Eintrag einer Client Anwendung im Popupmenü des Zeichens oder per Sprachbefehl auswählt, wenn die Client Anwendung ihren aktiven Status ändert oder wenn eine andere Client Anwendung die Verbindung mit dem-Agent beendet. Der-Agent sendet dieses Ereignis nur an die Client Anwendungen, die direkt betroffen sind. , die entweder zum aktiven Client werden oder den aktiven Client beendet.

### <a name="see-also"></a>Weitere Informationen

[* * * * Activateinput * * Ereignis * *](activateinput-event.md), [* * * * aktiv * * Eigenschaft * *](active-property.md), * * * * [deactivateinput * * Ereignis * *](deactivateinput-event.md), [* * * * aktivieren * * Methode * *](activate-method.md)


 

 





