---
title: Verwenden von Versionsinformationen
description: In diesem Thema wird erläutert, wie die Versions Informationsfunktionen verwendet werden.
ms.assetid: 447b57c9-9e94-4a28-897e-f7b87d9cb25a
keywords:
- Ressourcen, Versionsinformationen
- Versionsinformationen
- Informationen zur Installationsdatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8785275f5aac69218989250d1c0f83e0a1ff9f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725456"
---
# <a name="using-version-information"></a>Verwenden von Versionsinformationen

Ein Installationsprogramm umfasst in der Regel die folgenden Ziele:

-   , Um Dateien am richtigen Speicherort zu platzieren.
-   , Um den Benutzer zu benachrichtigen, wenn das Installationsprogramm eine vorhandene Datei durch eine Version ersetzt, die sich erheblich unterscheidet – beispielsweise, wenn Sie eine deutschsprachige Datei durch eine englischsprachige Datei ersetzen oder eine neuere Datei durch eine ältere Datei ersetzen.

Wenn Sie das Installationsprogramm schreiben, müssen Sie für jede Datei über die folgenden Informationen verfügen:

-   Der Name und Speicherort der Datei (als Quelldatei bezeichnet).
-   Der Name der entsprechenden Datei auf der Festplatte des Benutzers (als Zieldatei bezeichnet). Dieser Name ist in der Regel identisch mit dem Dateinamen auf dem Installations Datenträger.
-   Der Freigabe Status der Datei – d. h. ob die Datei für die zu installierende Anwendung privat ist oder von mehreren Anwendungen gemeinsam genutzt werden kann.

Das Installationsprogramm kann die [**verfindfile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) -Funktion verwenden, um zu bestimmen, wo die Datei auf den Datenträger kopiert werden soll. Diese Funktion kann auch verwendet werden, um anzugeben, ob die Datei für die Anwendung privat ist oder freigegeben werden kann. Wenn beim Auffinden der Datei ein Problem auftritt, gibt **verfindfile** einen Fehlerwert zurück. Wenn das System z. b. die Zieldatei verwendet, gibt **verfindfile** **VFF \_ FileInUse** zurück. Das Installationsprogramm muss den Benutzer über das Problem benachrichtigen und darauf reagieren, dass die Benutzer die Installation fortsetzen oder beenden können.

Die [**verinstallfile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) -Funktion kopiert die Quelldatei in eine temporäre Datei in dem Verzeichnis, das von [**verfindfile**](/windows/desktop/api/Winver/nf-winver-verfindfilea)angegeben wird. Falls erforderlich, erweitert **verinstallfile** die Datei mithilfe der Funktionen in der datendekomprimierungbibliothek.

[**Verinstallfile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) vergleicht die Versionsinformationen der temporären Datei mit der der Zieldatei. Wenn sich die beiden unterscheiden, gibt **verinstallfile** mindestens einen Fehlerwert zurück. Beispielsweise wird **Vif \_ srcold** zurückgegeben, wenn die temporäre Datei älter als die Zieldatei ist, und **Vif \_ difflang** , wenn die Dateien unterschiedliche Sprach-IDs oder Code Page Werte aufweisen. Das Installationsprogramm muss den Benutzer über das Problem benachrichtigen und darauf reagieren, dass die Benutzer die Installation fortsetzen oder beenden können.

Einige [**verinstallfile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) -Fehler sind wiederherstellbar. Das heißt, dass das Installationsprogramm " **verinstallfile** " erneut aufruft und die VIFF-Option " **\_ forceinstall** " angibt, um die Datei unabhängig vom Versions Konflikt zu installieren. Wenn **verinstallfile** " **Vif \_ tempfile** " zurückgibt und der Benutzer entscheidet, die Installation nicht zu erzwingen, sollte das Installationsprogramm die temporäre Datei löschen.

Bei [**verinstallfile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) kann ein nicht BEHEB barer Fehler auftreten, wenn versucht wird, die Installation zu erzwingen, obwohl der Fehler zuvor noch nicht vorhanden war. Beispielsweise könnte die Datei von einem anderen Benutzer gesperrt werden, bevor das Installationsprogramm versucht, die Installation zu erzwingen. Wenn ein Installationsprogramm versucht, die Installation nach einem nicht BEHEB baren Fehler zu erzwingen, schlägt **verinstallfile** fehl. Das Installationsprogramm muss Routinen enthalten, um diese Art von Fehler zu beheben.

Die empfohlene Lösung besteht darin, ein Dialogfeld mit den Schaltflächen **install**, **Skip** und **install all** anzuzeigen. (Eine andere Lösung ist ein Dialogfeld mit den Schaltflächen **Ja**, **Ja, über** **springen** und **Abbrechen**.) Mithilfe der Schaltfläche **alle installieren** sollte verhindert werden, dass das Installationsprogramm den Benutzer zu ähnlichen Fehlern auffordert, indem er die **VIFF \_ forceinstall** -Option in alle nachfolgenden Verwendungen von [**verinstallfile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea)einschließt. Bei nicht BEHEB baren Fehlern sollten die Schaltflächen **Installieren** und **installieren alle** deaktiviert werden.

Zum Anzeigen einer nützlichen Fehlermeldung für den Benutzer muss das Installationsprogramm normalerweise Informationen aus den Versions Ressourcen der in Konflikt stehenden Dateien abrufen. Es gibt vier Funktionen, die das Installationsprogramm zu diesem Zweck verwenden kann:

-   [**Fehler bei GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)
-   [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)
-   [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
-   [**Verlanguagename**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)

[**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) gibt die Größe der Versionsinformationen zurück. [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) verwendet Informationen, die von **GetFileVersionInfoSize** abgerufen werden, um eine Struktur abzurufen, die die Versionsinformationen enthält. [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) Ruft ein bestimmtes Element aus dieser Struktur ab.

Wenn [**verinstallfile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) beispielsweise den **Vif- \_ difftype** -Fehler zurückgibt, sollte das Installationsprogramm die Funktionen [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea), [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)und [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) in den temporären Dateien und Zieldateien verwenden, um den allgemeinen Typ der einzelnen Dateien abzurufen. Wenn die Sprachen der Dateien in Konflikt stehen, sollte das Installationsprogramm auch [**verlanguagename**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea) verwenden, um den binären sprach Bezeichner in eine Textdarstellung der Sprache zu übersetzen. (Beispielsweise übersetzt 0x040c in die Zeichenfolge "Französisch".)

Wenn [**verinstallfile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) einen Datei Fehler zurückgibt, wie z. **b. Vif \_ accessverletzungs**, sollte das Installationsprogramm die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion verwenden, um den letzten Fehlerwert abzurufen. Das Programm sollte diesen Wert in eine informative Meldung übersetzen, die dem Benutzer angezeigt wird. Das Programm darf keine Kontrolle zwischen den Aufrufen von " **verinstallfile** " und " **GetLastError**" erhalten.

 

 