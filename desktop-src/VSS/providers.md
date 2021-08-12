---
description: Anbieter verwalten ausgeführte Volumes und erstellen die Schattenkopien von ihnen bei Bedarf.
ms.assetid: 4e6b46b0-df9e-4458-b0ac-e237d7656337
title: Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9e098981c6246392fef75f717b1d7676df1aa134e4faef3e436ee8b3eb537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591327"
---
# <a name="providers"></a>Anbieter

[*Anbieter*](vssgloss-p.md) verwalten ausgeführte Volumes und erstellen die Schattenkopien von ihnen bei Bedarf.

Als Reaktion auf eine Anforderung von einem Anfordernden generiert ein Anbieter COM-Ereignisse, um Anwendungen einer kommenden Schattenkopie zu signalisieren. Anschließend erstellt und verwaltet er diese Kopie, bis sie nicht mehr benötigt wird.

Während eine Schattenkopie vorhanden ist, erstellt der Anbieter eine Umgebung, in der es effektiv zwei unabhängige Kopien eines Volumes gibt, die schattenkopiert wurden: eine der ausgeführten Datenträger, die wie gewohnt verwendet und aktualisiert wird, die andere eine Kopie, die für die Sicherung fest und stabil ist.

Während ein Standardanbieter als Teil von Windows bereitgestellt wird, können andere Anbieter ihre eigenen Implementierungen zur Verfügung stellen, die für ihre eigenen Speicherhardware- und Softwareangebote optimiert sind.

Aus Sicht eines Endbenutzers oder Entwicklers einer Sicherungs-/Wiederherstellungsanwendung verfügen alle Anbieter über die gleiche Schnittstelle (siehe [Auswählen von Anbietern](selecting-providers.md)).

Alle Anbieter müssen in der Lage sein, Folgendes zu tun:

-   Abfangen von E/A-Anforderungen zwischen dem Dateisystem und dem zugrunde liegenden Massenspeichersystem.
-   Erfassen und abrufen Sie den Status eines Volumes zum Zeitpunkt der Schattenkopie, und verwalten Sie dabei eine "Zeitpunkt"-Ansicht der Dateien auf dem Datenträger, ohne dass partielle E/A-Vorgänge im Zustand widergespiegelt werden.
-   Verwenden Sie diese "Zeitpunktansicht", um (minimal für VSS-fähige Anwendungen) ein virtuelles Volume verfügbar zu machen, das die kopierten Schattendaten enthält.

Je nachdem, wie dies erfolgt, kann ein Anbieter einen von drei Typen haben:

