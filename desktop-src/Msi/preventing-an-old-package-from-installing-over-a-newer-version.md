---
description: Windows Installationsupgradepakete können so erstellt werden, dass größere Upgrades nicht installiert werden, wenn ein Benutzer bereits eine neuere Version installiert hat.
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: Verhindern der Installation eines alten Pakets über eine neuere Version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e992cc1e32d2b25e5af587c00ca4f8ee28e4b09fd3100cb12b382ae90f8c1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145383"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a>Verhindern der Installation eines alten Pakets über eine neuere Version

Windows Installationsupgradepakete können so erstellt werden, dass größere Upgrades nicht installiert werden, wenn ein Benutzer bereits eine neuere Version installiert hat. Das Verfahren in diesem Thema kann nur Downgrades verhindern, die durch die Ausführung eines größeren Upgradepakets verursacht werden können. Dieses Verfahren basiert auf der [FindRelatedProducts-Aktion,](findrelatedproducts-action.md)die nur während einer erstmaligen Installation und nicht im Wartungsmodus (Neuinstallation) ausgeführt wird. Da kleinere Upgrades mithilfe der Neuinstallation durchgeführt werden, kann dieses Verfahren nicht verwendet werden, um zu bestimmen, ob ein kleineres Upgradepaket versucht, eine Anwendung herabzustufen. Weitere Informationen finden Sie unter [Vorbereiten einer Anwendung für zukünftige größere Upgrades.](preparing-an-application-for-future-major-upgrades.md)

**So verhindern Sie, dass ein altes Paket über eine neuere Version installiert wird**

1.  Geben Sie die [**UpgradeCode-Eigenschaft**](upgradecode.md) für die Gruppe verwandter Produkte ein, die möglicherweise berechtigt sind, dieses Upgrade zu erhalten, in die Spalte UpgradeCode der [Upgradetabelle](upgrade-table.md).
2.  Geben Sie das Bitflag **msidbUpgradeAttributesOnlyDetect** in der Spalte Attribute der [Upgradetabelle](upgrade-table.md)ein.
3.  Geben Sie die Von diesem Paket bereitgestellte Upgradeversion in die Spalte VersionMin der [Upgradetabelle](upgrade-table.md)ein. Lassen Sie die Spalte VersionMax leer.
4.  Geben Sie den Namen der Eigenschaft ein, die von der [FindRelatedProducts-Aktion](findrelatedproducts-action.md) in der Spalte ActionProperty der [Upgradetabelle](upgrade-table.md)festgelegt werden soll.
5.  Fügen Sie die [**SecureCustomProperties-Eigenschaft**](securecustomproperties.md) und die Eigenschaft namens in der ActionProperty -Spalte der [Upgradetabelle](upgrade-table.md) der [Eigenschaftentabelle](property-table.md)hinzu.
6.  Fügen Sie nach der Aktion FindRelatedProducts in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)einen [benutzerdefinierten Aktionstyp 19](custom-action-type-19.md) hinzu. Fügen Sie einen Datensatz in die [Tabelle CustomAction](customaction-table.md) für diese Aktion ein, und geben Sie den Text ein, der in der Spalte Target angezeigt werden soll. Die benutzerdefinierte Aktion vom Typ 19 ist in das Installationsprogramm integriert, sodass kein Code geschrieben werden muss.
7.  Geben Sie den Namen der ActionProperty in die Spalte Bedingung des Datensatzes in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md) ein, die den [benutzerdefinierten Aktionstyp 19](custom-action-type-19.md)enthält. Dadurch wird die benutzerdefinierte Aktion nur ausgeführt, wenn die [Upgradetabelle](upgrade-table.md) erkennt, dass bereits eine neuere Version installiert ist.

    Beispielsweise kann ein Windows Installer-Paket, das eine Gruppe verwandter Produkte auf Version 3.0 aktualisiert, die folgenden Datensätze in den Tabellen [Upgrade,](upgrade-table.md) [CustomAction,](customaction-table.md) [InstallExecuteSequence](installexecutesequence-table.md)und [Property](property-table.md) enthalten. Alle zugehörigen Produkte in der Gruppe verfügen über den gleichen UpgradeCode, aber das Installationsprogramm installiert dieses Upgradepaket nicht, wenn eine höhere Version als 3.0 bereits auf dem Computer installiert ist. In diesem Fall zeigt der Installer eine Fehlermeldung an, und die Installation schlägt fehl. Das Upgradepaket für Version 3.0 wird über die Versionen 1.0 und 2.0 installiert.

    [Upgradetabelle](upgrade-table.md)

    

    | Upgradecode                            | VersionMin | VersionMax | Sprache | Attribute                                | Entfernen | ActionProperty  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 3.0        |            |          | msidbUpgradeAttributesOnlyDetect          |        | NEWPRODUCTFOUND |
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 1.0        | 3.0        |          | msidbUpgradeAttributesVersionMinInclusive |        | UPGRADEFOUND    |

    

     

    [CustomAction-Tabelle](customaction-table.md)

    

    | Aktion | type | `Source` | Ziel                                 |
    |--------|------|--------|----------------------------------------|
    | KA1    | 19   |        | Ein höheres Upgrade ist bereits installiert. |

    

     

    [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)

    

    | Aktion              | Bedingung       | Sequenz |
    |---------------------|-----------------|----------|
    | FindRelatedProducts |                 | 200      |
    | KA1                 | NEWPRODUCTFOUND | 201      |

    

     

    [Eigenschaftentabelle](property-table.md)

    

    | Eigenschaft                                                 | Wert                        |
    |----------------------------------------------------------|------------------------------|
    | [**SecureCustomProperties**](securecustomproperties.md) | NEWPRODUCTFOUND; UPGRADEFOUND |

    

     

 

 



