---
description: Ebenso wie eine Anwendung einen Gerätekontext anzeigen (DC) erfordert, bevor Sie im Client Bereich eines Fensters gezeichnet werden kann, benötigt Sie einen Drucker-DC, bevor Sie mit dem Senden der Ausgabe an einen Drucker beginnen kann.
ms.assetid: 5bdcec28-e28d-402d-8d80-e8aa5ecb4e74
title: Drucker Geräte Kontexte (Dokumente und Drucken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b75fb79d6ab8bb4198bf52bff10eccf5ec3cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216442"
---
# <a name="printer-device-contexts-documents-and-printing"></a>Drucker Geräte Kontexte (Dokumente und Drucken)

Ebenso wie eine Anwendung einen Gerätekontext anzeigen (DC) erfordert, bevor Sie im Client Bereich eines Fensters gezeichnet werden kann, benötigt Sie einen Drucker-DC, bevor Sie mit dem Senden der Ausgabe an einen Drucker beginnen kann. Ein Drucker-DC ähnelt einem Display-DC darin, dass es sich um eine interne Datenstruktur handelt, die eine Reihe von Grafikobjekten und deren zugeordneten Attributen definiert und die Grafikmodi angibt, die die Ausgabe beeinflussen. Die Grafik Objekte enthalten einen Stift für das Zeichnen von Zeilen, einen Pinsel zum Zeichnen und ausfüllen und eine Schriftart für die Textausgabe.

Anders als bei einem Anzeige-DC ist ein Drucker-DC nicht im Besitz der Fenster Verwaltungs Komponente, und er kann nicht durch Aufrufen der [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) -Funktion abgerufen werden. Stattdessen muss eine [**Anwendung die Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createdca) "up" oder " [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) " aufrufen.

Wenn die Anwendung [**die Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-createdca) Funktion" aufruft, muss Sie einen Treiber-und einen Portnamen angeben. Rufen Sie die Funktion [**GetPrinter**](getprinter.md) oder [**enumprinter**](enumprinters.md) auf, um diese Namen abzurufen.

Wenn die Anwendung die [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion aufruft und den PD \_ returndc-Wert im **Flags** -Member der [**printdlgex**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) -Struktur angibt, gibt das System ein Handle für einen Gerätekontext für den Drucker zurück, der vom Benutzer ausgewählt wurde. Weitere Informationen finden Sie unter [Drucken von Eigenschaften](../dlgbox/print-property-sheet.md) Seiten und "Verwenden des Druckeigenschaften Blatts" in [Verwenden von allgemeinen Dialog Feldern](../dlgbox/using-common-dialog-boxes.md).

 

 