-   [Systemanbieter](#system-provider)
-   [Softwareanbieter](#software-providers)
-   [Hardwareanbieter](#hardware-providers)

## <a name="system-provider"></a>Systemanbieter

Ein Schattenkopieanbieter, der [*Systemanbieter,*](vssgloss-s.md)wird als Standardteil einer Betriebssysteminstallation Windows bereitgestellt. Derzeit ist der Systemanbieter eine bestimmte Instanz eines Softwareanbieters. Dies kann sich jedoch in Zukunft ändern.

Um eine "Zeitpunkt"-Ansicht eines Volumes zu verwalten, das in der Schattenkopie enthalten ist, verwendet der Systemanbieter eine Kopier-bei-Schreib-Technik. Kopien der Sektoren auf dem Datenträger, die seit dem Beginn der Erstellung der Schattenkopie geändert wurden (als "Diffs" bezeichnet), werden in einem Schattenkopiespeicherbereich gespeichert.

Daher kann der Systemanbieter das Live-Volume verfügbar machen, auf das normalerweise geschrieben und gelesen werden kann, und die "Unterschiede" auf die Daten des Live-Volumes anwenden, um die fixierten Daten der Schattenkopie effektiv verfügbar zu machen.

Für den Systemanbieter muss sich der Schattenkopie-Speicherbereich auf einem NTFS-Volume befinden. Das Volume, das als Schatten gesichert werden soll, muss kein NTFS-Volume sein, aber mindestens ein auf dem System eingebundenes Volume muss ein NTFS-Volume sein.

## <a name="software-providers"></a>Softwareanbieter

Softwareschattenkopieanbieter fangen E/A-Anforderungen in einer Softwareschicht zwischen dem Dateisystem und der Volume-Manager-Software ab und verarbeiten sie. Diese Anbieter werden als DLL-Komponente im Benutzermodus und mindestens ein Gerätetreiber im Kernelmodus implementiert, in der Regel (aber nicht notwendigerweise) als Speicherfiltertreiber. Die Erstellung dieser Schattenkopien erfolgt in Software.

Ein Softwareschattenkopieanbieter muss eine Point-in-Time-Ansicht eines Volumes verwalten, indem er Zugriff auf eine Gruppe von Dateien hat, mit denen der Volumestatus vor der Schattenkopie genau neu erstellt werden kann. Ein Beispiel hierfür ist die Kopier-bei-Schreib-Technik des Systemanbieters.

VsS legt jedoch keine Einschränkungen hinsichtlich der Technik fest, die Softwareanbieter zum Erstellen und Verwalten von Schattenkopien verwenden, und Drittanbieter können ihre Softwareanbieter nach Ihren Anforderungen implementieren.

Darüber hinaus bietet VSS Unterstützung für einen großen Teil der Funktionalität von Softwareschattenkopieanbietern, z. B. das Definieren des Zeitpunkts, die Datensynchronisierung und -leerung, die Bereitstellung einer gemeinsamen Schnittstelle für Sicherungsanwendungen und die Verwaltung der Schattenkopie.

Ein Softwareanbieter ist definitionsgemäß auf eine größere Bandbreite von Speicherplattformen anwendbar als ein Hardwareanbieter und sollte in der Lage sein, mit Basisdatenträgern oder logischen Volumes gleichermaßen gut zu arbeiten. Diese Allgemeinheit wirkt sich auf die Leistung aus, die durch die Implementierung von Schattenkopien in der Hardware verfügbar sein kann, und nutzt keine anbieterspezifischen Volumeerfassungs- oder Dateispiegelungsfeatures.

## <a name="hardware-providers"></a>Hardwareanbieter

Hardwareschattenkopieanbieter fangen E/A-Anforderungen vom Dateisystem auf Hardwareebene ab, indem sie in Verbindung mit einem Hardwarespeicheradapter oder Controller arbeiten. Die Erstellung der Schattenkopie wird von einem Hostadapter, einem Speichergerät oder einem RAID-Controller außerhalb des Betriebssystems ausgeführt.

Diese Anbieter werden als DLL-Komponente im Benutzermodus implementiert, die mit der Hardware kommuniziert, die die Schattenkopiedaten verfügbar macht. Daher müssen Hardwareschattenkopieanbieter möglicherweise andere Kernelmoduskomponenten aufrufen oder erstellen.

Hardwareanbieter machen VSS-Schattenkopien von gesamten Datenträgern oder logischen Einheiten (LUNs) verfügbar. Anfordernde behandeln weiterhin Schattenkopien von Volumes. die Zuordnung von Volume zu Datenträger wird intern von VSS verarbeitet. Schattenkopien, die von Hardwareanbietern von Volumes erstellt werden, die sich auf dynamischen Datenträgern befinden, haben eine bestimmte Anforderung: Sie können nicht in dasselbe System importiert werden. Sie müssen transportierbar erstellt und in ein zweites System importiert werden.

Während ein Hardwareschattenkopieanbieter VSS-Funktionen nutzt, die den Zeitpunkt definieren, die Datensynchronisierung ermöglichen, die Schattenkopie verwalten und eine gemeinsame Schnittstelle mit Sicherungsanwendungen bieten, gibt VSS nicht den zugrunde liegenden Mechanismus an, mit dem der Hardwareanbieter Schattenkopien erstellt und verwaltet.

 

 



