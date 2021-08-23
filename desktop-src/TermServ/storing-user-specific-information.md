---
title: Speichern von benutzerspezifischen Informationen
description: Anwendungen sollten benutzerspezifische Informationen an benutzerspezifischen Speicherorten speichern, die von den globalen, auf alle Benutzer bezogenen Informationen getrennt sind.
ms.assetid: 32bd1d24-1d2e-4c0a-acdb-0cc67f275e6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aa8e60ec89c3f9d161941d01e1aa241f0bb0245d0f5b57b1cc362dd836bdb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000430"
---
# <a name="storing-user-specific-information"></a>Speichern von benutzerspezifischen Informationen

In einer Remotedesktopdienste-Umgebung sollten Anwendungen benutzerspezifische Informationen an benutzerspezifischen Speicherorten speichern, getrennt von globalen Informationen, die für alle Benutzer gelten. Diese Regel gilt für in der Registrierung gespeicherte Informationen sowie für in Dateien gespeicherte Informationen. Gehen Sie im Allgemeinen nicht davon aus, dass ein Computer einem Benutzer entspricht.

Store benutzerspezifische Registrierungsinformationen unter dem **Registrierungsschlüssel HKEY \_ CURRENT \_ USER.** Remotedesktopdienste lädt die persönliche Registrierungsstruktur des aktuellen Benutzers in **HKEY \_ CURRENT \_ USER,** wenn sich der Benutzer anmeldet. Natürlich verwaltet Remotedesktopdienste registrierung, um sicherzustellen, dass jeder der angemeldeten Clients die richtige Benutzerstruktur unter **HKEY \_ CURRENT USER \_ erkennt.** Weitere Informationen zu Registrierungsschlüsseln finden Sie unter [Sicherheit und](/windows/desktop/SysInfo/registry-key-security-and-access-rights) Zugriffsrechte für Registrierungsschlüssel und [Hives-Registrierung.](/windows/desktop/SysInfo/registry-hives)

Im Gegensatz dazu verwenden alle Benutzer die **HKEY \_ LOCAL \_ MACHINE-Struktur.** Verwenden **Sie HKEY \_ LOCAL \_ MACHINE,** um computerspezifische Informationen und keine benutzerspezifischen Informationen zu speichern.

Store Benutzereinstellungsdateien oder andere benutzerspezifische Dateien im Stammverzeichnis des Benutzers oder in einem benutzerspezifischen Verzeichnis. Dieser Aspekt gilt für temporäre Dateien, die zum Speichern von Zwischeninformationen (z. B. zwischengespeicherte Daten) oder zum Übergeben von Daten an eine andere Anwendung verwendet werden. Benutzerspezifische temporäre Dateien müssen auch benutzerspezifisch gespeichert werden.

Sie können die [**SHGetSpecialFolderLocation-Funktion**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) mit dem CSIDL PERSONAL-Flag verwenden, um den Speicherort des persönlichen \_ Dateiverzeichnisses des Benutzers zu erhalten. Sie können auch die [**GetWindowsDirectory-Funktion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) verwenden, um den Pfad des Windows abzurufen. In einer Remotedesktopdienste ist das Windows für jeden Benutzer garantiert privat. Speichern Sie keine benutzerspezifischen Dateien im Systemverzeichnis, z. B. WINDOWS oder programmverzeichnis, z. B. Programme.

Um Konflikte zwischen benutzerspezifischen Informationen und Einstellungen zu vermeiden, sollten Anwendungen temporäre Informationen pro Benutzer in benutzerspezifischen temporären Dateien speichern. Benutzerspezifische temporäre Dateien verhindern auch Anwendungsfehler, die durch Dateisperrkonflikte verursacht werden. Verwenden Sie die [**GetTempPath-Funktion,**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) um den Pfad zum Speichern temporärer Informationen anzugeben.

 

 