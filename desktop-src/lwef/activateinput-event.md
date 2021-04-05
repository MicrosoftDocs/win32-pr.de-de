---
title: Activateinput-Ereignis
description: Activateinput-Ereignis
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0b4fdf83256d58dd247dee85b639f5499f013e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037481"
---
# <a name="activateinput-event"></a>Activateinput-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt auf, wenn ein Client als Eingabe aktiv wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub** - *Agent* \_ activateinput **(ByVal** - *Merkmal-ID * * *)**



| Teil          | BESCHREIBUNG                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *Merkmal-ID* | Gibt die ID des Zeichens zurück, über das der Client als Eingabe aktiv wird. |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Der Input-Active-Client empfängt die vom Server bereitgestellten Maus-und Spracheingabe Ereignisse. Der Server sendet dieses Ereignis nur an den Client, der als Eingabe aktiv wird.

Dieses Ereignis kann auftreten, wenn der Benutzer zum [Befehls](the-command-object.md) Objekt wechselt, z. b. durch Auswählen des Befehls Objekt Eintrags im Befehlsfenster oder im Popup Menü eines Zeichens. Dies kann auch vorkommen, wenn der Benutzer ein Zeichen (durch Klicken oder benennen des Namens) auswählt, wenn ein Zeichen sichtbar wird und wenn das Zeichen einer anderen Client Anwendung ausgeblendet wird. Sie können auch die [Aktivierungsmethode](activate-method.md) (mit dem **Status** 2) aufgerufen werden, um explizit das Zeichen zu erstellen, was dazu führt, dass die Client Anwendung aktiv wird und dieses Ereignis auslöst. Dieses Ereignis tritt jedoch nicht auf, wenn Sie die Methode Methode aktivieren nur verwenden, um anzugeben, ob der Client der aktive Client des Zeichens ist.

### <a name="see-also"></a>Weitere Informationen

[**Deactivateinput** -Ereignis](deactivateinput-event.md), [Methode **aktivieren**](activate-method.md)


 

 




