---
title: Size-Ereignis
description: Size-Ereignis
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146763c649ab22c59a8367e3135ee0ea277c8ae4c8e4bc58588cd70c0b5ec1c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961020"
---
# <a name="size-event"></a>Size-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn sich die Größe eines Zeichens ändert.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Größe** des *Sub-Agents* \_ **(ByVal** *CharacterID*, **ByVal** *Width*, **ByVal** *Height*)



| Teil          | BESCHREIBUNG                                                         |
|---------------|---------------------------------------------------------------------|
| *CharacterID* | Gibt die ID des verschobenen Zeichens zurück.                         |
| *Width*       | Gibt die neue Breite des Zeichenrahmens (in Pixel) als ganze Zahl zurück.  |
| *Height*      | Gibt die neue Höhe des Zeichenrahmens (in Pixel) als ganze Zahl zurück. |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Dieses Ereignis tritt auf, wenn eine Anwendung die Größe eines Zeichens ändert. Dieses Ereignis wird nur an die Clients des Zeichens gesendet (Anwendungen, die das Zeichen geladen haben).

### <a name="see-also"></a>Weitere Informationen

[**Move-Ereignis**](move-event.md)


 

 




