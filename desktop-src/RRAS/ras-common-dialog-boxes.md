---
title: Allgemeine RAS-Dialog Felder
description: Windows stellt eine Reihe von Funktionen bereit, mit denen die vom System bereitgestellten RAS-Dialogfelder angezeigt werden.
ms.assetid: 8231511a-7339-4fbb-8a39-f643ac575856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3032da8b0647b48941d85fc4f085ddb8ced0125f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102234"
---
# <a name="ras-common-dialog-boxes"></a>Allgemeine RAS-Dialog Felder

Windows stellt eine Reihe von Funktionen bereit, mit denen die vom System bereitgestellten RAS-Dialogfelder angezeigt werden. Diese Funktionen erleichtern Anwendungen die Anzeige einer vertrauten Benutzeroberfläche, sodass Benutzer RAS-Aufgaben ausführen können. Benutzer können z. b. Verbindungen einrichten und überwachen oder mit Telefonbucheinträgen arbeiten. Windows 95 unterstützt diese Funktionen zurzeit nicht.

Mit der [**rasphonebookdlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) -Funktion wird das Haupt Dialogfeld für das **Einwählnetzwerk** angezeigt. In diesem Dialogfeld kann der Benutzer einen ausgewählten Telefonbucheintrag auswählen, bearbeiten oder löschen, einen neuen Telefonbucheintrag erstellen oder Benutzereinstellungen angeben. Die **rasphonebookdlg** -Funktion verwendet die [**raspbdlg**](/previous-versions/windows/desktop/legacy/aa377607(v=vs.85)) -Struktur, um zusätzliche Eingabe-und Ausgabeparameter anzugeben. Beispielsweise können Sie Member der-Struktur festlegen, um die Position des Dialog Felds auf dem Bildschirm zu steuern. Mit der **raspbdlg** -Struktur können Sie eine [**raspbdlgfunc**](/windows/desktop/api/Rasdlg/nc-rasdlg-raspbdlgfunca) -Rückruffunktion angeben, die Benachrichtigungen über die Benutzeraktivität empfängt, während das Dialogfeld geöffnet ist. Beispielsweise ruft RAS Ihre **raspbdlgfunc** -Funktion auf, wenn der Benutzer einen Telefonbucheintrag abruft, bearbeitet, erstellt oder löscht.

Sie können die Funktion " [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) " verwenden, um einen RAS-Verbindungsvorgang zu starten, ohne das Haupt Dialogfeld "DFÜ **-Netzwerk** " anzuzeigen. Mit " **RasDialDlg**" geben Sie eine Telefonnummer oder einen Telefonbucheintrag an, der aufgerufen werden soll. Die-Funktion zeigt einen Stream von Dialogfeldern an, die den Zustand des Verbindungs Vorgangs angeben. Die **RasDialDlg** -Funktion verwendet eine [**RasDialDlg**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)) -Struktur, um zusätzliche Eingabe-und Ausgabeparameter anzugeben, z. b. die Position des Dialog Felds und den aufzurufenden Telefonbuch Teil Eintrag.

Um das Eigenschaften Blatt " **Einwählnetzwerk** " anzuzeigen, müssen Sie die Funktion " [**rasmonitordlg**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85)) " aufrufen. In diesem Dialogfeld können Benutzer den Status vorhandener Verbindungen überwachen. Die Funktion " **rasmonitordlg** " verwendet eine " [**rasmonitordlg**](/previous-versions/windows/desktop/legacy/aa377591(v=vs.85)) "-Struktur, um zusätzliche Eingabe-und Ausgabeparameter anzugeben, z. b. die Position des Dialog Felds und die Eigenschaften Blattseite, die oben angezeigt werden soll.

Sie können die Funktion " [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) " aufrufen, um ein Eigenschaften Blatt zum Erstellen, bearbeiten oder Kopieren eines Telefonbucheintrags anzuzeigen. Die Funktion " **RasEntryDlg** " verwendet eine " [**RasEntryDlg**](/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)) "-Struktur, um zusätzliche Eingabe-und Ausgabeparameter anzugeben, z. b. die Position des Dialog Felds und den Typ des Telefonbuch Vorgangs.

 

 