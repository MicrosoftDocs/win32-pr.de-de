---
title: Description-Eigenschaft (Legacy Windows Umgebungsfeatures)
description: Description-Eigenschaft
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7ff293af98303fa0dab97aca76ed169123ea229c1fc70c156ef2c099472157
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751992"
---
# <a name="description-property-legacy-windows-environment-features"></a>Description-Eigenschaft (Legacy Windows Umgebungsfeatures)

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt eine Zeichenfolge zurück, die die Beschreibung für das angegebene Zeichen angibt, oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*-Agent.* **Characters("**_CharacterID_*_")._* \[  =  *Beschreibungszeichenfolge*\]



| Teil     | BESCHREIBUNG                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| *string* | Ein Zeichenfolgenwert, der der Beschreibung des Zeichens (in der aktuellen Spracheinstellung) entspricht. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Beschreibung eines **Zeichens** kann von der **LanguageID-Einstellung** des Zeichens abhängen. Der Name eines Zeichens in einer Sprache kann sich unterscheiden oder andere Zeichen als in einer anderen verwenden. Die Standardbeschreibung des Zeichens **für** eine bestimmte Sprache wird definiert, wenn das Zeichen mit dem Microsoft Agent-Zeichen-Editor kompiliert wird.

> [!Note]  
> Die **Eigenschaftseinstellung** Beschreibung ist optional und wird möglicherweise nicht für alle Zeichen angegeben.

 

 

 




