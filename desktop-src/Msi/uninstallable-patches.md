---
description: Ob ein Patch deinstalliert werden kann, hängt davon ab, wie der Patch erstellt wurde, der Version von Windows Installer, die zur Installation des Patches verwendet wurde, und der Änderungen, die vom Patch an der Anwendung vorgenommen wurden.
ms.assetid: 95a5365c-e2ae-4e35-9aeb-67d04e67c7df
title: Nicht installierbare Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad46d85318378ed81d2278d3ea1290152723704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524887"
---
# <a name="uninstallable-patches"></a>Nicht installierbare Patches

Ob ein Patch deinstalliert werden kann, hängt davon ab, wie der Patch erstellt wurde, der Version von Windows Installer, die zur Installation des Patches verwendet wurde, und der Änderungen, die vom Patch an der Anwendung vorgenommen wurden. Wenn ein Patch nicht deinstalliert werden kann, besteht die einzige Möglichkeit zum Entfernen des Patches darin, die gesamte Anwendung zu deinstallieren und neu zu installieren, ohne dass der zu entfernende Patch angewendet wird.

Sie können für die Deinstallieren von Patches, die mit Windows Installer Version 3,0 angewendet werden, mithilfe der [Befehlszeilenoptionen](command-line-options.md), der [**msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) -Funktion oder der [**removepatches-Methode**](installer-removepatches.md) , wie im Abschnitt [Deinstallieren von Patches](uninstalling-patches.md) beschrieben, aufgerufen werden. Die Windows Installer überprüft, ob jedes der Patches, die in der [**msipatchremove**](msipatchremove.md) -Eigenschaft zum Entfernen aufgeführt werden, nicht installierbar ist. Wenn der Benutzer keine Berechtigungen zum Entfernen des Patches hat, ist der Patch für das Produkt unbekannt, die patchrichtlinie verhindert das Entfernen, oder der Patch wurde als nicht deinstallable gekennzeichnet. der Installer gibt eine Fehlermeldung zurück, die auf eine fehlgeschlagene Installations Transaktion hinweist.

**Windows Installer 2,0:** Nicht unterstützt. Patches, die mit einer früheren Version von Windows Installer als Windows Installer 3,0 angewendet wurden, können nicht installiert werden.

## <a name="patches-that-are-not-uninstallable"></a>Patches, die nicht installiert werden können

Ein Patch (. msp-Datei), der auf eine installierte Anwendung angewendet wird, kann in den folgenden Fällen nicht deinstalliert werden. Die einzige Methode zum Entfernen eines Patches, der nicht deinstalliert werden kann, besteht darin, die gepatchte Anwendung zu deinstallieren und die Anwendung dann erneut zu installieren, ohne den Patch erneut anzuwenden. In diesem Fall müssen Sie alle Patches erneut anwenden, die nicht aus der Anwendung entfernt werden sollen.

-   Patches, die mit einer Version von Windows Installer angewendet werden, die kleiner als Windows Installer 3,0 ist, können nicht installiert werden.
-   Patches, die auf auf einem Computer installierte Anwendungen angewendet werden, auf denen die von einem Administrator festgelegte [disablepatchuninstall](disablepatchuninstall.md) -Richtlinie installiert ist, können nicht installiert werden. Wenn diese Computer [Richtlinie](machine-policies.md)festgelegt wurde, können keine Patches auf dem Computer deinstalliert werden, auch nur von einem Administrator.
-   Patches, die keine [MsiPatchMetadata](msipatchmetadata-table.md) -Tabelle in Ihrer Datenbank aufweisen, können nicht installiert werden.
-   Patches, die die folgende Zeile in der [MsiPatchMetadata](msipatchmetadata-table.md) -Tabelle nicht enthalten, können nicht installiert werden. Der Patch kann für andere Werte des Unternehmens, der Eigenschaft und des Werts nicht installiert werden.

    | Company | Eigenschaft     | Wert |
    |---------|--------------|-------|
    | Normal  | Allowremoval | 1     |

    

     

-   Der Patch wurde auf eine Anwendung angewendet, die in einem Kontext installiert wurde, für den der Benutzer nicht über ausreichende Berechtigungen zum Deinstallieren von Patches verfügt. Die Wörter "nicht zulässig" in der folgenden Tabelle geben an, dass ein Administrator oder ein nicht Administrator Benutzer keine Patches aus gepatchten Anwendungen deinstallieren kann, die in diesem Kontext installiert sind. Das Wort "Allowed" in dieser Tabelle bedeutet, dass Berechtigungen keinen Administrator oder Benutzer ohne Administratorrechte daran hindern, Patches zu deinstallieren. aus den anderen in diesem Abschnitt beschriebenen Gründen ist es jedoch möglicherweise nicht möglich, den Patch zu deinstallieren.

    | anwendungsinstallationskontext        | Deinstallieren des Patches durch den Administrator | Deinstallation des Patches durch nicht Administrator                                                                                                                                                                                                                                                                             |
    |-----------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Per-Machine                             | Zulässig                          | In der Regel nicht zulässig ist die einzige Ausnahme, wenn der Patch mit dem Patching (LUA) angewendet wurde. Ein Patch, der als Lua-Patch gekennzeichnet ist, kann weder von Administratoren noch von nicht Administratoren installiert werden. Das Lua-Patchen ist nur für Pakete verfügbar, die von einem Medium pro Computer installiert werden und eine besondere Erstellung erfordern.<br/> |
    | Per-User für den aktuellen Benutzer nicht verwaltet   | Zulässig                          | Zulässig                                                                                                                                                                                                                                                                                                          |
    | Per-User nicht verwaltet für einen anderen Benutzer | Nicht zulässig                      | Nicht zulässig                                                                                                                                                                                                                                                                                                      |
    | Für aktuellen Benutzer Per-User verwaltet       | Zulässig                          | Nicht zulässig                                                                                                                                                                                                                                                                                                      |
    | Per-User für andere Benutzer verwaltet     | Nicht zulässig                      | Nicht zulässig                                                                                                                                                                                                                                                                                                      |

    

     

