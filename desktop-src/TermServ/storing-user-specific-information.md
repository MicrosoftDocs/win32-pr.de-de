---
title: Speichern von benutzerspezifischen Informationen
description: Anwendungen sollten benutzerspezifische Informationen an benutzerspezifischen Speicherorten speichern, die von den globalen, auf alle Benutzer bezogenen Informationen getrennt sind.
ms.assetid: 32bd1d24-1d2e-4c0a-acdb-0cc67f275e6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c6236b7ba11a8b3149533e920b9b9413085d93
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039154"
---
# <a name="storing-user-specific-information"></a>Speichern von benutzerspezifischen Informationen

In einer Remotedesktopdienste Umgebung sollten Anwendungen benutzerspezifische Informationen an benutzerspezifischen Speicherorten speichern, getrennt von globalen Informationen, die für alle Benutzer gelten. Diese Regel gilt für Informationen, die in der Registrierung gespeichert sind, sowie für Informationen, die in Dateien gespeichert sind. Nehmen Sie im Allgemeinen nicht an, dass ein Computer einem Benutzer entspricht.

Speichert benutzerspezifische Registrierungsinformationen unter dem Registrierungsschlüssel **HKEY \_ Current \_ User** . Remotedesktopdienste lädt die persönliche Registrierungs Struktur des aktuellen Benutzers in den **aktuellen HKEY- \_ \_ Benutzer** , wenn sich der Benutzer anmeldet. Remotedesktopdienste verwaltet die Registrierung natürlich, um sicherzustellen, dass jeder angemeldete Client die richtige Benutzer Struktur unter **HKEY \_ Current \_ User** erkennt. Weitere Informationen zu Registrierungs Schlüsseln finden Sie unter [Sicherheits-und Zugriffsrechte für den Registrierungsschlüssel](/windows/desktop/SysInfo/registry-key-security-and-access-rights) und [Registrierungs](/windows/desktop/SysInfo/registry-hives)Strukturen.

Im Gegensatz dazu geben alle Benutzer den HKEY-Hive für den **\_ lokalen \_ Computer** frei. Verwenden Sie **HKEY \_ local \_ Machine** , um Computer spezifische Informationen, nicht jedoch benutzerspezifische Informationen, zu speichern.

Speichert Benutzer Einstellungsdateien oder andere benutzerspezifische Dateien im Stammverzeichnis des Benutzers oder in einem vom Benutzer angegebenen Verzeichnis. Diese Überlegungen gelten für temporäre Dateien, die zum Speichern von zwischen Informationen (z. b. zwischengespeicherte Daten) oder zum Übergeben von Daten an eine andere Anwendung verwendet werden. Benutzerspezifische temporäre Dateien müssen auch pro Benutzer gespeichert werden.

Sie können die Funktion " [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) " mit dem "CSIDL Personal"- \_ Flag verwenden, um den Speicherort des Verzeichnisses für persönliche Dateien des Benutzers zu erhalten. Sie können auch die [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) -Funktion verwenden, um den Pfad des Windows-Verzeichnisses abzurufen. In einer Remotedesktopdienste Umgebung ist das Windows-Verzeichnis für jeden Benutzer garantiert privat. Speichern Sie keine benutzerspezifischen Dateien im System Verzeichnis, z. b. in Windows oder im Programmverzeichnis, wie z. b. Programmdateien.

Um Konflikte zwischen den Informationen und Einstellungen der Benutzer zu vermeiden, sollten Anwendungen benutzerspezifische temporäre Informationen in benutzerspezifischen temporären Dateien speichern. Benutzerspezifische temporäre Dateien verhindern auch Anwendungsfehler, die durch Datei Sperr Konflikte verursacht werden. Um den Pfad zum Speichern temporärer Informationen anzugeben, verwenden Sie die [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) -Funktion.

 

 