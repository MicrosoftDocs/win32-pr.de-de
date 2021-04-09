---
title: Neue Funktion "Datei Versionsverlauf"
description: Neue Funktion "Datei Versionsverlauf"
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70aad84f4d052d6a872c7b0cfc979d0fa05cb84
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104102470"
---
# <a name="new-file-history-feature"></a>Neue Funktion "Datei Versionsverlauf"

## <a name="platform"></a>Plattform

**Clients** – Windows 8 


## <a name="description"></a>BESCHREIBUNG

Die neue Funktion "Datei Versionsverlauf" ersetzt die vorhandene Sicherungs-und Wiederherstellungs Funktion und bietet Schutz für Benutzer Dateien, die in Benutzer Bibliotheken gespeichert sind. Es wird ein Satz von APIs bereitgestellt, mit denen Entwicklerprogramm gesteuert den Datei Versionsverlauf aktivieren und ein bestimmtes Speicher Ziel auswählen können. Die Dokumentation für diese APIs ist auf MSDN verfügbar.

Dies kann sich auf Workflows im Zusammenhang mit Datenschutz und Dokumentation auswirken, die von der Windows-Sicherung und-Wiederherstellung abhängen.

Es wird nicht empfohlen, beide Features gleichzeitig zu verwenden. Der Datei Versionsverlauf überprüft, ob ein Sicherungs Zeitplan vorhanden ist, und ist aktiv. Wenn ein Sicherungs Zeitplan gefunden wird, kann er von Benutzern nicht eingeschaltet werden. In diesem Fall müssen Benutzer, die den Datei Versionsverlauf verwenden möchten, den Windows-Sicherungs Zeitplan löschen.

## <a name="manifestation"></a>Ausstrahlung

Workflows können unterbrochen werden, und die Dokumentation für die vorherige Methode zum Zugreifen auf das Windows-Sicherungs-und Wiederherstellungs Feature muss aktualisiert werden, um diese Änderungen widerzuspiegeln.

## <a name="solution"></a>Lösung

Überarbeiten Sie apps, die Workflows enthalten, die durch das neue Feature "Datei Versionsverlauf" beeinträchtigt werden, um Konflikte zu entfernen und den neuen Satz von APIs zu integrieren.

## <a name="tests"></a>Tests

Die-API ermöglicht Entwicklern, zu bestimmen, ob der Datei Versionsverlauf aktiviert ist.

 

 




