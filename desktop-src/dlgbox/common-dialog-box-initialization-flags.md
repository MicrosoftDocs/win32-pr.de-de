---
title: Allgemeine Initialisierungs Flags für Dialog Felder
description: Flags werden verwendet, um das Verhalten und die Darstellung eines allgemeinen Dialog Felds zu ändern.
ms.assetid: 072cdcab-00d1-4a09-97fb-a6de2d51392e
keywords:
- Allgemeine Dialog Feld Bibliothek, Initialisierung
- Allgemeine Dialogfelder, initialisieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c994e743178e3b6a17129275affed099d3004
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/19/2020
ms.locfileid: "104474730"
---
# <a name="common-dialog-box-initialization-flags"></a>Allgemeine Initialisierungs Flags für Dialog Felder

Flags werden verwendet, um das Verhalten und die Darstellung eines allgemeinen Dialog Felds zu ändern. Initialisierungsflags sind die Werte, die Sie im **Flags** -Member der-Struktur festlegen, die zum Erstellen des Dialog Felds verwendet wird. Mithilfe der Flags geben Sie an, welche Steuerelemente in einem Dialogfeld Anfangswerte empfangen, welche Steuerelemente deaktiviert werden und wie Sie den Wertebereich ändern können, den der Benutzer mit den Steuerelementen festlegen kann. Außerdem verwenden Sie die Flags, um Hook-Prozeduren und benutzerdefinierte Vorlagen für die Dialogfelder zu aktivieren.

Beispielsweise können Sie den Wert von **CF- \_ Effekten** im **Flags** -Member der [**choosefont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Struktur festlegen, um das Dialogfeld **Schriftart** anzuweisen, die Effekte-Steuerelemente anzuzeigen. Mit diesen Steuerelementen können Benutzer sowohl eine Schriftart Farbe als auch durchgestrichen und Unterstreichung auswählen.

Die Initialisierungs Kennzeichen-Werte sind für jedes allgemeine Dialogfeld eindeutig und werden ausführlich von den **Flags** -Membern der folgenden Strukturen beschrieben, die Ihnen entsprechen:

-   [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
-   [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
-   [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
-   [**Pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
-   [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
-   [**Printdlgex**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

 

 




