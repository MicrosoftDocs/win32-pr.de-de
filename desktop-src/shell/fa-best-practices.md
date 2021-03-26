---
description: Die folgende Liste wird empfohlen, wenn Sie mit Dateizuordnungen arbeiten.
title: Bewährte Methoden für Dateizuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f49c1df6d145c32b8fcbdf70462b30f14f51b3d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525796"
---
# <a name="best-practices-for-file-associations"></a>Bewährte Methoden für Dateizuordnungen

Die folgende Liste wird empfohlen, wenn Sie mit Dateizuordnungen arbeiten.

-   [Dateizuordnungen nicht aus der Registrierung kopieren](#do-not-copy-file-associations-from-the-registry)
-   [Vermeiden Sie, wenn möglich, Hard-Coding Pfade in der Registrierung.](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [Erweitern Sie immer erweiternde Zeichen folgen in Anführungszeichen](#always-wrap-expanding-strings-in-quotation-marks)
-   ["AutoPlay/AutoRun" nicht mit Dateizuordnungen verwechseln](#do-not-confuse-autoplayautorun-with-file-associations)
-   [Verwechseln Sie die Internet Explorer-MIME-Datenbank nicht mit Dateizuordnungen.](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [Ordnungsgemäß formatierte und versionierte ProgIDs verwenden](#use-properly-formed-and-versioned-progids)
-   [Verwenden Sie keine kurzen Dateinamen Erweiterungen.](#do-not-use-short-file-name-extensions)
-   [Registrieren neuer Dateitypen in der IANA-MIME-Datenbank](#register-new-file-types-in-the-iana-mime-database)
-   [Registrieren beim Windows-Webdienst für Dateizuordnungen](#sign-up-with-the-windows-web-service-for-file-associations)
-   [Zugehörige Themen](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a>Dateizuordnungen nicht aus der Registrierung kopieren

Es wird empfohlen, dass Sie keine vorhandenen Dateizuordnungen aus der Registrierung kopieren. Dies führt häufig zu der Propagierung von unzureichend formatierten Dateizuordnungen. Stattdessen sollten Sie die unter [Beispielszenario für Datei](fa-sample-scenarios.md)Zuordnungen beschriebenen Schritte ausführen.

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a>Vermeiden Sie, wenn möglich, Hard-Coding Pfade in der Registrierung.

Ebenso wie hart codierte Pfade in Programmen Probleme verursachen können, können hart Codierungs Pfade in der Registrierung zu Problemen führen. Stattdessen sollten Sie Registrierungs Erweiterungs Zeichenfolgen (reg \_ Expand \_ SZ) verwenden, um ggf. Pfad Unabhängigkeit bereitzustellen. Anstatt diese Methode zu verwenden, verwenden Sie z. b. Folgendes:

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = C:\WINNT\hta.exe,1
```

Verwenden Sie diese Methode:

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = "%SYSTEMROOT%\hta.exe,1"
```

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a>Erweitern Sie immer erweiternde Zeichen folgen in Anführungszeichen

Erweiterungs Zeichenfolgen können Leerzeichen enthalten, wenn Sie erweitert werden. Da Leerzeichen häufig als Argument Trennzeichen interpretiert werden, werden unter bestimmten Umständen Probleme verursacht. Beispielsweise kann ein Befehl zum Aufrufen von myprogram wie folgt in der Registrierung gespeichert werden:

`%SYSTEMROOT%\MyProgram %1 %2`

"Myprogram" erwartet, dass "%1" der vollständige Pfad zu einem Dateinamen und "%2" ein Schalter ist, um eine Aktion anzugeben. Wenn dieser Befehl mit **den Argumenten c: \\ Program Files \\ My Documents \\document.txt** und **"/Print** ausgeführt wird und ein systemroot von C: \\ Winnt annimmt, wird er zu folgenden Zwecken erweitert:

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

In diesem Fall interpretiert myprogram, dass das erste Argument C: \\ Program ist, und das zweite Argument ist Files \\ My, das nicht das beabsichtigte Verhalten ist. Die Argumente werden jedoch unabhängig davon, ob Sie Leerzeichen enthalten, ordnungsgemäß interpretiert, wenn die erweiterbaren Zeichen folgen wie folgt in Anführungszeichen gesetzt werden:

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a>"AutoPlay/AutoRun" nicht mit Dateizuordnungen verwechseln

Dateizuordnungen ähneln in gewisser Weise AutoPlay/AutoRun. Allerdings bietet AutoPlay/AutoRun separate und unterschiedliche Funktionen, die von den Dateizuordnungen bereitgestellt werden. Weitere Informationen finden Sie unter [Erstellen einer Autorun-aktivierten CD-ROM-Anwendung](autoplay.md).

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a>Verwechseln Sie die Internet Explorer-MIME-Datenbank nicht mit Dateizuordnungen.

Dateizuordnungen ähneln der Windows Internet Explorer-MIME-Datenbank, da Dateitypen eine MIME-Typdefinition enthalten können (und sollten sollte). Die Internet Explorer-MIME-Datenbank ist jedoch getrennt und unterscheidet sich von Dateizuordnungen.

## <a name="use-properly-formed-and-versioned-progids"></a>Ordnungsgemäß formatierte und versionierte ProgIDs verwenden

Verwenden Sie immer [versionierte ProgIDs](fa-progids.md), auch wenn nur eine Version der ProgID vorhanden ist. ProgIDs mit Versions Angabe helfen, ProgID-Konflikte und über schreibungen zu vermeiden. Außerdem ermöglichen Sie, dass unterschiedliche Versionen einer Anwendung nebeneinander vorhanden sind.

## <a name="do-not-use-short-file-name-extensions"></a>Verwenden Sie keine kurzen Dateinamen Erweiterungen.

Lange Dateinamen Erweiterungen bieten folgende Vorteile:

-   Die begrenzte Länge der kurzen Erweiterungen macht Sie anfällig für *Erweiterungs Kollisionen.* Ein Erweiterungs Konflikt tritt auf, wenn die gleiche Erweiterung verwendet wird, um mehrere Dateitypen zu klassifizieren. Die Verwendung von langen Erweiterungen verringert die Wahrscheinlichkeit einer Kollision erheblich.
-   Kurze Dateinamen sind tendenziell etwas kryptisch. Lange Erweiterungen sind tendenziell aussagekräftiger, da zusätzliche Informationen in die Erweiterung eingebettet werden können.

Weitere Informationen finden Sie unter [Dateinamen Erweiterungen](fa-file-extensions.md).

## <a name="register-new-file-types-in-the-iana-mime-database"></a>Registrieren neuer Dateitypen in der IANA-MIME-Datenbank

Die Internet Assigned Numbers Authority (IANA) bewahrt eine öffentliche Datenbank registrierter MIME-Typen auf. Wenn Sie einen neuen öffentlichen Dateityp definieren, wird empfohlen, dass Sie auch einen MIME-Typ für den Dateityp definieren und diesen Typ bei der IANA registrieren. Es fallen keine Kosten für die Registrierung an.

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a>Registrieren beim Windows-Webdienst für Dateizuordnungen

Anwendungsentwickler können sich mit dem Windows-Webdienst anmelden, den Benutzer für die Suche nach Anwendungen verwenden, die auf bestimmte Dateitypen angewendet werden können. Der Prozess für die Registrierung mit dem Webdienst wird im [Windows-Datei Zuordnungs System-Onboarding-Prozess](https://support.microsoft.com/kb/929149)ausführlich erläutert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispielszenario für Datei Zuordnung](fa-sample-scenarios.md)
</dt> <dt>

[Richtlinien für die Verwaltung von Standardanwendungen in Windows Vista und höher](vista-managing-defaults.md)
</dt> <dt>

[Standardprogramme](default-programs.md)
</dt> <dt>

[Festlegen des Programm Zugriffs und der Computer Standardwerte (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 



