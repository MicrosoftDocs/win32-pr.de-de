---
title: Description-Eigenschaft (Features der Legacy-Windows-Umgebung)
description: Description-Eigenschaft
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4fb60b20a57f56a914c7e44ced957d91bf7085
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039940"
---
# <a name="description-property-legacy-windows-environment-features"></a>Description-Eigenschaft (Features der Legacy-Windows-Umgebung)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt eine Zeichenfolge zurück, die die Beschreibung für das angegebene Zeichen angibt, oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent*. **Zeichen ("**_Merkmal-ID_*_"). Description_* - \[  =  *Zeichenfolge*\]



| Teil     | BESCHREIBUNG                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| *string* | Ein Zeichen folgen Wert, der der Beschreibung des Zeichens entspricht (in der aktuellen Spracheinstellung). |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Beschreibung** eines Zeichens hängt möglicherweise von der **LanguageID** -Einstellung des Zeichens ab. Der Name eines Zeichens in einer Sprache kann anders sein oder andere Zeichen als in einem anderen verwenden. Die Standard **Beschreibung** des Zeichens für eine bestimmte Sprache wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.

> [!Note]  
> Die **Description** -Eigenschaften Einstellung ist optional und kann nicht für alle Zeichen angegeben werden.

 

 

 




