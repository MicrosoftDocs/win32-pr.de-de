---
title: Caption-Eigenschaft (Commands Collection-Objekt)
description: Erfahren Sie mehr über die Caption-Eigenschaft des Command Collection-Objekts. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34ae7bd6da1fc6cc60f882cc231af5730a1077e
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262052"
---
# <a name="caption-property-commands-collection-object"></a>Caption-Eigenschaft (Commands Collection-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Bestimmt den Text, der für ein [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) im Popupmenü des Zeichens angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_")._ * [Commands.Caption-Zeichenfolge](caption-property.md) \[  =  \]



| Teil     | Beschreibung                                                              |
|----------|--------------------------------------------------------------------------|
| *string* | Ein Zeichenfolgenausdruck, der den als Beschriftung angezeigten Text ergibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Durch Festlegen der [**Caption-Eigenschaft**](caption-property.md) für Ihre [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) wird definiert, wie sie im Popupmenü des Zeichens angezeigt wird, wenn die [**Visible-Eigenschaft**](visible-property.md) auf True festgelegt ist und Ihre Anwendung nicht der eingabeaktive Client ist. Um einen Zugriffsschlüssel (unlineiertes mnemonic) für Die **Beschriftung** anzugeben, schließen Sie vor diesem Zeichen ein ampersand (&) Zeichen ein.

Wenn Sie Befehle für eine [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) mit einer [**Beschriftung**](caption-property.md)definieren, definieren Sie in der Regel auch eine **Beschriftung** für die zugehörige **Commands-Sammlung.**

 

 
