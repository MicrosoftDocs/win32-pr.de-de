---
description: Das Einbetten einer Schriftart ist das Verfahren, bei dem ein Dokument und die darin enthaltenen Schriftarten in eine Datei für die Übertragung an einen anderen Computer gebündelt werden.
ms.assetid: ded409f1-5bd9-411b-b905-fc49c484786a
title: Eingebettete Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb8ab821afa5f44ded05a4a61a53439b8db9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130781"
---
# <a name="embedded-fonts"></a>Eingebettete Schriftarten

Das Einbetten einer Schriftart ist das Verfahren, bei dem ein Dokument und die darin enthaltenen Schriftarten in eine Datei für die Übertragung an einen anderen Computer gebündelt werden. Durch das Einbetten einer Schriftart wird sichergestellt, dass auf dem Computer, der die Datei empfängt, eine in einer übertragenen Datei angegebene Schriftart vorhanden ist. Es können jedoch nicht alle Schriftarten von Computer zu Computer verschoben werden, da die meisten Schriftarten jeweils nur auf einem Computer lizenziert sind. Nur TrueType-und OpenType-Schriftarten können eingebettet werden.

Anwendungen sollten eine Schriftart nur dann in ein Dokument einbetten, wenn Sie von einem Benutzer angefordert werden. Eine Anwendung kann nicht zusammen mit Dokumenten verteilt werden, die eingebettete Schriftarten enthalten, und eine Anwendung selbst darf keine eingebettete Schriftart enthalten. Wenn eine Anwendung eine Schriftart in einem beliebigen Format verteilt, müssen die proprietären Rechte des Besitzers der Schriftart bestätigt werden.

Es kann einen Verstoß gegen die proprietären Rechte oder den Benutzer Lizenzvertrag eines Schriftart Herstellers darstellen, um Schriftarten einzubetten, wenn Einbettungen nicht zulässig sind oder die folgenden Richtlinien zum Einbetten von Schriftarten nicht beachtet werden müssen. Die Lizenz einer Schriftart erteilt möglicherweise nur Lese-/Schreibberechtigung für eine Schriftart, die auf dem Zielcomputer installiert und verwendet werden soll. Oder die Lizenz erteilt eine Leseberechtigung. Mit der Berechtigung "schreibgeschützt" kann ein Dokument vom Zielcomputer angezeigt und gedruckt (aber nicht geändert) werden. Dokumente mit schreibgeschützten eingebetteten Schriftarten sind selbst schreibgeschützt. Schreibgeschützte eingebettete Schriftarten dürfen nicht aus dem Dokument entbündelt und auf dem Zielcomputer installiert sein.

Eine Anwendung kann den Lizenzstatus ermitteln, indem Sie die [**getoutlinetextmetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) -Funktion aufrufen und den **otmfstype** -Member der [**outlinetextmetric**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) -Struktur untersucht. Wenn Bit 1 von **otmarstype** festgelegt ist, ist die Einbettung für die Schriftart nicht zulässig. Wenn Bit 1 eindeutig ist, kann die Schriftart eingebettet werden. Wenn Bit 2 festgelegt ist, ist die Einbettung schreibgeschützt.

Zum Einbetten einer TrueType-Schriftart kann eine Anwendung die [**getfontdata**](/windows/desktop/api/Wingdi/nf-wingdi-getfontdata) -Funktion verwenden, um die Schriftart Datei zu lesen. Wenn die Parameter *dwtable* und *dwOffset* von [**getfontdata**](/windows/win32/api/wingdi/nf-wingdi-getfontdata) auf 0l und der *cbData* -Parameter auf 1L festgelegt werden, wird sichergestellt, dass die Anwendung die gesamte Schriftart Datei von Anfang an liest.

Es stehen verschiedene Funktionen zum Einbetten von OpenType-Schriftarten zur Verfügung, abhängig von der Zeichenbreite und dem Speicherort der Schriftart Daten. Zum Einbetten einer OpenType-Unicode-Schriftart, die sich in einem Gerätekontext befindet, kann eine Anwendung [**ttembedfont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont)verwenden. Zum Einbetten einer OpenType-UCS-4-Schriftart, die sich in einem Gerätekontext befindet, kann eine Anwendung [**ttembedfontex**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontex)verwenden. Zum Einbetten einer OpenType-Unicode-Schriftart, die sich in einer Schriftart Datei befindet, kann eine Anwendung [**ttembedfontfromfile**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontfromfilea)verwenden. Weitere Informationen zum Einbetten von OpenType-Schriftarten finden Sie in der [Referenz zur Schriftart Einbettung](font-embedding-reference.md).

Nachdem eine Anwendung die Schriftart Daten abgerufen hat, kann Sie die Daten unter Verwendung eines beliebigen anwendbaren Formats mit dem Dokument speichern. Die meisten Anwendungen erstellen ein Schriftart Verzeichnis im Dokument, das die eingebetteten Schriftarten auflistet, und gibt an, ob die Einbettung Lese-/Schreibzugriff oder schreibgeschützt ist. Eine Anwendung kann die " **otmpstylename** "-und " **otmfamilyname** "-Member der " [**outlinetextmetric**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica) "-Struktur verwenden, um die Schriftart zu identifizieren.

Wenn das schreibgeschützte Bit für die eingebettete Schriftart festgelegt ist, müssen Anwendungen die Schriftart Daten verschlüsseln, bevor Sie mit dem Dokument gespeichert werden. Die Verschlüsselungsmethode muss nicht kompliziert sein. Beispielsweise ist die Verwendung des XOR-Operators zum Kombinieren der Schriftart Daten mit einer Anwendungs definierten Konstante ausreichend und schnell.

 

 
