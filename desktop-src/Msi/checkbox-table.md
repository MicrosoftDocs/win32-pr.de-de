---
description: Die CheckBox-Tabelle listet die Werte für die Kontrollkästchen auf.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: CheckBox-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848769f9430681a8c37de0afd8d9d1fa8abfee2f833798ecbdc5271535f79da4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649870"
---
# <a name="checkbox-table"></a>CheckBox-Tabelle

Die CheckBox-Tabelle listet die Werte für die Kontrollkästchen auf.

Die CheckBox-Tabelle enthält die folgenden Spalten.



| Spalte   | Typ                         | Key | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Eigenschaft | [Identifier](identifier.md) | J   | N        |
| Wert    | [Formatiert](formatted.md)   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Eigenschaft
</dt> <dd>

Eine benannte Eigenschaft, die an dieses Element gebunden werden soll.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Die diesem Element zugeordnete Wertzeichenfolge.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn das Kontrollkästchen aktiviert ist, wird die entsprechende Eigenschaft auf den angegebenen Wert festgelegt. Wenn kein Wert angegeben ist oder diese Tabelle nicht vorhanden ist, wird die -Eigenschaft auf ihren ursprünglichen Wert festgelegt, wenn das Kontrollkästchen aktiviert ist. Wenn der ursprüngliche Wert NULL ist, wird die -Eigenschaft auf "1" festgelegt.

Der Inhalt der Value-Spalte wird von der [**MsiFormatRecord-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) formatiert, wenn das Steuerelement erstellt wird. Daher kann sie jeden Ausdruck enthalten, den die **MsiFormatRecord-Funktion** interpretieren kann. Die Spalte Wert wird nur formatiert, wenn das Steuerelement erstellt wird, und sie wird nicht aktualisiert, wenn eine eigenschaft, die an einem Ausdruck beteiligt ist, während der Lebensdauer des Steuerelements geändert wird.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



