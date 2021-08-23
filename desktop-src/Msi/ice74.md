---
description: ICE74 überprüft, ob die FASTOEM-Eigenschaft nicht in der Property-Tabelle erstellt wurde.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3120b0f4cd40acc53a1bcd3623dac33941a7f5da39bc538781e4ffd1d56345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328320"
---
# <a name="ice74"></a>ICE74

ICE74 überprüft, ob die [**FASTOEM-Eigenschaft**](fastoem.md) nicht in der [Property-Tabelle](property-table.md)erstellt wurde.

Mit der [**FASTOEM-Eigenschaft**](fastoem.md) können OEMs die Zeit verkürzen, die zum erstmaligen Installieren Windows Installer-Anwendungen erforderlich ist. Sie kann nach der ersten Installation nicht mehr verwendet werden. Die **FASTOEM-Eigenschaft** darf nicht in der Property-Tabelle erstellt werden, da dies nachfolgende Installationen für die Wartung, Entfernung oder Reparatur der Anwendung beeinträchtigt.

ICE74 überprüft auch, ob die [**UpgradeCode-Eigenschaft**](upgradecode.md) in der [Property-Tabelle](property-table.md)erstellt wurde und dass ihr Wert keine NULL-GUID, , {00000000-0000-0000-0000-000000000000} ist.

## <a name="result"></a>Ergebnis

ICE74 kann die folgenden Fehler melden.



| ICE74-Fehler                                                                       | Beschreibung                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Die [**FASTOEM-Eigenschaft**](fastoem.md) kann nicht in der Property-Tabelle erstellt werden. | Die [**FASTOEM-Eigenschaft**](fastoem.md) wurde in der Tabelle Property festgelegt.                             |
| ' \[ 2 \] ' ist kein gültiger [**UpgradeCode.**](upgradecode.md)                        | Für die [**UpgradeCode-Eigenschaft**](upgradecode.md) in der Tabelle Property wurde eine NULL-GUID eingegeben. |



 

ICE74 kann die folgende Warnung posten.



| ICE74-Warnung                                                                                                                                                                                             | Beschreibung                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Die [**UpgradeCode-Eigenschaft**](upgradecode.md) wird nicht in der Property-Tabelle erstellt. Es wird dringend empfohlen, dass Autoren von Installationspaketen einen **UpgradeCode** für ihre Anwendung angeben. | Die [**UpgradeCode-Eigenschaft**](upgradecode.md) wird nicht in der Property-Tabelle erstellt. |



 

## <a name="example"></a>Beispiel

ICE74 meldet den folgenden Fehler, wenn die [**FASTOEM-Eigenschaft**](fastoem.md) festgelegt ist: Fastoem

``` syntax
 property cannot be authored in the Property table.
```

[Eigenschaftentabelle](property-table.md) (partiell)



| Eigenschaft                   | Wert |
|----------------------------|-------|
| [**FASTOEM**](fastoem.md) | 1     |



 

Um diesen Fehler zu beheben, entfernen Sie die [**FASTOEM-Eigenschaft**](fastoem.md) aus der Eigenschaftentabelle.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**FASTOEM-Eigenschaft**](fastoem.md)
</dt> <dt>

[Eigenschaftentabelle](property-table.md)
</dt> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



