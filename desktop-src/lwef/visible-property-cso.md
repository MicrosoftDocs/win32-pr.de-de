---
title: Visible-Eigenschaft (Commands-Objekt)
description: Erfahren Sie mehr über die Visible-Eigenschaft des Commands-Objekts, die bestimmt, ob die Beschriftung Ihrer Commands-Sammlung im Popupmenü des Zeichens angezeigt wird.
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ea780ed5f19dbe732b18de741f9d7ee376df67
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396255"
---
# <a name="visible-property-commands-object"></a>Visible-Eigenschaft (Commands-Objekt)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen Wert zurück, der bestimmt, ob die Beschriftung Ihrer [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) im Popupmenü des Zeichens angezeigt wird, oder legt diesen fest.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Commands.Visible* *  \[  =  *boolean*\]



| Teil      | Beschreibung                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der an gibt, ob das [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) im Popupmenü des Zeichens angezeigt wird. <br/> **True** Die Beschriftung wird angezeigt.<br/> **False** Die Beschriftung wird nicht angezeigt.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Damit die Beschriftung im Popupmenü des Zeichens angezeigt wird, wenn Ihre Anwendung nicht der eingabeaktive Client ist, muss diese Eigenschaft auf **True** und die [**Caption-Eigenschaft**](caption-property.md) für Ihre Commands-Sammlung festgelegt werden. Darüber hinaus muss diese Eigenschaft auf **True** festgelegt werden, damit Befehle in Ihrer Sammlung im Popupmenü angezeigt werden, wenn Ihre Anwendung eingabeaktiv ist.

 

