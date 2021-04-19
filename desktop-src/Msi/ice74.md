---
description: ICE74 überprüft, ob die FASTOEM-Eigenschaft in der Eigenschaften Tabelle nicht erstellt wurde.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fe2762710e061f2c88f55893294a40fbac8700f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348455"
---
# <a name="ice74"></a>ICE74

ICE74 überprüft, ob die [**FASTOEM**](fastoem.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md)nicht erstellt wurde.

Mit der [**FASTOEM**](fastoem.md) -Eigenschaft können OEMs den Zeitaufwand für die erstmalige Installation Windows Installer Anwendungen verkürzen. Sie kann nach der ersten Installation nicht verwendet werden. Die **FASTOEM** -Eigenschaft darf nicht in der Eigenschaften Tabelle erstellt werden, da dies zu den nachfolgenden Installationen für die Wartung, Entfernung oder Reparatur der Anwendung beeinträchtigt.

ICE74 überprüft auch, ob die [**UpgradeCode**](upgradecode.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md)erstellt wurde und ob der Wert keine NULL-GUID ist {00000000-0000-0000-0000-000000000000} .

## <a name="result"></a>Ergebnis

ICE74 kann die folgenden Fehler veröffentlichen.



| ICE74-Fehler                                                                       | BESCHREIBUNG                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Die [**FASTOEM**](fastoem.md) -Eigenschaft kann in der Eigenschaften Tabelle nicht erstellt werden. | Die [**FASTOEM**](fastoem.md) -Eigenschaft wurde in der Eigenschaften Tabelle festgelegt.                             |
| " \[ 2 \] " ist kein gültiger [**UpgradeCode**](upgradecode.md).                        | Eine NULL-GUID wurde für die [**UpgradeCode**](upgradecode.md) -Eigenschaft in der Eigenschaften Tabelle eingegeben. |



 

ICE74 kann folgende Warnung veröffentlichen.



| ICE74-Warnung                                                                                                                                                                                             | BESCHREIBUNG                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Die [**UpgradeCode**](upgradecode.md) -Eigenschaft ist in der Eigenschaften Tabelle nicht erstellt. Es wird dringend empfohlen, dass Autoren von Installationspaketen einen **UpgradeCode** für Ihre Anwendung angeben. | Die [**UpgradeCode**](upgradecode.md) -Eigenschaft ist in der Eigenschaften Tabelle nicht erstellt. |



 

## <a name="example"></a>Beispiel

ICE74 meldet den folgenden Fehler, wenn die [**FASTOEM**](fastoem.md) -Eigenschaft festgelegt ist: FASTOEM

``` syntax
 property cannot be authored in the Property table.
```

[Eigenschaften Tabelle](property-table.md) (partiell)



| Eigenschaft                   | Wert |
|----------------------------|-------|
| [**FASTOEM**](fastoem.md) | 1     |



 

Entfernen Sie die [**FASTOEM**](fastoem.md) -Eigenschaft aus der Eigenschaften Tabelle, um diesen Fehler zu beheben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**FASTOEM-Eigenschaft**](fastoem.md)
</dt> <dt>

[Eigenschaften Tabelle](property-table.md)
</dt> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



