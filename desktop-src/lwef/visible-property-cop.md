---
title: Visible-Eigenschaft (Befehlsobjekt)
description: Erfahren Sie mehr über die Visible-Eigenschaft des Command-Objekts, das zurückgibt oder festlegt, ob der Befehl im Popupmenü des Zeichens sichtbar ist.
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4efec1ad8a97d6412a560a81836273b93ebf2b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396245"
---
# <a name="visible-property-command-object"></a>Visible-Eigenschaft (Befehlsobjekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob der [**Befehl**](/windows/desktop/lwef/the-command-object) im Popupmenü des Zeichens angezeigt wird.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Commands(**"* name *"**). Sichtbarer* *  \[  =  *boolescher Wert*\]



| Teil      | Beschreibung                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der angibt, ob die Beschriftung des [**Befehls**](/windows/desktop/lwef/the-command-object)im Popupmenü des Zeichens angezeigt wird.<br/> **True** (Standard) Die Beschriftung wird angezeigt.<br/> **False** Die Beschriftung wird nicht angezeigt.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Legen Sie diese Eigenschaft auf **False** fest, wenn Sie Spracheingaben für Ihre eigenen Schnittstellen einschließen möchten, ohne dass sie im Popupmenü für das Zeichen angezeigt werden. Wenn Sie die [**Caption-Eigenschaft**](caption-property.md) eines [**Command-Objekts**](/windows/desktop/lwef/the-command-object) auf die leere Zeichenfolge ("") festlegen, wird der Beschriftungstext unabhängig von der [](visible-property.md) Visible-Eigenschaftseinstellung nicht im Popupmenü angezeigt (z. B. als leere Zeile).

Die [](visible-property.md) Visible-Eigenschafteneinstellung der [**übergeordneten Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) eines [**Command-Objekts**](/windows/desktop/lwef/the-command-object) wirkt sich nicht auf die **Visible-Eigenschafteneinstellung** des **Befehls** aus.

 

