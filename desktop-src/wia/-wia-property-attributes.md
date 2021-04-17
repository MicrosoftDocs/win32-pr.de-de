---
description: Alle Element Objekte verfügen über Eigenschaften.
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: Eigenschafts Attribute (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c635cb0d4e21fe2a1d65a3f21254f8e9c04d64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485059"
---
# <a name="property-attributes-wia"></a>Eigenschafts Attribute (WIA)

Alle Element Objekte verfügen über Eigenschaften. Die Eigenschaften verfügen über Attribute. Beispielsweise geben Eigenschafts Attribute an, ob eine Eigenschaft aus gelesen, geschrieben oder gelöscht wird. Sie geben auch die gültigen Eigenschaftswerte an. Die folgenden Konstanten sind gültige Eigenschafts Attribute: 

| Property-Attribut        | Bedeutung                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| WIA-Unterstützung zwischen speicherbar \_ \_      | Das Gerät kann den Wert der Eigenschaft Zwischenspeichern.                                                               |
| WIA- \_ Prop- \_ Flag           | Die-Eigenschaft verfügt über eine Liste der zulässigen Flagwerte. Flagwerte werden mithilfe einer bitweisen **or** -Operation kombiniert. |
| WIA- \_ Prop- \_ Liste           | Die-Eigenschaft verfügt über eine Liste der zulässigen Werte.                                                                 |
| WIA- \_ Prop \_ None           | Der-Eigenschaft sind keine gültigen Werte zugeordnet.                                          |
| WIA- \_ Prop- \_ Bereich          | Die-Eigenschaft weist einen Bereich gültiger Werte auf.                                                                |
| WIA- \_ Prop- \_ Lesevorgang           | Die Anwendung kann den Wert der Eigenschaft lesen.                                                           |
| WIA- \_ Prop- \_ RW             | Die Anwendung kann den Wert der Eigenschaft lesen und schreiben.                                                 |
| WIA- \_ Prop- \_ Synchronisierung \_ erforderlich | Darf nicht verwendet werden.                                                                                              |
| WIA- \_ Prop- \_ Schreibvorgang          | Die Anwendung kann den Wert der Eigenschaft schreiben.                                                          |



 

 

 



