---
description: Die LaunchCondition-Tabelle wird von der LaunchConditions-Aktion verwendet. Es enthält eine Liste der Bedingungen, die alle für den Beginn der Installation erfüllt sein müssen.
ms.assetid: 6e550cc7-c479-417e-ab89-882d8fece4e1
title: LaunchCondition-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d67834f058575dde297454480040028ef9c5732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343307"
---
# <a name="launchcondition-table"></a>LaunchCondition-Tabelle

Die LaunchCondition-Tabelle wird von der [LaunchConditions-Aktion](launchconditions-action.md)verwendet. Es enthält eine Liste der Bedingungen, die alle für den Beginn der Installation erfüllt sein müssen.

Die LaunchCondition-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                       | Schlüssel | Nullwerte zulässig |
|-------------|----------------------------|-----|----------|
| Bedingung   | [Condition](condition.md) | J   | N        |
| BESCHREIBUNG | [Großformatige](formatted.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage
</dt> <dd>

Ausdruck, der als true ausgewertet werden muss, damit die Installation beginnt.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Lokalisier barer Text, der angezeigt wird, wenn die Bedingung fehlschlägt und die Installation beendet werden muss.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können die Reihenfolge, in der die Startbedingungen ausgewertet werden, nicht garantieren, indem Sie diese Tabelle erstellen. Wenn es erforderlich ist, die Reihenfolge zu steuern, in der die Bedingungen ausgewertet werden, sollten Sie hierfür benutzerdefinierte Aktionen vom Typ 19 benutzerdefinierte Aktionen in der Installation verwenden.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



