---
title: Name-Eigenschaft (Character-Objekt)
description: Name-Eigenschaft
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e7b4a8872952cce0ae68445ec22a5599891674
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474838"
---
# <a name="name-property-characters-object"></a>Name-Eigenschaft (Character-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt eine Zeichenfolge zurück, die den Standardnamen des angegebenen Zeichens angibt, oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("**_Merkmal-ID_*_"). Namens_ *  \[  =  *Zeichenfolge*\]



| Teil     | BESCHREIBUNG                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| *string* | Ein Zeichen folgen Wert, der dem Namen des Zeichens entspricht (in der aktuellen Spracheinstellung). |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der **Name** eines Zeichens hängt möglicherweise von der [**LanguageID**](languageid-property.md) -Einstellung des Zeichens ab. Der Name eines Zeichens in einer Sprache kann anders sein oder andere Zeichen als in einem anderen verwenden. Der Standard **Name** des Zeichens für eine bestimmte Sprache wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.

Vermeiden Sie das Umbenennen eines Zeichens, insbesondere dann, wenn es in einem Szenario verwendet wird, in dem andere Client Anwendungen dasselbe Zeichen verwenden können. Außerdem verwendet der-Agent den Zeichen **Namen** , um automatisch Befehle zum Ausblenden und zeigen des Zeichens zu erstellen.

 

 




