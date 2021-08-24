---
title: BalloonShow-Ereignis
description: BalloonShow-Ereignis
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10aa8ab2c556fdf603a3972033a7440041fef6a45f828115c649a8a42810eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726140"
---
# <a name="balloonshow-event"></a>BalloonShow-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn die Wortsprechblase eines Zeichens angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**BalloonShow** des *Sub-Agents* \_  **(ByVal** *CharacterID))**



| Teil          | Beschreibung                                                       |
|---------------|-------------------------------------------------------------------|
| *CharacterID* | Gibt die ID des Zeichens zurück, das dem Wort balloon zugeordnet ist. |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Der Server sendet dieses Ereignis nur an die Clients des Zeichens (Anwendungen, die das Zeichen geladen haben), das den Wortsprechblasen verwendet.

### <a name="see-also"></a>Weitere Informationen

[**BalloonHide-Ereignis**](balloonhide-event.md)


 

 




