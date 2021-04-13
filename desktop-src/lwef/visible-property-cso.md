---
title: Visible-Eigenschaft (Commands-Objekt)
description: Visible-Eigenschaft
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaba059a375c23569195ddaea82e6d03cb943ec
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391452"
---
# <a name="visible-property-commands-object"></a>Visible-Eigenschaft (Commands-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen Wert zurück, der bestimmt, ob die Beschriftung der [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung im Popupmenü des Zeichens angezeigt wird, oder legt diesen fest.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*Agent ***. Zeichen (**"* Merkmal-ID *" * *). Commands. Visible* *  \[  =  *boolescher* Wert\]



| Teil      | BESCHREIBUNG                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der angibt, ob das [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Objekt im Popupmenü des Zeichens angezeigt wird. <br/> **True** Die Beschriftung wird angezeigt.<br/> **False** Die Beschriftung wird nicht angezeigt.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Damit die Beschriftung im Popupmenü des Zeichens angezeigt wird, wenn Ihre Anwendung nicht der Input-Active-Client ist, muss diese Eigenschaft auf **true** festgelegt werden, und die [**Caption**](caption-property.md) -Eigenschaft muss für die Commands-Auflistung festgelegt sein. Außerdem muss diese Eigenschaft auf **true** festgelegt werden, damit Befehle in ihrer Auflistung im Popup Menü angezeigt werden, wenn die Anwendung Eingabe aktiv ist.

 