-   Ein [wichtiges Upgrade](major-upgrades.md) , das von einem Patch angewendet wird, kann nicht installiert werden. Wichtige Upgrades einer Anwendung sollten ausgeführt werden, indem die aktualisierte Anwendung (MSI-Datei) anstelle eines Patches installiert wird.
-   Auf eine administrative Installation angewendete Patches können nicht installiert werden. Das Patchen administrativer Installationen wird nicht empfohlen. Der aktuelle Satz von Patches sollte auf den Computer des Benutzers angewendet werden, nachdem der Benutzer die Anwendung über das administrative image installiert hat. Dadurch kann verhindert werden, dass sich der auf dem Computer des Benutzers zwischengespeicherte [Paketcode](package-codes.md) von dem Paket Code bei der administrativen Installation unterscheidet. Wenn sich der Paket Code, der auf dem Computer des Benutzers zwischengespeichert ist, von dem auf dem Computer des Benutzers unterscheidet, installieren Sie die Anwendung über die administrative Installation neu, und Patchen Sie dann den Client Computer.
-   Wenn ein Patch einer der Tabellen in der folgenden Liste neuen Inhalt hinzufügt, markiert Windows Installer den Patch als nicht installier Bar. Mit einem nicht installierbaren Patch können einer-Installation neue Dateien, Assemblys, Registrierungseinträge, Komponenten oder Features hinzugefügt werden, indem Datenbanktabellen neue Zeilen hinzugefügt werden, die nicht in dieser Liste enthalten sind.

    -   [AppId](appid-table.md)
    -   [BindImage](bindimage-table.md)
    -   [Klasse](class-table.md)
    -   [ComPlus](complus-table.md)
    -   [CreateFolder](createfolder-table.md)
    -   [Duplicatefile](duplicatefile-table.md)
    -   [Umgebung](environment-table.md)
    -   [Erweiterung](extension-table.md)
    -   [Schriftart](font-table.md)
    -   [INIFILE](inifile-table.md)
    -   [Isolatedcomponent](isolatedcomponent-table.md)
    -   [Sperr Berechtigungen](lockpermissions-table.md)
    -   [Msilockpermissionsex](msilockpermissionsex-table.md)
    -   [Medi](mime-table.md)
    -   [MoveFile](movefile-table.md)
    -   [Msiserviceconfig](msiserviceconfig-table.md)
    -   [Msiserviceconfigfailureactions](msiserviceconfigfailureactions-table.md)
    -   [Odbcatcher Tribute](odbcattribute-table.md)
    -   [ODBCDatasource](odbcdatasource-table.md)
    -   [Odbcdriver](odbcdriver-table.md)
    -   [Odbcsourceattribute](odbcsourceattribute-table.md)
    -   [Odbctranslator](odbctranslator-table.md)
    -   [ProgID](progid-table.md)
    -   [PublishComponent](publishcomponent-table.md)
    -   [Removeinifile](removeinifile-table.md)
    -   [Selfreg](selfreg-table.md)
    -   [ServiceControl](servicecontrol-table.md)
    -   [Serviceingestall](serviceinstall-table.md)
    -   [Export der Typbibliothek](typelib-table.md)
    -   [Verb](verb-table.md)
    -   [!Note]  
        > Wenn ein Patch den Tabellen [RemoveFile](removefile-table.md) oder [removeregistry](removeregistry-table.md) neuen Inhalt hinzufügt, markiert Windows Installer den Patch nicht als nicht installier Bar. Der Patch kann jedoch nicht deinstallieren, es sei denn, die Ressource, die den neuen Inhalt entfernen soll, ist im ursprünglichen Installationspaket nicht bereits vorhanden. Wenn der Patch beispielsweise der Tabelle "RemoveFile" eine neue Zeile hinzufügt, kann die entfernte Datei nicht durch Deinstallieren des Patches wieder hergestellt werden, wenn die Datei für die [Dateitabelle](file-table.md)extern ist. Die Datei muss in der Dateitabelle des ursprünglichen Pakets sowie angewendete Patches erstellt worden sein, damit der Patch nicht installiert werden kann.

         

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patchsequenzierung](sequencing-patches.md)
</dt> <dt>

[Entfernen von Patches](removing-patches.md)
</dt> <dt>

[Patches werden deinstalliert.](uninstalling-patches.md)
</dt> <dt>

[Patch zum Deinstallieren benutzerdefinierter Aktionen](patch-uninstall-custom-actions.md)
</dt> <dt>

[**Msipatchremove**](msipatchremove.md)
</dt> <dt>

[**Msienumapplicationsex**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**Msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**Msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 




