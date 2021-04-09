---
title: Ereignis verschieben
description: Ereignis verschieben
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31facb1d57b807fb0322783a291b77ef5a7c1487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856208"
---
# <a name="move-event"></a>Ereignis verschieben

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn ein Zeichen verschoben wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub-** *Agent*- \_ **Verschiebung (ByVal** - *Kenn zeichenkennung*, **ByVal** *X*, **ByVal** *Y*, **ByVal** - *Ursache * * *)**



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Merkmal-ID* | Gibt die ID des Zeichens zurück, das verschoben wurde.                                                                                                                                                                                                                                                                                                   |
| *X*           | Gibt die x-Koordinate (in Pixel) des oberen Rands der neuen Position des Zeichen Rahmens als Ganzzahl zurück.                                                                                                                                                                                                                                         |
| *J*           | Gibt die y-Koordinate (in Pixel) des linken Rands der neuen Position des Zeichen Rahmens als Ganzzahl zurück.                                                                                                                                                                                                                                        |
| *Ursache*       | Gibt einen Wert zurück, der angibt, wodurch das Zeichen verschoben wurde. 1 der Benutzer hat das Zeichen gezogen.<br/> 2 Ihre Client Anwendung hat das Zeichen verschoben.<br/> 3 eine andere Client Anwendung hat das Zeichen verschoben.<br/> 4 der Agent-Server hat das Zeichen verschoben, um es nach einer Änderung der Bildschirmauflösung auf dem Bildschirm aufzubewahren.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Dieses Ereignis tritt auf, wenn der Benutzer oder eine Anwendung die Position des Zeichens ändert. Die Koordinaten sind in der oberen linken Ecke des Bildschirms relevant. Dieses Ereignis wird nur an die Clients des Zeichens gesendet (Anwendungen, die das Zeichen geladen haben).

**Siehe auch**

[**Eigenschaft "muvecause**](movecause-property.md)", [ **Größen Ereignis**](size-event.md)

 

 





