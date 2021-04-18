---
description: Windows Installer Upgradepakete können erstellt werden, damit größere Upgrades nicht installiert werden, wenn ein Benutzer bereits eine neuere Version installiert hat.
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: Verhindern, dass ein altes Paket über eine neuere Version installiert wird
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320ab062c4ffbc740d85c59ece3d3baaa63f4209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357513"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a>Verhindern, dass ein altes Paket über eine neuere Version installiert wird

Windows Installer Upgradepakete können erstellt werden, damit größere Upgrades nicht installiert werden, wenn ein Benutzer bereits eine neuere Version installiert hat. Mit dem in diesem Thema beschriebenen Verfahren können nur Herabstufungen verhindert werden, die möglicherweise durch Ausführen eines größeren upgradepakets verursacht werden. Dieses Verfahren basiert auf der [Aktion "FindRelatedProducts](findrelatedproducts-action.md)", die nur während einer erstmaligen Installation ausgeführt wird und nicht im Wartungsmodus (Neuinstallation) ausgeführt wird. Da kleinere Upgrades mithilfe der erneuten Installation durchgeführt werden, kann mit diesem Verfahren nicht bestimmt werden, ob ein geringfügiges Upgradepaket versucht, ein Downgrade für eine Anwendung durchzuführen. Weitere Informationen finden Sie unter [Vorbereiten einer Anwendung für zukünftige größere Upgrades](preparing-an-application-for-future-major-upgrades.md).

**So verhindern Sie, dass ein altes Paket über eine neuere Version installiert wird**

1.  Geben Sie die [**UpgradeCode**](upgradecode.md) -Eigenschaft für die Gruppe verwandter Produkte ein, die möglicherweise berechtigt sind, dieses Upgrade in der UpgradeCode-Spalte der [upgradetabelle](upgrade-table.md)zu erhalten.
2.  Geben Sie das Bitflag **msidbupgradeattributesonlydetect** in der Spalte Attribute der [upgradetabelle](upgrade-table.md)ein.
3.  Geben Sie die Version des Upgrades, das von diesem Paket bereitgestellt wird, in die Spalte versionmin der [upgradetabelle](upgrade-table.md)ein. Lassen Sie die Spalte versionmax leer.
4.  Geben Sie den Namen der Eigenschaft ein, die von der [FindRelatedProducts-Aktion](findrelatedproducts-action.md) in der Action Property-Spalte der [upgradetabelle](upgrade-table.md)festgelegt werden soll.
5.  Fügen Sie der Eigenschaften [Tabelle](property-table.md)die [**securecustomproperties**](securecustomproperties.md) -Eigenschaft und die-Eigenschaft in der Spalte "Aktions Eigenschaft" der [upgradetabelle](upgrade-table.md) hinzu.
6.  Fügen Sie nach der Aktion FindRelatedProducts in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)einen [benutzerdefinierten Aktionstyp 19](custom-action-type-19.md) hinzu. Fügen Sie für diese Aktion einen Datensatz in die [Tabelle "CustomAction](customaction-table.md) " ein, und geben Sie den Text ein, der in der Ziel Spalte angezeigt werden soll. Die benutzerdefinierte Aktion vom Typ 19 ist in das Installationsprogramm integriert, sodass kein Code geschrieben werden kann.
7.  Geben Sie den Namen der Action Property in die Spalte Bedingung des Datensatzes in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) ein, die den [benutzerdefinierten Aktionstyp 19](custom-action-type-19.md)enthält. Dadurch wird die benutzerdefinierte Aktion nur ausgeführt, wenn die [upgradetabelle](upgrade-table.md) erkennt, dass eine neuere Version bereits installiert ist.

    Beispielsweise kann ein Windows Installer Paket, das eine Gruppe verwandter Produkte auf Version 3,0 aktualisiert, in den Tabellen [Upgrade](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md)und [Property](property-table.md) die folgenden Datensätze enthalten. Alle zugehörigen Produkte in der Gruppe verfügen über denselben UpgradeCode, aber das Installationsprogramm installiert dieses Upgradepaket nicht, wenn eine Version, die höher als 3,0 ist, bereits auf dem Computer installiert ist. In diesem Fall zeigt das Installationsprogramm eine Fehlermeldung an, und die Installation schlägt fehl. Das Upgradepaket der Version 3,0 wird über die Versionen 1,0 und 2,0 installiert.

    [Upgradetabelle](upgrade-table.md)

    

    | UpgradeCode auch                            | Versionmin | Versionmax | Sprache | Attribute                                | Entfernen | Aktions Eigenschaft  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | {E7BE6D45-49ff-4701-A17E-BDCC98CE180D} | 3.0        |            |          | msidbupgraabattributesonlydetect          |        | Newproductfound |
    | {E7BE6D45-49ff-4701-A17E-BDCC98CE180D} | 1.0        | 3.0        |          | msidbupgraabattributesversionmininclusive |        | Upgrade gefunden    |

    

     

    [Tabelle "CustomAction"](customaction-table.md)

    

    | Aktion | type | `Source` | Ziel                                 |
    |--------|------|--------|----------------------------------------|
    | KA1    | 19   |        | Ein höheres Upgrade ist bereits installiert. |

    

     

    [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)

    

    | Aktion              | Bedingung       | Sequenz |
    |---------------------|-----------------|----------|
    | FindRelatedProducts |                 | 200      |
    | KA1                 | Newproductfound | 201      |

    

     

    [Eigenschaften Tabelle](property-table.md)

    

    | Eigenschaft                                                 | Wert                        |
    |----------------------------------------------------------|------------------------------|
    | [**Securecustomproperties**](securecustomproperties.md) | Newproductfound; Upgrade gefunden |

    

     

 

 



