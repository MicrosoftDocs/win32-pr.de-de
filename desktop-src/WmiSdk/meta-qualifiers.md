---
description: Metaqualifizierer verfeinern die Definition von Metakonstrukten im CIM-Modell, indem sie die tatsächliche Verwendung einer Klassen- oder Eigenschaftendeklaration innerhalb der MOF-Syntax verdeutlichen.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Metaqualifizierer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76609fecca3e3831372ea813e7210cd449c2e1e4fc527df605bc523efd4c1be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131176"
---
# <a name="meta-qualifiers"></a>Metaqualifizierer

Metaqualifizierer verfeinern die Definition von Metakonstrukten im CIM-Modell, indem sie die tatsächliche Verwendung einer Klassen- oder Eigenschaftendeklaration innerhalb der MOF-Syntax verdeutlichen.

<dt>

<span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Verband**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Klassen

Gibt an, ob die Klasse eine Zuordnungsklasse ist, die verwendet wird, um eine Beziehung zwischen zwei anderen Klassen zu beschreiben. Das Fehlen dieses Qualifizierers gibt an, dass die Klasse keine Zuordnungsklasse ist. Dieser Qualifizierer schließen sich mit Indication gegenseitig **aus.** Weitere Informationen finden Sie unter [Deklarieren einer Association-Klasse.](declaring-an-association-class.md)

</dd> <dt>

<span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Angabe**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Klassen

Gibt an, ob die Objektklasse eine Angabe definiert. Dieser Qualifizierer schließen sich mit Association gegenseitig **aus.** Der Standardwert ist **FALSE.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[WMI-Qualifizierer](wmi-qualifiers.md)
</dt> <dt>

[Hinzufügen eines Qualifizierers](adding-a-qualifier.md)
</dt> </dl>

 

 




