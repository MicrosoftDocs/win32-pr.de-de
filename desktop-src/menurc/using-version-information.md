---
title: Verwenden von Versionsinformationen
description: In diesem Thema wird erläutert, wie die Versionsinformationsfunktionen verwendet werden.
ms.assetid: 447b57c9-9e94-4a28-897e-f7b87d9cb25a
keywords:
- Ressourcen,Versionsinformationen
- Versionsinformationen
- Installationsdateiinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0447bc1dfc3b2d5d5006bb5ff9ca3e9fa8f3d488e9b5621acb932c843fc3630f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846990"
---
# <a name="using-version-information"></a>Verwenden von Versionsinformationen

Ein Installationsprogramm hat in der Regel die folgenden Ziele:

-   So platzieren Sie Dateien am richtigen Speicherort.
-   Um den Benutzer zu benachrichtigen, wenn das Installationsprogramm eine vorhandene Datei durch eine deutlich andere Version ersetzt, z. B. durch Ersetzen einer Datei in deutscher Sprache durch eine englischsprachige Datei oder ersetzen Sie eine neuere Datei durch eine ältere Datei.

Beim Schreiben des Installationsprogramms müssen Sie über die folgenden Informationen für jede Datei verfügen:

-   Name und Speicherort der Datei (als Quelldatei bezeichnet).
-   Der Name der entsprechenden Datei auf der Festplatte des Benutzers (als Zieldatei bezeichnet). Dieser Name ist in der Regel mit dem Dateinamen auf dem Installationsdatenträger identisch.
-   Der Freigabestatus der Datei, d. &a. ob die Datei für die installierte Anwendung privat ist oder von mehreren Anwendungen gemeinsam genutzt werden kann.

Das Installationsprogramm kann die [**VerFindFile-Funktion**](/windows/desktop/api/Winver/nf-winver-verfindfilea) verwenden, um zu bestimmen, wo die Datei auf den Datenträger kopiert werden soll. Diese Funktion kann auch verwendet werden, um anzugeben, ob die Datei für die Anwendung privat ist oder freigegeben werden kann. Wenn beim Suchen der Datei ein Problem auftritt, gibt **VerFindFile** einen Fehlerwert zurück. Wenn das System beispielsweise die Zieldatei verwendet, gibt **VerFindFile** **VFF \_ FILEINUSE zurück.** Das Installationsprogramm muss den Benutzer über das Problem benachrichtigen und auf die Entscheidung des Benutzers reagieren, die Installation fortzufahren oder zu beenden.

Die [**VerInstallFile-Funktion**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) kopiert die Quelldatei in eine temporäre Datei in dem von [**VerFindFile angegebenen Verzeichnis.**](/windows/desktop/api/Winver/nf-winver-verfindfilea) Bei Bedarf erweitert **VerInstallFile** die Datei mithilfe der Funktionen in der Datendekomprimierungsbibliothek.

[**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) vergleicht die Versionsinformationen der temporären Datei mit denen der Zieldatei. Wenn sich die beiden Unterscheiden, **gibt VerInstallFile** einen oder mehrere Fehlerwerte zurück. Beispielsweise wird **VIF \_ SRCOLD** zurückgegeben, wenn die temporäre Datei älter als die Zieldatei ist, und **VIF \_ DIFFLANG,** wenn die Dateien unterschiedliche Sprachbezeichner oder Codepagewerte haben. Das Installationsprogramm muss den Benutzer über das Problem benachrichtigen und auf die Entscheidung des Benutzers reagieren, die Installation fortzufahren oder zu beenden.

Einige [**VerInstallFile-Fehler**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) können wiederhergestellt werden. Das heißt, das Installationsprogramm kann **VerInstallFile unter** Angabe der **Option VIFF \_ FORCEINSTALL** erneut aufrufen, um die Datei unabhängig vom Versionskonflikt zu installieren. Wenn **VerInstallFile** **VIF \_ TEMPFILE** zurückgibt und der Benutzer die Installation nicht erzwingen möchte, sollte das Installationsprogramm die temporäre Datei löschen.

[**Bei VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) kann beim Versuch, die Installation zu erzwingen, ein nicht behebbarer Fehler auftreten, obwohl der Fehler zuvor nicht vorhanden war. Beispielsweise könnte die Datei von einem anderen Benutzer gesperrt werden, bevor das Installationsprogramm versucht hat, die Installation zu erzwingen. Wenn ein Installationsprogramm versucht, die Installation nach einem nicht wiederherstellbaren Fehler zu erzwingen, **schlägt VerInstallFile** fehl. Das Installationsprogramm muss Routinen für die Wiederherstellung nach dieser Art von Fehler enthalten.

Die empfohlene Lösung besteht in der Anzeige eines Dialogfelds mit den Schaltflächen **Installieren,** **Überspringen** und **Alle installieren.** (Eine andere Lösung ist ein Dialogfeld mit den Schaltflächen **Ja,** **Ja zu Allen,** **Überspringen** und **Abbrechen.)** Die **Schaltfläche Alle installieren** sollte verhindern, dass das Installationsprogramm den Benutzer zu ähnlichen Fehlern auffordern kann, indem die Option **VIFF \_ FORCEINSTALL** in alle nachfolgenden Verwendungen von [**VerInstallFile einfing.**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) Bei nicht behebbaren Fehlern sollten die **Schaltflächen Alle** **installieren** und installieren deaktiviert werden.

Um dem Benutzer eine nützliche Fehlermeldung anzuzeigen, muss das Installationsprogramm in der Regel Informationen aus den Versionsressourcen der in Konflikt stehenden Dateien abrufen. Es gibt vier Funktionen, die das Installationsprogramm für diesen Zweck verwenden kann:

-   [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)
-   [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)
-   [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
-   [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)

[**GetFileVersionInfoSize gibt**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) die Größe der Versionsinformationen zurück. [**GetFileVersionInfo verwendet**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) von **GetFileVersionInfoSize** abgerufene Informationen, um eine Struktur abzurufen, die die Versionsinformationen enthält. [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) ruft einen bestimmten Member aus dieser Struktur ab.

Wenn [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) beispielsweise den **VIF \_ DIFFTYPE-Fehler** zurückgibt, sollte das Installationsprogramm die [**Funktionen GetFileVersionInfoSize,**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)und [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) für die temporären und Zieldateien verwenden, um den allgemeinen Typ jeder Datei zu erhalten. Wenn die Sprachen der Dateien in Konflikt stehen, sollte das Installationsprogramm auch [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea) verwenden, um den Bezeichner der binären Sprache in eine Textdarstellung der Sprache zu übersetzen. (Beispielsweise wird 0x040C in die Zeichenfolge "Französisch" übersetzt.)

Wenn [**VerInstallFile einen**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) Dateifehler zurückgibt, z. B. **VIF \_ ACCESSVIOLATION,** sollte das Installationsprogramm die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) verwenden, um den letzten Fehlerwert abzurufen. Das Programm sollte diesen Wert in eine informative Meldung übersetzen, die dem Benutzer angezeigt wird. Das Programm darf keine Kontrolle zwischen den Aufrufen von **VerInstallFile und** **GetLastError ergeben.**

 

 