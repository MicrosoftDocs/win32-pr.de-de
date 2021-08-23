---
description: Ob ein Patch deinstalliert werden kann, hängt davon ab, wie der Patch erstellt wurde, welche Version von Windows Installer zum Installieren des Patches verwendet wurde und welche Änderungen vom Patch an der Anwendung vorgenommen wurden.
ms.assetid: 95a5365c-e2ae-4e35-9aeb-67d04e67c7df
title: Deinstallationsfähige Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a3abea369a09dd51e995ba28dcab1463032bb6e5dec9648d3eae39be4cbf21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527640"
---
# <a name="uninstallable-patches"></a>Deinstallationsfähige Patches

Ob ein Patch deinstalliert werden kann, hängt davon ab, wie der Patch erstellt wurde, welche Version von Windows Installer zum Installieren des Patches verwendet wurde und welche Änderungen vom Patch an der Anwendung vorgenommen wurden. Wenn ein Patch nicht deinstalliert werden kann, besteht die einzige Möglichkeit zum Entfernen des Patches darin, die gesamte Anwendung zu deinstallieren und neu zu installieren, ohne dass der Patch entfernt wird.

Sie können die Deinstallation von Patches aufrufen, die mit Windows Installer Version 3.0 angewendet wurden, indem Sie [Befehlszeilenoptionen,](command-line-options.md)die [**MsiRemovePatches-Funktion**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) oder die [**RemovePatches-Methode**](installer-removepatches.md) verwenden, wie im Abschnitt [Deinstallieren von Patches](uninstalling-patches.md) beschrieben. Der Windows Installer überprüft, ob jedes der Patches, die in der [**MSIPATCHREMOVE-Eigenschaft**](msipatchremove.md) zum Entfernen aufgeführt sind, deinstalliert werden kann. Wenn der Benutzer nicht über berechtigungen zum Entfernen des Patches verfügt, der Patch für das Produkt unbekannt ist, die Patchrichtlinie das Entfernen verhindert oder der Patch als nicht deinstallationsfähig markiert wurde, gibt das Installationsprogramm einen Fehler zurück, der auf eine fehlgeschlagene Installationstransaktion hinweist.

**Windows Installer 2.0:** Wird nicht unterstützt. Patches, die mit einer Version von Windows Installer angewendet werden, die älter als Windows Installer 3.0 ist, können nicht deinstalliert werden.

## <a name="patches-that-are-not-uninstallable"></a>Patches, die nicht deinstalliert werden können

Ein Patch (MSP-Datei), der auf eine installierte Anwendung angewendet wird, kann in den folgenden Fällen nicht deinstalliert werden. Die einzige Methode zum Entfernen eines Patches, der nicht deinstalliert werden kann, besteht darin, die gepatchte Anwendung zu deinstallieren und dann die Anwendung neu zu installieren, ohne den Patch erneut anwenden zu müssen. In diesem Fall müssen Sie alle Patches erneut anwenden, die nicht aus der Anwendung entfernt werden sollen.

-   Patches, die mit einer Version von Windows Installer angewendet werden, die kleiner als Windows Installer 3.0 ist, können nicht deinstalliert werden.
-   Patches, die auf Anwendungen angewendet werden, die auf einem Computer installiert sind, auf dem die [Richtlinie DisablePatchUninstall](disablepatchuninstall.md) von einem Administrator festgelegt wurde, können nicht deinstalliert werden. Wenn diese [Computerrichtlinie](machine-policies.md)festgelegt wurde, können auch von einem Administrator keine Patches auf dem Computer deinstalliert werden.
-   Patches, die keine [MsiPatchMetadata-Tabelle](msipatchmetadata-table.md) in ihrer Datenbank enthalten, können nicht deinstalliert werden.
-   Patches, die die folgende Zeile nicht in der [MsiPatchMetadata-Tabelle](msipatchmetadata-table.md) enthalten, können nicht deinstalliert werden. Der Patch kann für andere Werte von Unternehmen, Eigenschaft und Wert nicht deinstalliert werden.

    | Company | Eigenschaft     | Wert |
    |---------|--------------|-------|
    | {Null}  | AllowRemoval | 1     |

    

     

-   Der Patch wurde auf eine Anwendung angewendet, die in einem Kontext installiert ist, für den der Benutzer nicht über ausreichende Berechtigungen zum Deinstallieren von Patches verfügt. Die Wörter "Nicht zulässig" in der folgenden Tabelle geben an, dass ein Administrator oder Benutzer ohne Administratorrechte keine Patches aus gepatchten Anwendungen deinstallieren kann, die in diesem Kontext installiert sind. Das Wort "Zulässig" in dieser Tabelle bedeutet, dass Berechtigungen einen Administrator oder Benutzer ohne Administratorrechte nicht daran hindern, Patches zu deinstallieren. Aus einem der anderen in diesem Abschnitt beschriebenen Gründe ist es jedoch möglicherweise immer noch nicht möglich, den Patch zu deinstallieren.

    | Anwendungsinstallationskontext        | Administratordeinstallation des Patches | Nicht-Administratordeinstallation des Patches                                                                                                                                                                                                                                                                             |
    |-----------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Per-Machine                             | Zulässig                          | Allgemein nicht zulässig Die einzige Ausnahme ist, wenn der Patch mithilfe von (LUA)-Patching angewendet wurde. Ein als LUA-Patch markierter Patch kann entweder von Administratoren oder nicht von Administratoren deinstalliert werden. LUA-Patches sind nur für Pakete verfügbar, die pro Computer über Medien installiert werden und eine spezielle Erstellung erfordern.<br/> |
    | Per-User nicht verwaltet für den aktuellen Benutzer   | Zulässig                          | Zulässig                                                                                                                                                                                                                                                                                                          |
    | Per-User nicht verwaltet für verschiedene Benutzer | Nicht zulässig                      | Nicht zulässig                                                                                                                                                                                                                                                                                                      |
    | Per-User für den aktuellen Benutzer verwaltet       | Zulässig                          | Nicht zulässig                                                                                                                                                                                                                                                                                                      |
    | Per-User für verschiedene Benutzer verwaltet     | Nicht zulässig                      | Nicht zulässig                                                                                                                                                                                                                                                                                                      |

    

     

