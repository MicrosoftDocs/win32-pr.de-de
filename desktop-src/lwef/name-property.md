---
title: Name-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Name-Eigenschaft des Characters-Objekts. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08509d5d2a349c56548259db4846203da6f632ff76c86309db87e6aa90583a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608650"
---
# <a name="name-property-characters-object"></a>Name-Eigenschaft (Characters-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt eine Zeichenfolge zurück, die den Standardnamen des angegebenen Zeichens angibt, oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_")._ *  \[  =  *Namenszeichenfolge*\]



| Teil     | Beschreibung                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| *string* | Ein Zeichenfolgenwert, der dem Namen des Zeichens entspricht (in der aktuellen Spracheinstellung). |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der **Name** eines Zeichens kann von der [**LanguageID-Einstellung**](languageid-property.md) des Zeichens abhängen. Der Name eines Zeichens in einer Sprache kann anders sein oder andere Zeichen als in einer anderen Sprache verwenden. Der **Standardname** des Zeichens für eine bestimmte Sprache wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.

Vermeiden Sie das Umbenennen eines Zeichens, insbesondere wenn es in einem Szenario verwendet wird, in dem andere Clientanwendungen das gleiche Zeichen verwenden können. Außerdem verwendet der -Agent den **Namen** des Zeichens, um automatisch Befehle zum Ausblenden und Anzeigen des Zeichens zu erstellen.

 

 




