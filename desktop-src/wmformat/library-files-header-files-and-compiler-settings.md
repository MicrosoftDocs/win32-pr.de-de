---
title: Bibliotheksdateien, Header Dateien und Compilereinstellungen
description: Bibliotheksdateien, Header Dateien und Compilereinstellungen
ms.assetid: 7563bb3a-7bea-4e0c-8205-a16b276c8d1e
keywords:
- Windows Media-Format-SDK, DRM-Bibliotheksdateien
- Windows Media-Format-SDK, Bibliotheksdateien
- Windows Media-Format-SDK, DRM-Header Dateien
- Windows Media-Format-SDK, Header Dateien
- Windows Media-Format-SDK, DRM-Compilereinstellungen
- Windows Media-Format-SDK, Compilereinstellungen
- Digital Rights Management (DRM), Bibliotheksdateien
- DRM-Dateien (Digital Rights Management), Bibliotheksdateien
- Digital Rights Management (DRM), Header Dateien
- DRM-Dateien (Digital Rights Management), Header Dateien
- Digital Rights Management (DRM), Compilereinstellungen
- DRM (Digital Rights Management), Compilereinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b0b10ea03cc08d5b689b74f9c647f7d0138fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100739"
---
# <a name="library-files-header-files-and-compiler-settings"></a>Bibliotheksdateien, Header Dateien und Compilereinstellungen

Die Programmier Komponenten der erweiterten APIs des Windows Media DRM-Clients werden in der Header Datei "wmdrmsdk. h" definiert und in den Bibliotheken "wmdrmsdk. lib" und "mfuuid. lib" implementiert.

Für einige Funktionen der erweiterten APIs des Windows Media DRM-Clients ist es erforderlich, dass Sie eine geschützte Bibliothek von Microsoft erhalten. Diese Bibliothek, die in dieser Dokumentation als stubbibliothek bezeichnet wird, ist für den Empfänger spezifisch und gibt die Anwendungs Sicherheitsstufe für Ihre Anwendungen an. Die Stub-Bibliothek ersetzt wmdrmsdk. lib; Sie sollten niemals eine Verknüpfung mit beiden herstellen.

**Hinweis** Die DRM-stubbibliothek ist von der stubbibliothek getrennt, die vom Rest des Windows Media Format SDK verwendet wird, aber mit der gleichen Methode lizenziert ist.

**Hinweis** Die DRM-stubbibliothek muss nach der Bibliotheksdatei msvcrt. lib mit Ihrer Anwendung verknüpft werden, um Linker-Fehler zu vermeiden.

Die Stub-Bibliothek enthält ein eingebettetes Zertifikat, das von Microsoft gesperrt werden kann, wenn Sie die Geschäftsbedingungen des Lizenzvertrags nicht einhalten.

Bestimmte Methoden, die die stubbibliothek erfordern, werden in der-Dokumentation bezeichnet. Wenn Sie versuchen, eine solche Methode ohne Verknüpfung mit der stubbibliothek zu verwenden, wird ein Fehler vom Typ "NS \_ E \_ DRM- \_ stublib erforderlich" zurückgegeben \_ .

Das DRM-Subsystem kann nicht in einem Debugbuild verwendet werden. Wenn dies versucht wird, geben Methoden der API den Fehler "NS \_ E \_ DRM- \_ Debugging \_ nicht \_ zulässig" zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Einstieg**](drm-getting-started.md)
</dt> <dt>

[**Bibliotheksdateien und Compilereinstellungen**](library-files-and-compiler-settings.md)
</dt> <dt>

[**Abrufen der erforderlichen DRM-Bibliothek**](obtaining-the-required-drm-library.md)
</dt> </dl>

 

 




