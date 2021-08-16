---
title: Caption-Eigenschaft (Commands-Auflistungsobjekt)
description: Erfahren Sie mehr über die Caption-Eigenschaft des Command Collection-Objekts. Microsoft Agent ist ab 7 Windows veraltet.
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3467543de127bf0d9e898273f68d4cb921b7ab88ef52e965d73be4c1b465786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976700"
---
# <a name="caption-property-commands-collection-object"></a>Caption-Eigenschaft (Commands-Auflistungsobjekt)

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Bestimmt den Text, der für ein [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) im Popupmenü des Zeichens angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_")._ * [Commands.Caption-Zeichenfolge](caption-property.md) \[  =  \]



| Teil     | BESCHREIBUNG                                                              |
|----------|--------------------------------------------------------------------------|
| *string* | Ein Zeichenfolgenausdruck, der den als Beschriftung angezeigten Text auswertet. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das Festlegen der [**Caption-Eigenschaft**](caption-property.md) für Ihre [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) definiert, wie sie im Popupmenü des Zeichens angezeigt wird, wenn die [**Visible-Eigenschaft**](visible-property.md) auf True festgelegt ist und Ihre Anwendung nicht der eingabeaktive Client ist. Um einen Zugriffsschlüssel (unlined mnemonic) für Die Beschriftung **anzugeben,** schließen Sie ein ampersand-Zeichen (&) vor diesem Zeichen ein.

Wenn Sie Befehle für eine [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) definieren, die über eine [**Beschriftung**](caption-property.md)verfügt, definieren Sie in der Regel auch eine **Beschriftung** für die zugeordnete **Commands-Sammlung.**

 

 
