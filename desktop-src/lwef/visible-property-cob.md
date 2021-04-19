---
title: Visible-Eigenschaft (Character-Objekt)
description: Visible-Eigenschaft
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a994fd59e5eaaebcaabbd9257b860fa4e27a09b4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106339531"
---
# <a name="visible-property-characters-object"></a>Visible-Eigenschaft (Character-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen booleschen Wert zurück, der angibt, ob das Zeichen sichtbar ist.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*Agent ***. Zeichen (**"* Merkmal-ID *" * *). Sichtbar**



| Wert | BESCHREIBUNG                            |
|-------|----------------------------------------|
| True  | Das Zeichen wird angezeigt.            |
| False | Das Zeichen ist ausgeblendet (nicht sichtbar). |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt an, ob der Rahmen des Zeichens angezeigt wird. Es bedeutet nicht unbedingt, dass ein Bild auf dem Bildschirm vorhanden ist. Diese Eigenschaft gibt z. b. **true** zurück, auch wenn das Zeichen vom sichtbaren Anzeigebereich positioniert ist oder wenn der aktuelle Zeichen Rahmen keine Bilder enthält. Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens.

Diese Eigenschaft ist schreibgeschützt. Um ein Zeichen sichtbar oder ausgeblendet zu machen, verwenden Sie die Methoden zum [**anzeigen**](show-method.md) oder [**Ausblenden**](https://www.bing.com/search?q=**Hide**) .

 

 




