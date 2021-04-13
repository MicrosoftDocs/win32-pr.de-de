---
title: Conficetext-Eigenschaft
description: Conficetext-Eigenschaft
ms.assetid: ff856af7-c5ad-4970-8778-b59a76c5e276
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb30b5ac481b6011d3575ab99dbc389f426b085d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390241"
---
# <a name="confidencetext-property"></a>Conficetext-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den **vertrauenden Text** des Clients zurück, der in der Abhör Info angezeigt wird, oder legt diesen fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*-Agent ***. Zeichen ("*** Merkmal-ID ***"). Befehle ("*** Name ***")**. **Vertrauvertrautext** \[  =  *Zeichenfolge*\]



| Teil     | BESCHREIBUNG                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| *string* | Ein Zeichen folgen Ausdruck, der den Text für den **vertrauentext** für den [**Befehl**](/windows/desktop/lwef/the-command-object)ergibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn der zurückgegebene Vertrauens Wert der besten Entsprechung (User Input. Confidence) die Einstellung " [**Vertrauen**](confidence-property.md) " nicht überschreitet, zeigt der Server den Text an, der in " **vertrauenstext** " in der Abhör info angegeben ist.

 

 