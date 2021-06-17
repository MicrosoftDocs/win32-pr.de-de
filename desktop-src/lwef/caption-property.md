---
title: Caption-Eigenschaft (Befehlsobjekt)
description: Erfahren Sie mehr über die Caption-Eigenschaft des Command-Objekts. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0eb41def3b183fe4185b9c66a9ca5cd172372fb
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262552"
---
# <a name="caption-property-command-object"></a>Caption-Eigenschaft (Befehlsobjekt)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Bestimmt den Text, der für einen [**Befehl im**](/windows/desktop/lwef/the-command-object) Popupmenü des angegebenen Zeichens angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Commands("_*_name_*_")._ *  \[  =  *Beschriftungszeichenfolge*\]



| Teil     | Beschreibung                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| *string* | Ein Zeichenfolgenausdruck, der den Text auswertet, der als Beschriftung für den Befehl **angezeigt wird.** |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um einen Zugriffsschlüssel (unlined mnemonic) für Die Beschriftung **anzugeben,** schließen Sie vor diesem Zeichen ein ampersand-Zeichen (&) ein.

Wenn Sie keine **VoiceCaption** für Ihren Befehl definieren, wird Ihre **Caption-Einstellung** verwendet.

 

 
