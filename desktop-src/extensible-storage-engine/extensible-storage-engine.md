---
description: 'Weitere Informationen finden Sie hier: Extensible Storage Engine'
title: Erweiterbare Speicher-Engine
TOCTitle: Extensible Storage Engine
ms:assetid: 5c485eff-4329-4dc1-aa45-fb66e6554792
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269259(v=EXCHG.10)
ms:contentKeyID: 32765561
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 0ef85de696f52d2220c11b05ed7ada76a70df871
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041915"
---
# <a name="extensible-storage-engine"></a>Erweiterbare Speicher-Engine


_**Gilt für:** Windows | Windows Server_

## <a name="extensible-storage-engine"></a>Erweiterbare Speicher-Engine

Beim Extensible Storage Engine (ESE) handelt es sich um eine erweiterte ISAM (Sequential Access Method)-Speichertechnologie. ESE ermöglicht Anwendungen das Speichern und Abrufen von Daten aus Tabellen mit indizierter oder sequenzieller Cursor Navigation. Es unterstützt denormalisierte Schemas, einschließlich Breite Tabellen mit vielen sparsespalten, mehrwertigen Spalten und sparsespalten und umfangreichen Indizes. Dadurch können Anwendungen einen konsistenten Daten Zustand mithilfe von transaktiven Datenaktualisierungen und-Abruf nutzen. Ein Mechanismus zur Wiederherstellung von abstürzen wird bereitgestellt, damit die Datenkonsistenz auch bei einem Systemabsturz gewahrt bleibt. Es bietet ACID-Transaktionen (atomarische konsistente isolierte dauerhafte Transaktionen) über Daten und Schemas über ein Write-Ahead-Protokoll und ein Snapshot-Isolations Modell. Transaktionen in ESE sind stark gleichzeitig, sodass ESE für Server Anwendungen nützlich ist. Daten werden zwischengespeichert, um den Leistungsdaten Zugriff zu maximieren. Außerdem ist es sehr einfach, was für Anwendungen nützlich ist, die in zusätzlichen Rollen eingesetzt werden.

ESE dient der Verwendung in Anwendungen, die eine schnelle und/oder einfache strukturierte Datenspeicherung erfordern, bei der der Rohdatendatei-Zugriff oder die Registrierung die Indizierungs-oder Datengrößen Anforderungen der Anwendung nicht unterstützt.

Sie wird von Anwendungen verwendet, die nie mehr als 1 Megabyte an Daten speichern und in Anwendungen mit Datenbanken verwendet werden, die in Extremfällen über 1 Terabyte und in der Regel über 50 Gigabytes verfügen.

Diese Dokumentation richtet sich an Entwickler, die mit C und C++ vertraut sind, sowie grundlegende Datenbankkonzepte wie Tabellen, Spalten, Indizes, Wiederherstellungen und Transaktionen. Die einzige Zugriffsmethode für ESE ist die C-API, die in dieser Dokumentation beschrieben wird.

Die erweiterbare Speicher-Engine ist eine Windows-Komponente, die in Windows 2000 eingeführt wurde. Nicht alle Features oder APIs sind in allen Versionen der Windows-Betriebssysteme verfügbar.

ESE bietet eine Benutzermodus-Speicher-Engine, die Daten in flachen Binärdateien verwaltet, auf die über die Windows-APIs zugegriffen werden kann. Der Zugriff auf ESE erfolgt über eine DLL, die direkt in den Prozess der Anwendung geladen wird. Es sind keine Remote Zugriffsmethoden erforderlich, die von der Datenbank-Engine selbst bereitgestellt werden. Obwohl ESE über keine Remote-oder prozessübergreifende Zugriffsmethode verfügt, können die verwendeten Datendateien mithilfe von SMB (Server Message Block) über die Windows-APIs Remote bereitgestellt werden, dies wird jedoch nicht empfohlen.

**Hinweis**  Windows XP 64-Bit Edition ist mit Windows Server 2003 identisch, um den unterstützten ESE-Funktions Satz zu bestimmen.

### <a name="notes"></a>Notizen

ESE wurde früher als Joint Engine Technology (Jet) Blue bezeichnet. häufig wird der Begriff "Jet Blue" oder "Jet" mit dem Begriff "ESE" außerhalb dieser Dokumentation austauschbar verwendet. Es gibt jedoch tatsächlich zwei vollständig getrennte Implementierungen der Jet-API mit dem Namen Jet Blue und Jet Red. Der Begriff "Jet" wird häufig auch verwendet, um auf Jet Red zu verweisen. dabei handelt es sich um die Datenbank-Engine, die mit Microsoft Office Access verwendet wird. Die beiden Jet-Implementierungen unterscheiden sich vollständig, werden separat gewartet, haben eine sehr andere Funktions Reihe und sind nicht austauschbar. In der ESE-Dokumentation bezieht sich "Jet" auf die ESE-oder Jet-API, wenn Sie von ESE implementiert wird. Alle Verweise auf das Jet Red werden immer explizit als "Jet Red" bezeichnet.

### <a name="in-this-section"></a>In diesem Abschnitt

[Extensible Storage Engine-Referenz](./extensible-storage-engine-reference.md)
