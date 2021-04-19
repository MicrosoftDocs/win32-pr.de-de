---
description: In der CheckBox-Tabelle sind die Werte für die Kontrollkästchen aufgeführt.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: CheckBox-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3600b741543a88e7ded71cd385a56b499c8ef516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349808"
---
# <a name="checkbox-table"></a>CheckBox-Tabelle

In der CheckBox-Tabelle sind die Werte für die Kontrollkästchen aufgeführt.

Die CheckBox-Tabelle weist die folgenden Spalten auf.



| Spalte   | Typ                         | Schlüssel | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Eigenschaft | [Bezeichner](identifier.md) | J   | N        |
| Wert    | [Großformatige](formatted.md)   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property
</dt> <dd>

Eine benannte Eigenschaft, die an dieses Element gebunden werden soll.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Die diesem Element zugeordnete Wert Zeichenfolge.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn das Kontrollkästchen aktiviert ist, wird die entsprechende Eigenschaft auf den angegebenen Wert festgelegt. Wenn kein Wert angegeben ist oder diese Tabelle nicht vorhanden ist, wird die-Eigenschaft auf den ursprünglichen Wert festgelegt, wenn das Kontrollkästchen aktiviert ist. Wenn der ursprüngliche Wert NULL ist, wird die-Eigenschaft auf "1" festgelegt.

Der Inhalt der Value-Spalte wird bei der Erstellung des Steuer Elements durch die [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) -Funktion formatiert. Daher kann Sie jeden beliebigen Ausdruck enthalten, der von der **msiformatrecord** -Funktion interpretiert werden kann. Die Value-Spalte wird nur formatiert, wenn das Steuerelement erstellt wird, und wird nicht aktualisiert, wenn eine an einem Ausdruck beteiligte Eigenschaft während der Lebensdauer des Steuer Elements geändert wird.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



