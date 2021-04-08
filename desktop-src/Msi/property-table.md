---
description: Die Eigenschaften Tabelle enthält die Eigenschaftsnamen und-Werte für alle definierten Eigenschaften in der Installation. Eigenschaften mit NULL-Werten sind nicht in der Tabelle vorhanden.
ms.assetid: 1f4215b2-dc71-4e6e-bc2e-3b43316806b9
title: Eigenschaften Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612ab63aa36de6cf91ec8176eefec84cef591c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756481"
---
# <a name="property-table"></a>Eigenschaften Tabelle

Die Eigenschaften Tabelle enthält die Eigenschaftsnamen und-Werte für alle definierten Eigenschaften in der Installation. Eigenschaften mit NULL-Werten sind nicht in der Tabelle vorhanden.

Die Eigenschaften Tabelle weist die folgenden Spalten auf.



| Spalte   | Typ                         | Schlüssel | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Eigenschaft | [Bezeichner](identifier.md) | J   | N        |
| Wert    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property
</dt> <dd>

Der Name einer Eigenschaft. Siehe [Eigenschaften](properties.md).

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Ein Lokalisier barer Zeichen folgen Wert für die-Eigenschaft. Dies darf niemals NULL oder eine leere Zeichenfolge sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass Sie die Eigenschafts Tabelle nicht verwenden können, um eine Eigenschaft auf den Wert einer anderen Eigenschaft festzulegen. Das Installationsprogramm führt keine Aktion für die Text Zeichenfolge aus, die in der Spalte Wert eingegeben wurde, bevor die Eigenschaft in der Eigenschafts Spalte Wenn firstproperty in die Eigenschafts Spalte und \[ secondproperty \] in der Spalte Wert eingegeben wird, wird der Wert von firstproperty auf die Text Zeichenfolge " \[ secondproperty \] " und nicht auf den Wert der secondproperty-Eigenschaft festgelegt. Dies ist erforderlich, um zu verhindern, dass Zirkel Verweise in der Eigenschaften Tabelle erstellt werden. Stattdessen können Sie eine Eigenschaft mit einem [benutzerdefinierten Aktionstyp 51](custom-action-type-51.md)auf einen anderen festlegen.

Beachten Sie, dass die Eigenschaft [**adminproperties**](adminproperties.md) verwendet werden kann, um die Werte in der Eigenschaften Tabelle während einer [administrativen Installation](administrative-installation.md)zu überschreiben.

Verwenden Sie keine Eigenschaften für Kenn Wörter oder andere Informationen, die sicher bleiben müssen. Das Installationsprogramm kann den Wert einer Eigenschaft, die in die Eigenschaften Tabelle geschrieben oder zur Laufzeit erstellt wurde, in ein Protokoll oder die Systemregistrierung schreiben.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE05](ice05.md)  
[ICE06](ice06.md)  
[ICE16](ice16.md)  
[ICE24](ice24.md)  
[ICE31](ice31.md)  
[ICE34](ice34.md)  
[ICE36](ice36.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE48](ice48.md)  
[ICE52](ice52.md)  
[ICE61](ice61.md)  
[ICE73](ice73.md)  
[ICE74](ice74.md)  
[ICE80](ice80.md)  
[ICE87](ice87.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
[ICE99](ice99.md)  
</dl>

 

 