-   Ein [größeres Upgrade,](major-upgrades.md) das von einem Patch angewendet wird, kann nicht deinstalliert werden. Größere Upgrades einer Anwendung sollten durchgeführt werden, indem die aktualisierte Anwendung (.msi-Datei) anstelle eines Patches installiert wird.
-   Patches, die auf eine Administratorinstallation angewendet werden, können nicht deinstalliert werden. Das Patchen von Administratorinstallationen wird nicht empfohlen. Der aktuelle Satz von Patches sollte auf den Computer des Benutzers angewendet werden, nachdem der Benutzer die Anwendung über das Administratorimage installiert hat. Dadurch kann verhindert werden, dass sich der auf dem Computer des Benutzers zwischengespeicherte [Paketcode](package-codes.md) von dem Paketcode bei der Administratorinstallation unterscheidet. Wenn sich der auf dem Computer des Benutzers zwischengespeicherte Paketcode von dem auf der Administratorinstallation unterscheidet, installieren Sie die Anwendung über die Administratorinstallation neu, und patchen Sie dann den Clientcomputer.
-   Wenn ein Patch einer der Tabellen in der folgenden Liste neuen Inhalt hinzufügt, markiert Windows Installer den Patch als nicht deinstallationsfähig. Ein deinstallationsfähiger Patch kann einer Installation neue Dateien, Assemblys, Registrierungseinträge, Komponenten oder Features hinzufügen, indem datenbanktabellen neue Zeilen hinzugefügt werden, die nicht in dieser Liste enthalten sind.

    -   [AppId](appid-table.md)
    -   [BindImage](bindimage-table.md)
    -   [Klasse](class-table.md)
    -   [Complus](complus-table.md)
    -   [CreateFolder](createfolder-table.md)
    -   [DuplicateFile](duplicatefile-table.md)
    -   [Umgebung](environment-table.md)
    -   [Erweiterung](extension-table.md)
    -   [Schriftart](font-table.md)
    -   [IniFile](inifile-table.md)
    -   [IsolatedComponent](isolatedcomponent-table.md)
    -   [LockPermissions](lockpermissions-table.md)
    -   [MsiLockPermissionsEx](msilockpermissionsex-table.md)
    -   [Mime](mime-table.md)
    -   [MoveFile](movefile-table.md)
    -   [MsiServiceConfig](msiserviceconfig-table.md)
    -   [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md)
    -   [ODBCAttribute](odbcattribute-table.md)
    -   [ODBCDataSource](odbcdatasource-table.md)
    -   [ODBCDriver](odbcdriver-table.md)
    -   [ODBCSourceAttribute](odbcsourceattribute-table.md)
    -   [ODBCTranslator](odbctranslator-table.md)
    -   [Progid](progid-table.md)
    -   [PublishComponent](publishcomponent-table.md)
    -   [RemoveIniFile](removeinifile-table.md)
    -   [SelfReg](selfreg-table.md)
    -   [ServiceControl](servicecontrol-table.md)
    -   [ServiceInstall](serviceinstall-table.md)
    -   [Typelib](typelib-table.md)
    -   [Verb](verb-table.md)
    -   [!Note]  
        > Wenn ein Patch neue Inhalte zu den Tabellen [RemoveFile](removefile-table.md) oder [RemoveRegistry](removeregistry-table.md) hinzufügt, markiert Windows Installer den Patch nicht als nicht deinstallationsfähig. Der Patch kann jedoch nur deinstalliert werden, wenn die Ressource zum Entfernen des neuen Inhalts nicht bereits im ursprünglichen Installationspaket vorhanden ist. Wenn der Patch z. B. der RemoveFile-Tabelle eine neue Zeile hinzufügt, kann die entfernte Datei nicht wiederhergestellt werden, indem der Patch deinstalliert wird, wenn die Datei außerhalb der [Dateitabelle](file-table.md)ist. Die Datei muss in der Dateitabelle des ursprünglichen Pakets und den angewendeten Patches erstellt worden sein, damit der Patch deinstalliert werden kann.

         

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patchsequenzierung](sequencing-patches.md)
</dt> <dt>

[Entfernen von Patches](removing-patches.md)
</dt> <dt>

[Deinstallieren von Patches](uninstalling-patches.md)
</dt> <dt>

[Benutzerdefinierte Aktionen zum Deinstallieren von Patches](patch-uninstall-custom-actions.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 




