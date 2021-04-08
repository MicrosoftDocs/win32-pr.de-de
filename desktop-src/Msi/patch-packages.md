---
description: Eine Windows Installer Patch (MSP-Datei) ist eine Datei, die zum Bereitstellen von Updates für Windows Installer Anwendungen verwendet wird.
ms.assetid: f59736d7-0b5a-466c-ab60-f210ccccb07f
title: Patch-Pakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b4bb5b7e182c8118f5a40c45be440784b92099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755609"
---
# <a name="patch-packages"></a>Patch-Pakete

Eine Windows Installer Patch (MSP-Datei) ist eine Datei, die zum Bereitstellen von Updates für Windows Installer Anwendungen verwendet wird. Der Patch ist ein eigenständiges Paket, das alle zum Aktualisieren der Anwendung erforderlichen Informationen enthält. Ein Patchpaket (MSP-Datei) kann für die gesamte aktualisierte Anwendung wesentlich kleiner als das Windows Installer Paket (MSI-Datei) sein. Weitere Informationen zur Bereitstellung kleinerer Updates für Anwendungen finden Sie unter [verringern der Patchgröße](reducing-patch-size.md).

Ein Patchpaket enthält die eigentlichen Updates der Anwendung und beschreibt, welche Versionen der Anwendung den Patch empfangen können. Patches enthalten mindestens zwei Daten Bank Transformationen. Durch eine Transformation werden die Informationen in der Installations Datenbank der Anwendung aktualisiert. Die andere Transformation fügt Informationen hinzu, die vom Installationsprogramm zum Patchen von Dateien verwendet werden. Das Installationsprogramm verwendet die Informationen, die von den Transformationen bereitgestellt werden, um Patchdateien anzuwenden, die im CAB-Datei Datenstrom des Patchpakets gespeichert werden. Ein Patchpaket verfügt über keine Datenbank wie ein Installationspaket (MSI-Datei).

Ab Windows Installer Version 3,0 können Patchpakete Informationen enthalten, die die patchsequenz für den Patch relativ zu anderen Updates in der [msipatchsequence](msipatchsequence-table.md) -Tabelle und zusätzliche beschreibende Informationen in der [MsiPatchMetadata](msipatchmetadata-table.md) -Tabelle beschreiben.

Benutzer können Anwendungen und Updates über ein Netzwerkadministrator Image installieren. Obwohl Patchpakete auf administrative Installationen angewendet werden können, besteht die empfohlene Methode zur Bereitstellung von Updates darin, dass Benutzer die ursprüngliche Anwendung installieren und dann die Patches auf die lokale Instanz der Anwendung auf Ihrem Computer anwenden. Dies sorgt dafür, dass die Benutzer mit dem administrativen Abbild synchronisiert werden. Wenn ein Patch auf die administrative Installation angewendet wird, müssen sich alle Clients dieser administrativen Installation wiederholen und die Anwendung neu installieren, um das Update zu erhalten. Bis ein Benutzer eine Wiederholung und Neuinstallation durchläuft, kann der Benutzer die Installation nicht mehr über die gepatchte administrative Installation installieren.

Ab Windows Installer 3,0 können nicht Administratoren Patches auf pro Benutzer verwaltete Anwendungen anwenden, nachdem der Patch von einem Administrator als vertrauenswürdig eingestuft wurde. Weitere Informationen hierzu finden Sie unter [Patching Per-User Managed Applications](patching-per-user-managed-applications.md). Eine andere Methode ist das Patchen von Benutzerkonten mit den geringsten Rechten.

> [!Note]  
> Wenn die [allowlockdownpatch](allowlockdownpatch.md) -Richtlinie festgelegt wurde, können Benutzer ohne Administratorrechte einen Patch auf eine vorhandene Anwendung anwenden, während eine Installation mit erhöhten Rechten ausgeführt wird. Diese Methode wird nicht empfohlen, da Sie ermöglicht, dass nicht vertrauenswürdige Patches auf eine Anwendung angewendet werden, die mit erhöhten Rechten ausgeführt werden kann.

 

Patchpakete bestehen aus den folgenden Teilen: Weitere Informationen zur Erstellung von Patch-Paketen finden Sie unter [Erstellen eines Patchpakets](creating-a-patch-package.md).

## <a name="summary-information-stream"></a>Zusammenfassungs Informationsdaten Strom

Der Datenstrom für Zusammenfassungs Informationen des Patchpakets enthält Informationen zur Identität und zum Zweck des Patches.

Der Datenstrom für Zusammenfassungs Informationen enthält mindestens Folgendes:

-   Eine GUID, die den Patch eindeutig identifiziert. Die GUID für diesen Patch wird mit einer Liste von GUIDs für frühere Patches angehängt, die durch diesen Patch ersetzt werden.
-   Eine durch Semikolons getrennte Liste von Produktcodes für gültige Ziele für diesen Patch.
-   Eine durch Semikolons getrennte Liste der Namen der Transformations unter Speicher in der Reihenfolge, in der Sie verarbeitet werden sollen.
-   Eine durch Semikolons getrennte Liste der Quellen für diesen Patch.

## <a name="transform-substorage"></a>Transformieren von unter Speicher

Ein Patchpaket enthält Transformationen, mit denen Dateien, Registrierungseinträge, Benutzeroberflächen und Anpassungen hinzugefügt oder entfernt werden können. Transformationen sind als substorages im Paket enthalten. Ein Patchpaket enthält zwei Transformationen für jede Zieldatenbank. Eine Transformation ist die tatsächliche Aktualisierung der Installations Datenbank und wird anhand der Unterschiede zwischen den ursprünglichen und aktualisierten Images des Installationspakets generiert. Die andere Transformation fügt Einträge zu den Tabellen [Patch](patch-table.md), [patchpackage](patchpackage-table.md), [Media](media-table.md), [InstallExecuteSequence](installexecutesequence-table.md)und [AdminExecuteSequence](adminexecutesequence-table.md) hinzu. Informationen in der unter Speicher werden mit einem bestimmten [**UpgradeCode**](upgradecode.md), [**ProductCode**](productcode.md), [**ProductVersion**](productversion.md)und [**productlanguage**](productlanguage.md)verknüpft. Ein Patchpaket, das auf mehrere Ziele angewendet werden kann, enthält mehr als ein paar dieser Transformationen.

## <a name="cabinet-file-stream"></a>CAB-Datei Datenstrom

Der CAB-Datei Datenstrom, der in einem Patch enthalten ist, kann diese Dateitypen enthalten:

-   Patchdateien mit den Informationen, die erforderlich sind, um die alte Version der Datei in die neue Version zu ändern. Eine einzelne Patchdatei kann verwendet werden, um eine oder mehrere alte Versionen einer Datei zu aktualisieren.
-   Zusätzliche Dateien, die der Anwendung hinzugefügt werden, die nicht in der alten Version vorhanden sind.
-   Eine gesamte Ersetzungs Datei. In den seltenen Fällen, in denen die neue Version einer Datei kleiner ist als der Patch, der zum Aktualisieren der alten Version dieser Datei erforderlich ist, kann die neue Datei vollständig eingefügt werden. Dabei handelt es sich um neue Dateien, die über Ihre alten Versionen installiert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Patchpakets](creating-a-patch-package.md)
</dt> </dl>

 

 



