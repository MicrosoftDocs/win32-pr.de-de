---
description: So wie eine Anwendung einen Anzeigegerätekontext (DC) erfordert, bevor sie mit dem Zeichnen im Clientbereich eines Fensters beginnen kann, benötigt sie einen Druckerdomänencontroller, bevor sie mit dem Senden der Ausgabe an einen Drucker beginnen kann.
ms.assetid: 5bdcec28-e28d-402d-8d80-e8aa5ecb4e74
title: Druckergerätekontexte (Dokumente und Drucken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c868d5bf8247375375b33bcb034a70bd6f28c5b9104b61e264543a63281069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947400"
---
# <a name="printer-device-contexts-documents-and-printing"></a>Druckergerätekontexte (Dokumente und Drucken)

So wie eine Anwendung einen Anzeigegerätekontext (DC) erfordert, bevor sie mit dem Zeichnen im Clientbereich eines Fensters beginnen kann, benötigt sie einen Druckerdomänencontroller, bevor sie mit dem Senden der Ausgabe an einen Drucker beginnen kann. Ein Druckerdomänencontroller ähnelt einem Anzeigedomänencontroller, da es sich um eine interne Datenstruktur handelt, die eine Reihe von Grafikobjekten und deren zugeordnete Attribute definiert und die Grafikmodi angibt, die sich auf die Ausgabe auswirken. Die grafischen Objekte enthalten einen Stift für die Linienzeichnung, einen Pinsel zum Zeichnen und Auffüllen und eine Schriftart für die Textausgabe.

Im Gegensatz zu einem Anzeigedomänencontroller befindet sich ein Druckerdomänencontroller nicht im Besitz der Fensterverwaltungskomponente und kann nicht durch Aufrufen der [**GetDC-Funktion ermittelt**](/windows/desktop/api/winuser/nf-winuser-getdc) werden. Stattdessen muss eine Anwendung die [**Funktion CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) oder [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) aufrufen.

Wenn Ihre Anwendung die [**CreateDC-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createdca) aufruft, muss sie einen Treiber- und Portnamen angeben. Um diese Namen abzurufen, rufen Sie die [**GetPrinter- oder**](getprinter.md) [**EnumPrinters-Funktion**](enumprinters.md) auf.

Wenn Ihre Anwendung die [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) aufruft und den PD RETURNDC-Wert im \_ **Flags-Element** der [**PRINTDLGEX-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) angibt, gibt das System ein Handle an einen Gerätekontext für den vom Benutzer ausgewählten Drucker zurück. Weitere Informationen finden Sie unter [Print Property Sheet](../dlgbox/print-property-sheet.md) und "Using the Print Property Sheet" in Using Common Dialog [Boxes](../dlgbox/using-common-dialog-boxes.md).

 

 
