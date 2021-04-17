---
title: Eigenschaft "Vertrauen"
description: Eigenschaft "Vertrauen"
ms.assetid: 28a57970-4649-4a9a-9fb2-bf3f0b2f54ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa004e5690c534b7467c293d26cdf60f327dcfb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390178"
---
# <a name="confidence-property"></a>Eigenschaft "Vertrauen"

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob das **Vertrauen** des Clients in der Abhör Info angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID ***"). Befehle ("*** Name ***")**. * * Vertrauens* *  \[  =  *Nummer*\]



| Teil     | BESCHREIBUNG                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| *Number* | Ein numerischer Ausdruck, der eine lange ganze Zahl ergibt, die den Vertrauens Wert für den [**Befehl**](/windows/desktop/lwef/the-command-object)identifiziert. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn der zurückgegebene Vertrauens Wert der besten Entsprechung (User Input. Confidence) nicht den Wert überschreitet, den Sie für die Eigenschaft **Vertrauen** festgelegt haben, wird der in [**conficetext**](confidencetext-property.md) angegebene Text in der lausch Info angezeigt.

 

 