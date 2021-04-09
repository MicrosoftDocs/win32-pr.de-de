---
title: Debug-Ereignis
description: Debug-Ereignis
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2fe1ff13b599fe5fbcf2dac22e548a0432f415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947838"
---
# <a name="deactivateinput-event"></a>Debug-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt auf, wenn ein Client nicht mehr Eingabe aktiv wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub** - *Agent * * \_ ** Geräte- *  ID **(ByVal** - *Merkmal-ID * * *)**



| Teil          | BESCHREIBUNG                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *Merkmal-ID* | Gibt die ID des Zeichens zurück, das dazu führt, dass der Client nicht mehr Eingabe aktiv wird. |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Ein nicht-Eingabe-aktiv-Client empfängt keine Maus-oder sprach Ereignisse mehr vom Server (es sei denn, er wird erneut zur Eingabe aktiv). Der Server sendet dieses Ereignis nur an den Client, der als nicht Eingabe aktiv wird.

Dieses Ereignis tritt auf, wenn die Client Anwendung aktiv ist und der Benutzer die Beschriftung eines anderen Clients im Popupmenü eines Zeichens oder im Fenster "Sprachbefehle" auswählt oder die [**Aktivierungs**](activate-method.md) Methode aufruft und den Parameter " **State** " auf 0 (null) festgelegt hat. Dies kann auch vorkommen, wenn der Benutzer den Namen eines anderen Zeichens durch Klicken oder sprechen auswählt. Sie erhalten dieses Ereignis auch dann, wenn das Zeichen ausgeblendet ist oder ein anderes Zeichen sichtbar wird.

### <a name="see-also"></a>Weitere Informationen

[**Activateinput-Ereignis**](activateinput-event.md)


 

 




