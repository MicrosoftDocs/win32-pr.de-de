---
description: Die UIText-Tabelle enthält die lokalisierten Versionen einiger der Zeichen folgen, die in der Benutzeroberfläche verwendet werden. Diese Zeichen folgen sind nicht Teil einer anderen Tabelle. Die UIText-Tabelle ist für Zeichen folgen, die keine logische Position in einer anderen Tabelle aufweisen.
ms.assetid: 2965e3a8-2cbf-4445-963b-ec2040692106
title: UIText-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5fe8bbdec694511103636508d229ab0d2e40afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128100"
---
# <a name="uitext-table"></a>UIText-Tabelle

Die UIText-Tabelle enthält die lokalisierten Versionen einiger der Zeichen folgen, die in der Benutzeroberfläche verwendet werden. Diese Zeichen folgen sind nicht Teil einer anderen Tabelle. Die UIText-Tabelle ist für Zeichen folgen, die keine logische Position in einer anderen Tabelle aufweisen.

Die UIText-Tabelle weist die folgenden Spalten auf.



| Spalte | Typ                         | Schlüssel | Nullwerte zulässig |
|--------|------------------------------|-----|----------|
| Schlüssel    | [Bezeichner](identifier.md) | J   | N        |
| Text   | [Text](text.md)             | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Wichtigen
</dt> <dd>

Ein eindeutiger Schlüssel, der die jeweilige Zeichenfolge identifiziert.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Die lokalisierte Version der Zeichenfolge.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Einige Steuerelemente verwenden die UIText-Tabelle als Quelle von Zeichen folgen. Informationen dazu, welche Zeichen folgen in dieser Tabelle für jedes bestimmte Steuerelement erforderlich sind, finden Sie unter den einzelnen Steuerelementen in der [Benutzeroberflächen Referenz](user-interface-reference.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



