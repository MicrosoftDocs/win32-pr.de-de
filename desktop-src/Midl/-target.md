---
title: /target-Schalter
description: Der/Target-Schalter ermöglicht es dem Mittel-Compiler, Optimierungen zu aktivieren, die nur in neueren Versionen von Windows verfügbar sind. Der/Target-Schalter aktiviert automatisch weitere Switches.
ms.assetid: 8c5aa319-e6a6-4803-99f3-ed8751d565d5
keywords:
- /Target-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /target
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 43c17c6bb06eca94a1738ddc71255cd7cd441c5c
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104050652"
---
# <a name="target-switch"></a>/target-Schalter

Der **/target** -Schalter ermöglicht es dem Mittel-Compiler, Optimierungen zu aktivieren, die nur in neueren Versionen von Windows verfügbar sind. Der **/target** -Schalter aktiviert automatisch weitere Switches.

``` syntax
midl /target level
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*level* 
</dt> <dd>

Gibt die Zielebene an, z. b. NT50, NT51, nt60, NT61, NT62 oder NT100.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Schalter **/target** aktiviert basierend auf dem Betriebssystem automatisch weitere Switches, wie in der folgenden Tabelle angegeben:



| Betriebssystem | /Target-Ebene | Aktivierte Switches                     |
|------------------|---------------|----------------------------------------|
| Windows 2000     | NT50          | /Oicf/Error alle/robust               |
| Windows XP       | NT51          | /Oicf/Error alle/robust/Protocol alle |
| Windows Vista    | NT60          | /Oicf/Error alle/robust/Protocol alle |
| Windows 7        | NT61          | /Oicf/Error alle/robust/Protocol alle |
| Windows 8        | NT62          | /Oicf/Error alle/robust/Protocol alle |
| Windows 10       | NT100         | /Oicf/Error alle/robust/Protocol alle |
 

Um sicherzustellen, dass ein Stub auf dem System ausgeführt wird, das durch den **/target** -Schalter angegeben ist, gibt "Mittel l" einen Fehler aus, wenn ein Feature vorhanden ist, das nur auf einer neueren Version von Windows In der folgenden Tabelle wird die minimale **/target** -Ebene angegeben, die zum Aktivieren des Features erforderlich ist. Höhere Zielebenen umfassen alle Features von niedrigeren Zielebenen.



| Mindestens erforderliche/Target-Ebene | Features                                                                                                                                                                                          |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NT50                           | /robust<br/> \[Nachricht\]<br/> \[async\]<br/> \[Async- \_ UUID\]<br/> \[Benachrichtigen \] im/Oicf-Modus<br/> \[Codieren \] oder \[ decodieren \] im/Oicf-Modus<br/>                   |
| NT51                           | /Protocol 64-Bit-Unterstützung<br/> \[teilweise \_ ignorieren\]<br/> \[\_zuordnen erzwingen\]<br/>                                                                                                 |
| NT60                           | Erzwungene komplexe Struktur Marshalling<br/> Kontext Handles in einem Array oder einer Struktur<br/> \[Bereichs \] Unterstützung für Zeichen folgen ohne Größenanpassung<br/> \[Typ \_ Strict- \_ Kontext \_ handle\]<br/> |
| NT61                           | Direkte com-Stub-Aufrufe für Schnittstellen mit weniger als 32 Methoden erfordern das Verknüpfen von com-Stubs mit **OLE32.DLL**.<br/>                                                                          |
| NT62                           | Arm-Unterstützung<br/> WinRT-Unterstützung<br/>                                                                                                                                                   |
| NT100                          | \[system_handle \] Unterstützung<br /> |


 

## <a name="examples"></a>Beispiele

**Mittel l/Target NT50**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>
