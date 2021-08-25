---
title: Allgemeine RAS-Dialogfelder
description: Windows stellt eine Reihe von Funktionen bereit, die die vom System bereitgestellten RAS-Dialogfelder anzeigen.
ms.assetid: 8231511a-7339-4fbb-8a39-f643ac575856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be93db8e8d1819abe56d98bb293a7b6b027089be0648b00f7848d5204e911ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909720"
---
# <a name="ras-common-dialog-boxes"></a>Allgemeine RAS-Dialogfelder

Windows stellt eine Reihe von Funktionen bereit, die die vom System bereitgestellten RAS-Dialogfelder anzeigen. Diese Funktionen erleichtern Anwendungen das Anzeigen einer vertrauten Benutzeroberfläche, sodass Benutzer RAS-Aufgaben ausführen können. Beispielsweise können Benutzer Verbindungen herstellen und überwachen oder mit Telefonbucheinträgen arbeiten. Windows 95 unterstützt diese Funktionen derzeit nicht.

Die [**RasPhonebookDlg-Funktion**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) zeigt das Hauptdialogfeld **DFÜ-Netzwerk** an. In diesem Dialogfeld kann der Benutzer einen ausgewählten Telefonbucheintrag wählen, bearbeiten oder löschen, einen neuen Telefonbucheintrag erstellen oder Benutzereinstellungen angeben. Die **RasPhonebookDlg-Funktion** verwendet die [**RASPBDLG-Struktur,**](/previous-versions/windows/desktop/legacy/aa377607(v=vs.85)) um zusätzliche Eingabe- und Ausgabeparameter anzugeben. Beispielsweise können Sie Member der -Struktur festlegen, um die Position des Dialogfelds auf dem Bildschirm zu steuern. Sie können die **RASPBDLG-Struktur** verwenden, um eine [**RasPBDlgFunc-Rückruffunktion**](/windows/desktop/api/Rasdlg/nc-rasdlg-raspbdlgfunca) anzugeben, die Benachrichtigungen über Benutzeraktivitäten empfängt, während das Dialogfeld geöffnet ist. Ras ruft beispielsweise Ihre **RasPBDlgFunc-Funktion** auf, wenn der Benutzer einen Telefonbucheintrag wählt, bearbeitet, erstellt oder löscht.

Sie können die [**RasDialDlg-Funktion**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) verwenden, um einen RAS-Verbindungsvorgang zu starten, ohne das Hauptdialogfeld **DFÜ-Netzwerk** anzuzeigen. Mit **RasDialDlg** geben Sie eine Telefonnummer oder einen Telefonbucheintrag für den Anruf an. Die Funktion zeigt einen Stream von Dialogfeldern an, die den Zustand des Verbindungsvorgangs angeben. Die **RasDialDlg-Funktion** verwendet eine [**RASDIALDLG-Struktur,**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)) um zusätzliche Eingabe- und Ausgabeparameter anzugeben, z. B. die Position des Dialogfelds und die Telefonbuchunterentladung, die aufgerufen werden soll.

Um das **DFÜ-Netzwerk** Eigenschaftenblatt anzuzeigen, rufen Sie die [**RasMonitorDlg-Funktion auf.**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85)) In diesem Dialogfeld kann der Benutzer den Status vorhandener Verbindungen überwachen. Die **RasMonitorDlg-Funktion** verwendet eine [**RASMONITORDLG-Struktur,**](/previous-versions/windows/desktop/legacy/aa377591(v=vs.85)) um zusätzliche Eingabe- und Ausgabeparameter anzugeben, z. B. die Position des Dialogfelds und die Eigenschaftenblattseite, die oben angezeigt werden soll.

Sie können die [**RasEntryDlg-Funktion**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) aufrufen, um ein Eigenschaftenblatt zum Erstellen, Bearbeiten oder Kopieren eines Telefonbucheintrags anzuzeigen. Die **RasEntryDlg-Funktion** verwendet eine [**RASENTRYDLG-Struktur,**](/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)) um zusätzliche Eingabe- und Ausgabeparameter anzugeben, z. B. die Position des Dialogfelds und den Typ des Telefonbuchvorgangs.

 

 