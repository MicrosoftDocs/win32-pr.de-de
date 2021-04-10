---
title: Größen Ereignis
description: Größen Ereignis
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a896d2dcbf8b925c0ca13fa429f6dfd95bc21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855983"
---
# <a name="size-event"></a>Größen Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn die Größe eines Zeichens geändert wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub** - *Agent*- \_ **Größe (ByVal** - *Kenn zeichenkennung*, **ByVal** - *Breite*, **ByVal** - *Höhe*)



| Teil          | BESCHREIBUNG                                                         |
|---------------|---------------------------------------------------------------------|
| *Merkmal-ID* | Gibt die ID des Zeichens zurück, das verschoben wurde.                         |
| *Width*       | Gibt die neue Breite des Zeichen Rahmens (in Pixel) als ganze Zahl zurück.  |
| *Height*      | Gibt die neue Höhe des Zeichen Rahmens (in Pixel) als ganze Zahl zurück. |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Dieses Ereignis tritt auf, wenn eine Anwendung die Größe eines Zeichens ändert. Dieses Ereignis wird nur an die Clients des Zeichens gesendet (Anwendungen, die das Zeichen geladen haben).

### <a name="see-also"></a>Weitere Informationen

[**Ereignis verschieben**](move-event.md)


 

 




