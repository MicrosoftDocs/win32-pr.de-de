---
title: Name-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Name-Eigenschaft des Characters-Objekts. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7365550d5d4d4071cf4292e505f16e7047628cf1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989325"
---
# <a name="name-property-characters-object"></a>Name-Eigenschaft (Characters-Objekt)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt eine Zeichenfolge zurück, die den Standardnamen des angegebenen Zeichens angibt, oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Namenszeichenfolge_ *  \[  =  \]



| Teil     | Beschreibung                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| *string* | Ein Zeichenfolgenwert, der dem Namen des Zeichens (in der aktuellen Spracheinstellung) entspricht. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Name eines **Zeichens** kann von der [**LanguageID-Einstellung**](languageid-property.md) des Zeichens abhängen. Der Name eines Zeichens in einer Sprache kann sich unterscheiden oder andere Zeichen als in einer anderen verwenden. Der Standardname des **Zeichens für** eine bestimmte Sprache wird definiert, wenn das Zeichen mit dem Microsoft Agent-Zeichen-Editor kompiliert wird.

Vermeiden Sie das Umbenennen eines Zeichens, insbesondere wenn es in einem Szenario verwendet wird, in dem andere Clientanwendungen dasselbe Zeichen verwenden können. Außerdem verwendet der -Agent  den Namen des Zeichens, um automatisch Befehle zum Ausblenden und Anzeigen des Zeichens zu erstellen.

 

 




