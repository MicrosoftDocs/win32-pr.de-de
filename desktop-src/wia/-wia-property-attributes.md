---
description: Alle Elementobjekte verfügen über Eigenschaften.
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: Eigenschaftenattribute (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdee1cdee48bba6183f9bcae2abc521ac9f53dfb33eec544ab3ed6bead4947b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007530"
---
# <a name="property-attributes-wia"></a>Eigenschaftenattribute (WIA)

Alle Elementobjekte verfügen über Eigenschaften. Die Eigenschaften verfügen über Attribute. Eigenschaftsattribute geben beispielsweise an, ob eine Eigenschaft gelesen, geschrieben oder gelöscht wird. Sie geben auch die gültigen Eigenschaftswerte an. Die folgenden Konstanten sind gültige Eigenschaftsattribute: 

| Eigenschaftsattribut        | Bedeutung                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| WIA \_ PROP \_ CACHEABLE      | Das Gerät kann den Wert der Eigenschaft zwischenspeichern.                                                               |
| \_WIA-PROP-FLAG \_           | Die -Eigenschaft verfügt über eine Liste der Legal Flag-Werte. Flagwerte werden mithilfe einer bitweise **OR-Operation** kombiniert. |
| WIA \_ PROP \_ LIST           | Die -Eigenschaft verfügt über eine Liste der rechtlichen Werte.                                                                 |
| WIA \_ PROP \_ NONE           | Der Eigenschaft sind keine gültigen Werte zugeordnet.                                          |
| WIA \_ PROP \_ RANGE          | Die -Eigenschaft verfügt über einen Bereich gültiger Werte.                                                                |
| WIA \_ PROP \_ READ           | Die Anwendung kann den Wert der Eigenschaft lesen.                                                           |
| WIA \_ PROP \_ RW             | Die Anwendung kann den Wert der Eigenschaft lesen und schreiben.                                                 |
| WIA \_ PROP \_ SYNC \_ ERFORDERLICH | Darf nicht verwendet werden.                                                                                              |
| WIA \_ PROP \_ WRITE          | Die Anwendung kann den Wert der Eigenschaft schreiben.                                                          |



 

 

 



