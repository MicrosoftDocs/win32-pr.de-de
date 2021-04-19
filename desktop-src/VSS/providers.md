---
description: Anbieter verwalten laufende Volumes und erstellen die Schatten Kopien von Ihnen bei Bedarf.
ms.assetid: 4e6b46b0-df9e-4458-b0ac-e237d7656337
title: Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb336dbb51fcbd715ea236ecdc0c62d81daf29d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367872"
---
# <a name="providers"></a>Anbieter

[*Anbieter*](vssgloss-p.md) verwalten laufende Volumes und erstellen die Schatten Kopien von Ihnen bei Bedarf.

Als Antwort auf eine Anforderung eines Anforderers generiert ein Anbieter COM-Ereignisse, um Anwendungen über eine kommende Schatten Kopie zu signalisieren, und erstellt und verwaltet diese Kopie, bis Sie nicht mehr benötigt wird.

Während eine Schatten Kopie vorhanden ist, erstellt der Anbieter eine Umgebung, in der effektiv zwei unabhängige Kopien eines Volumes vorhanden sind, auf die Schatten kopiert wurde: ein Datenträger, der als normal verwendet und aktualisiert wird, der andere eine Kopie, die Festplatte ist und für die Sicherung stabil ist.

Während ein Standardanbieter als Teil von Windows bereitgestellt wird, können andere Anbieter eigene Implementierungen bereitstellen, die für Ihre eigene Speicherhardware und Ihre Software Angebote optimiert sind.

Aus Sicht eines Endbenutzers oder eines Sicherungs-/wiederherstellungsentwicklers haben alle Anbieter die gleiche Schnittstelle (siehe Auswählen von [Anbietern](selecting-providers.md)).

Alle Anbieter müssen in der Lage sein, folgende Aktionen durchzuführen:

-   Fangen Sie e/a-Anforderungen zwischen dem Dateisystem und dem zugrunde liegenden Massen Speichersystem ab.
-   Erfassen und Abrufen des Status eines Volumes zum Zeitpunkt der Schatten Kopie, wobei eine "Zeitpunkt"-Ansicht der Dateien auf dem Datenträger beibehalten wird und keine partiellen e/a-Vorgänge in seinem Zustand reflektiert werden.
-   Verwenden Sie diese "Point-in-Time"-Ansicht, um (minimal für VSS-fähige Anwendungen) ein virtuelles Volume verfügbar zu machen, das die Schatten kopierten Daten enthält.

Abhängig davon, wie dies geschieht, kann ein Anbieter einen von drei Typen aufweisen:

