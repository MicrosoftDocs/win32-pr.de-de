---
title: Caption-Eigenschaft (Command-Objekt)
description: Erfahren Sie mehr über die Caption-Eigenschaft des Command-Objekts. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be282591a6ed59993239bfd37baa639c4c2572ba54db6d1e46118ed98e317fda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726160"
---
# <a name="caption-property-command-object"></a>Caption-Eigenschaft (Command-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Bestimmt den Text, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object) im Popupmenü des angegebenen Zeichens angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Commands("_*_name_*_"). Beschriftungszeichenfolge_ *  \[  =  \]



| Teil     | Beschreibung                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| *string* | Ein Zeichenfolgenausdruck, der den Text ergibt, der als Beschriftung für den **Befehl** angezeigt wird. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um einen Zugriffsschlüssel (unlineiertes mnemonic) für Ihre **Beschriftung** anzugeben, schließen Sie ein ampersand (&)-Zeichen vor dieses Zeichen ein.

Wenn Sie keine **VoiceCaption** für Ihren Befehl definieren, wird Ihre **Einstellung Caption** verwendet.

 

 
