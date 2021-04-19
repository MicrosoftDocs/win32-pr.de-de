---
description: Meta-Qualifizierer verfeinern die Definition von Meta-Konstrukten im CIM-Modell, indem Sie die tatsächliche Verwendung einer Klassen-oder Eigenschafts Deklaration innerhalb der MOF-Syntax verdeutlichen.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Metaqualifizierer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8618ef8258f403a43e08be54b3acbd5bb1e923c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364056"
---
# <a name="meta-qualifiers"></a>Metaqualifizierer

Meta-Qualifizierer verfeinern die Definition von Meta-Konstrukten im CIM-Modell, indem Sie die tatsächliche Verwendung einer Klassen-oder Eigenschafts Deklaration innerhalb der MOF-Syntax verdeutlichen.

<dt>

<span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Anwalt**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Klassen

Gibt an, ob die Klasse eine Zuordnungs Klasse ist, mit der eine Beziehung zwischen zwei anderen Klassen beschrieben wird. Das Fehlen dieses Qualifizierers gibt an, dass die Klasse keine Association-Klasse ist. Diese Qualifizierer schließen sich gegenseitig **aus.** Weitere Informationen finden Sie unter [Deklarieren einer Association-Klasse](declaring-an-association-class.md).

</dd> <dt>

<span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Aufschluss**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Klassen

Gibt an, ob die Objektklasse eine Angabe definiert. Dieser Qualifizierer schließt sich gegenseitig mit **Association** aus. Der Standardwert ist **false**.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI Qualifizierer](wmi-qualifiers.md)
</dt> <dt>

[Fügen eines Qualifizierers](adding-a-qualifier.md)
</dt> </dl>

 

 




