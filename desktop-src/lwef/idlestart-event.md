---
title: IdleStart-Ereignis
description: IdleStart-Ereignis
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81458d4c88bc5db4ae4231ecb4ca47f456700917f42d6ccdfe5a6013bc288849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716050"
---
# <a name="idlestart-event"></a>IdleStart-Ereignis

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn der Server ein Zeichen in den **Idling-Zustand** setzt.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Sub-Agent** \_ IdleStart* *  **(ByVal** *CharacterID).)**



| Teil          | Beschreibung                                         |
|---------------|-----------------------------------------------------|
| *CharacterID* | Gibt die ID des Idlingzeichens als Zeichenfolge zurück. |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Der Server sendet dieses Ereignis an alle Clients des Zeichens.

### <a name="see-also"></a>Weitere Informationen

[**IdleComplete-Ereignis**](idlecomplete-event.md)


 

 




