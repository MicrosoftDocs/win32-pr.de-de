---
title: Visible-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Visible-Eigenschaft des Characters-Objekts, das einen booleschen Wert zurückgibt, der angibt, ob das Zeichen sichtbar ist.
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7358cd87a7fb3232b22cef33cbee5f2609708875
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396305"
---
# <a name="visible-property-characters-object"></a>Visible-Eigenschaft (Characters-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen booleschen Wert zurück, der angibt, ob das Zeichen sichtbar ist.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Sichtbar**



| Wert | Beschreibung                            |
|-------|----------------------------------------|
| True  | Das Zeichen wird angezeigt.            |
| Falsch | Das Zeichen ist ausgeblendet (nicht sichtbar). |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt an, ob der Rahmen des Zeichens angezeigt wird. Dies bedeutet nicht unbedingt, dass ein Bild auf dem Bildschirm vorhanden ist. Diese Eigenschaft gibt beispielsweise **True** zurück, auch wenn das Zeichen außerhalb des sichtbaren Anzeigebereichs positioniert ist oder wenn der aktuelle Zeichenrahmen keine Bilder enthält. Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens.

Diese Eigenschaft ist schreibgeschützt. Um ein Zeichen sichtbar oder ausgeblendet zu machen, verwenden Sie die Methoden [**Anzeigen**](show-method.md) oder [**Ausblenden.**](https://www.bing.com/search?q=**Hide**)

 

 