-   [System Anbieter](#system-provider)
-   [Software Anbieter](#software-providers)
-   [Hardware Anbieter](#hardware-providers)

## <a name="system-provider"></a>System Anbieter

Ein Schattenkopieanbieter, der [*Systemanbieter*](vssgloss-s.md), wird als Standard Teil einer Windows-Betriebssystem Installation bereitgestellt. Derzeit ist der Systemanbieter eine bestimmte Instanz eines Softwareanbieters. Dies kann sich jedoch in Zukunft ändern.

Um einen "Zeitpunkt"-Ansicht eines in der Schatten Kopie enthaltenen Volumes beizubehalten, verwendet der Systemanbieter eine Kopiermethode. Kopien der Sektoren auf dem Datenträger, die seit dem Beginn der Erstellung der Schatten Kopie geändert wurden, werden in einem Speicherbereich für Schatten Kopien gespeichert.

Daher kann der Systemanbieter das Live Volume verfügbar machen, das in den Normalfall geschrieben und daraus gelesen werden kann, und die "diffs" auf die Daten des Livevolumes anwenden, um die fixierten Daten der Schatten Kopie effektiv verfügbar zu machen.

Für den Systemanbieter muss sich der Schattenkopie-Speicherbereich auf einem NTFS-Volume befinden. Das Volume, das als Schatten gesichert werden soll, muss kein NTFS-Volume sein, aber mindestens ein auf dem System eingebundenes Volume muss ein NTFS-Volume sein.

## <a name="software-providers"></a>Software Anbieter

Software Schatten Kopie-Anbieter fangen e/a-Anforderungen in einer Software Schicht zwischen dem Dateisystem und der Volume Manager-Software auf und verarbeiten Sie. Diese Anbieter werden als benutzermodusdll-Komponente und mindestens ein Gerätetreiber im Kernelmodus implementiert, in der Regel (aber nicht unbedingt) ein Speicher Filtertreiber. Die Erstellung dieser Schatten Kopien erfolgt in der Software.

Ein Software Schatten Kopie-Anbieter muss eine "Point-in-Time"-Ansicht eines Volumes verwalten, indem er auf einen Satz von Dateien zugreifen kann, mit dem der Volumestatus vor der Schatten Kopie korrekt neu erstellt werden kann. Ein Beispiel hierfür ist die Copy-on-write-Technik des Systemanbieters.

Allerdings gelten für VSS keine Einschränkungen hinsichtlich der Technik, die Softwareanbieter zum Erstellen und Verwalten von Schatten Kopien verwenden. Drittanbieter können Ihre Softwareanbieter so implementieren, dass Sie Ihren Anforderungen entsprechen.

Außerdem bietet VSS Unterstützung für einen Großteil der Funktionen von Software Schatten Kopien, wie z. b. das Definieren des Zeitpunkts, das Synchronisieren und leeren von Daten, das Bereitstellen einer gemeinsamen Schnittstelle für Sicherungs Anwendungen und die Verwaltung der Schatten Kopie.

Ein Softwareanbieter ist definitionsgemäß auf eine größere Anzahl von Speicher Plattformen als ein Hardware Anbieter anwendbar und sollte in der Lage sein, mit Basis Datenträgern oder logischen Volumes gleich gut zu arbeiten. Diese Generalität stellt die Leistung dar, die möglicherweise durch Implementieren von Schatten Kopien in der Hardware verfügbar ist, und nutzt keine herstellerspezifischen Volumen Erfassungs-oder Datei Spiegelungs Features.

## <a name="hardware-providers"></a>Hardware Anbieter

Hardware Schattenkopieanbieter fangen e/a-Anforderungen aus dem Dateisystem auf Hardwareebene aus, indem Sie in Verbindung mit einem Hardware Speicher Adapter oder-Controller arbeiten. Das Erstellen der Schatten Kopie wird von einem Host Adapter, einem Speichergerät oder einem RAID-Controller außerhalb des Betriebssystems ausgeführt.

Diese Anbieter werden als benutzermodusdll-Komponente implementiert, die mit der Hardware kommuniziert, von der die Schattenkopiedaten verfügbar gemacht werden. Daher müssen Hardware Schattenkopieanbieter möglicherweise andere Kernelmoduskomponenten anrufen oder erstellen.

Hardware Anbieter machen VSS-Schatten Kopien ganzer Datenträger oder logischer Einheiten (Logical Units, LUNs) verfügbar. Der Anforderer behandelt weiterhin Schatten Kopien von Volumes. die gesamte Zuordnung von Volumes zu Datenträgern wird intern von VSS verarbeitet. Von Hardwareanbietern von Volumes, die sich auf dynamischen Datenträgern befinden, erstellte Schatten Kopien haben eine bestimmte Anforderung: Sie können nicht auf das gleiche System importiert werden. Sie müssen austauschen erstellt und auf einem zweiten System importiert werden.

Während ein Hardware Schatten Kopie-Anbieter VSS-Funktionen verwendet, die den Zeitpunkt definieren, die Datensynchronisierung ermöglicht, die Schatten Kopie verwaltet und eine gemeinsame Schnittstelle mit Sicherungs Anwendungen bereitstellt, gibt VSS nicht den zugrunde liegenden Mechanismus an, mit dem der Hardware Anbieter Schatten Kopien erstellt und verwaltet.

 

 



