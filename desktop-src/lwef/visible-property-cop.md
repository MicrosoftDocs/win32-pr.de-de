---
title: Visible-Eigenschaft (Befehls Objekt)
description: Visible-Eigenschaft
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feaa6603812bf0938e6639021eb0f8660382af37
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106342391"
---
# <a name="visible-property-command-object"></a>Visible-Eigenschaft (Befehls Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob der [**Befehl**](/windows/desktop/lwef/the-command-object) im Popupmenü des Zeichens sichtbar ist.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*Agent ***. Zeichen (**"* Merkmal-ID *"**). Befehle (**"* Name *" * *). Sichtbarer* *  \[  =  *boolescher* Wert\]



| Teil      | BESCHREIBUNG                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der angibt, ob die Beschriftung des [**Befehls**](/windows/desktop/lwef/the-command-object)im Popupmenü des Zeichens angezeigt wird.<br/> **True** (Standard) die Beschriftung wird angezeigt.<br/> **False** Die Beschriftung wird nicht angezeigt.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Legen Sie diese Eigenschaft auf " **false** " fest, wenn Sie Spracheingaben für Ihre eigenen Schnittstellen einschließen möchten, ohne dass Sie im Popup Menü für das Zeichen angezeigt werden. Wenn Sie die [**Caption**](caption-property.md) -Eigenschaft eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts auf die leere Zeichenfolge ("") festlegen, wird der Beschriftungs Text nicht im Popup Menü (z. b. als Leerzeile) angezeigt, unabhängig von dessen [**sichtbarer**](visible-property.md) Eigenschaften Einstellung.

Die [**Visible**](visible-property.md) -Eigenschaften Einstellung der Auflistung der übergeordneten [**Befehle**](/windows/desktop/lwef/the-commands-collection-object) eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts wirkt sich nicht auf die **sichtbare** Eigenschafts Einstellung des **Befehls** aus.

 

