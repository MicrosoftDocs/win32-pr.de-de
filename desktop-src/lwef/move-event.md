---
title: Move-Ereignis
description: Move-Ereignis
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9938f79a0c23340c5ed34be52019afe5f9f3fa6caefb6920941cb17dc13c0fc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476348"
---
# <a name="move-event"></a>Move-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn ein Zeichen verschoben wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Move** des *Sub-Agents* \_ **(ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *Cause))**



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Gibt die ID des verschobenen Zeichens zurück.                                                                                                                                                                                                                                                                                                   |
| *X*           | Gibt die x-Koordinate (in Pixel) des oberen Rands der neuen Position des Zeichenrahmens als ganze Zahl zurück.                                                                                                                                                                                                                                         |
| *J*           | Gibt die y-Koordinate (in Pixel) des linken Rands der neuen Position des Zeichenrahmens als ganze Zahl zurück.                                                                                                                                                                                                                                        |
| *Ursache*       | Gibt einen Wert zurück, der angibt, wodurch das Zeichen verschoben wurde. 1 Der Benutzer hat das Zeichen gezogen.<br/> 2 Ihre Clientanwendung hat das Zeichen verschoben.<br/> 3 Das Zeichen wurde von einer anderen Clientanwendung verschoben.<br/> 4 Der Agent-Server hat das Zeichen verschoben, um es nach einer Bildschirmauflösungsänderung auf dem Bildschirm zu halten.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Dieses Ereignis tritt auf, wenn der Benutzer oder eine Anwendung die Position des Zeichens ändert. Koordinaten sind für die obere linke Ecke des Bildschirms relevant. Dieses Ereignis wird nur an die Clients des Zeichens gesendet (Anwendungen, die das Zeichen geladen haben).

**Siehe auch**

[**MoveCause-Eigenschaft,**](movecause-property.md) [ **Size-Ereignis**](size-event.md)

 

 





