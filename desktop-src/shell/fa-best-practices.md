---
description: Die folgende Liste enthält empfohlene bewährte Methoden, die Sie beim Arbeiten mit Dateizuordnungen verwenden sollten.
title: Bewährte Methoden für Dateizuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8cfa57faea9423af31e494c37d97af2b61d690095fb669a6a9b47109f6e97e70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094215"
---
# <a name="best-practices-for-file-associations"></a>Bewährte Methoden für Dateizuordnungen

Die folgende Liste enthält empfohlene bewährte Methoden, die Sie beim Arbeiten mit Dateizuordnungen verwenden sollten.

-   [Dateizuordnungen nicht aus der Registrierung kopieren](#do-not-copy-file-associations-from-the-registry)
-   [Vermeiden Hard-Coding Pfaden zur Registrierung nach Möglichkeit](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [Erweiternde Zeichenfolgen immer in Anführungszeichen umschließen](#always-wrap-expanding-strings-in-quotation-marks)
-   [Autoplay/Autorun nicht mit Dateizuordnungen verwechseln](#do-not-confuse-autoplayautorun-with-file-associations)
-   [Verwechseln Sie die Internet Explorer MIME-Datenbank nicht mit Dateizuordnungen.](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [Ordnungsgemäß gebildete und versionsgeschützte ProgIDs verwenden](#use-properly-formed-and-versioned-progids)
-   [Verwenden Sie keine kurzen Dateierweiterungen.](#do-not-use-short-file-name-extensions)
-   [Registrieren neuer Dateitypen in der IANA MIME-Datenbank](#register-new-file-types-in-the-iana-mime-database)
-   [Registrieren beim Windows-Webdienst für Dateizuordnungen](#sign-up-with-the-windows-web-service-for-file-associations)
-   [Zugehörige Themen](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a>Dateizuordnungen nicht aus der Registrierung kopieren

Es wird empfohlen, vorhandene Dateizuordnungen nicht aus der Registrierung zu kopieren. Dies führt häufig zur Weitergabe von schlecht gebildeten Dateizuordnungen. Führen Sie stattdessen die Schritte aus, die unter [File Association Sample Scenario (Beispielszenario für Dateiassoz) beschrieben sind.](fa-sample-scenarios.md)

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a>Vermeiden Hard-Coding Pfaden zur Registrierung nach Möglichkeit

Ebenso wie hart codierende Pfade in Programmen Probleme verursachen können, können hart codierende Pfade in der Registrierung auch zu Problemen führen. Stattdessen sollten Sie Registrierungserweiterungszeichenfolgen (REG EXPAND SZ) verwenden, um ggf. \_ \_ Pfadunabhängigkeit zu bieten. Anstatt diese Methode zu verwenden, verwenden Sie beispielsweise Folgendes:

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

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a>Erweiternde Zeichenfolgen immer in Anführungszeichen umschließen

Erweiternde Zeichenfolgen können Leerzeichen enthalten, wenn sie erweitert werden. Da Leerzeichen häufig als Argumenttrennzeichen interpretiert werden, verursachen sie unter bestimmten Umständen Probleme. Beispielsweise kann ein Befehl zum Aufrufen von MyProgram wie in der Registrierung gespeichert werden:

`%SYSTEMROOT%\MyProgram %1 %2`

MyProgram erwartet, dass %1 der vollständige Pfad zu einem Dateinamen und %2 ein Schalter ist, um eine Aktion anzugeben. Wenn dieser Befehl mit den Argumenten **C: \\ Programme Eigene Dokumente \\ \\document.txt** und **/print** ausgeführt wird und ein SYSTEMROOT von C: WINNT angenommen wird, wird er auf folgenden Befehl \\ erweitert:

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

In diesem Fall interpretiert MyProgram, dass das erste Argument C: Program und das zweite Argument Files My ist, was \\ nicht das \\ beabsichtigte Verhalten ist. Die Argumente werden jedoch unabhängig davon, ob sie Leerzeichen enthalten, richtig interpretiert, wenn die erweiternden Zeichenfolgen wie folgt in Anführungszeichen eingeschlossen sind:

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a>Autoplay/Autorun nicht mit Dateizuordnungen verwechseln

Dateizuordnungen ähneln in einigen Fällen autoplay/autorun. Autoplay/Autorun bietet jedoch separate und unterschiedliche Einrichtungen von denen, die von Dateizuordnungen bereitgestellt werden. Weitere Informationen finden Sie unter [Creating an AutoRun-enabled CD-ROM Application](autoplay.md).

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a>Verwechseln Sie die Internet Explorer MIME-Datenbank nicht mit Dateizuordnungen.

Dateizuordnungen ähneln der Windows Internet Explorer MIME-Datenbank, da Dateitypen eine MIME-Typdefinition enthalten können (und sollten). Die mime Internet Explorer datenbank ist jedoch getrennt und von Dateizuordnungen getrennt.

## <a name="use-properly-formed-and-versioned-progids"></a>Ordnungsgemäß gebildete und versionsgeschützte ProgIDs verwenden

Verwenden Sie [immer ProgIDs mit Versionsversion,](fa-progids.md)auch wenn nur eine Version der ProgID verfügbar ist. Versionierte ProgIDs helfen, ProgID-Konflikte und Überschreibungen zu vermeiden. Sie ermöglichen auch, dass verschiedene Versionen einer Anwendung gemeinsam vorhanden sind.

## <a name="do-not-use-short-file-name-extensions"></a>Verwenden Sie keine kurzen Dateierweiterungen.

Lange Dateinamenerweiterungen bieten die folgenden Vorteile:

-   Die begrenzte Länge kurzer Erweiterungen macht sie anfällig für *Erweiterungskollisionen.* Ein Erweiterungskollision tritt auf, wenn dieselbe Erweiterung verwendet wird, um mehrere Dateitypen zu klassifizieren. Die Verwendung von langen Erweiterungen verringert die Wahrscheinlichkeit eines Zusammenstoßes erheblich.
-   Kurze Dateinamen sind in der Regel etwas kryptisch. Lange Erweiterungen sind in der Regel sinnvoller, da zusätzliche Informationen in die Erweiterung eingebettet werden können.

Weitere Informationen finden Sie unter [Dateierweiterungen](fa-file-extensions.md).

## <a name="register-new-file-types-in-the-iana-mime-database"></a>Registrieren neuer Dateitypen in der IANA MIME-Datenbank

Die Internet Assigned Numbers Authority (IANA) führt eine öffentliche Datenbank mit registrierten MIME-Typen. Beim Definieren eines neuen öffentlichen Dateityps wird empfohlen, auch einen MIME-Typ für den Dateityp zu definieren und diesen Typ bei der IANA zu registrieren. Für die Registrierung sind keine Kosten erforderlich.

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a>Registrieren beim Windows-Webdienst für Dateizuordnungen

Anwendungsentwickler können sich mit dem Windows-Webdienst registrieren, mit dem Benutzer Anwendungen finden, die mit bestimmten Dateitypen arbeiten können. Der Prozess für die Registrierung beim Webdienst wird im Windows [File Association System-On-Boarding-Prozess ausführlich ausführlich.](https://support.microsoft.com/kb/929149)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispielszenario für dateiassoz](fa-sample-scenarios.md)
</dt> <dt>

[Richtlinien für die Verwaltung von Standardanwendungen in Windows Vista und höher](vista-managing-defaults.md)
</dt> <dt>

[Standardprogramme](default-programs.md)
</dt> <dt>

[Festlegen von Programmzugriff und Computereinstellungen (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 



