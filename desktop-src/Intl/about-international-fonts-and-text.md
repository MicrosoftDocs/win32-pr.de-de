---
description: In den Themen in diesem Abschnitt werden die grundlegenden Funktionen internationaler Schriftarten behandelt.
ms.assetid: a47303b5-f49b-4d6c-b061-9d6475530e83
title: Internationale Schriftart Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ade599577f97c696d3205e32bfaaca106ddaae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363567"
---
# <a name="international-font-management"></a>Internationale Schriftart Verwaltung

In den Themen in diesem Abschnitt werden die grundlegenden Funktionen internationaler Schriftarten behandelt. Anweisungen zur Verwendung der internationalen Schriftart Technologie in Ihren Anwendungen finden Sie unter [internationale Schriftart Enumeration und-Auswahl](using-international-fonts-and-text.md) und [Verwenden von MS Shell Dlg und MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md).

## <a name="font-management-infrastructure"></a>Schriftart Verwaltungsinfrastruktur

Ab Windows 7 unterstützt die Schriftart Verwaltungsinfrastruktur das Ausblenden von Schriftarten, die für die Schriftart Auswahllisten eines Benutzers nicht geeignet sind. Die Standardeinstellungen für das System sind das automatische Ausblenden von Schriftarten, die nicht für die auf dem Betriebssystem System aktivierten Eingabe Sprachen (Tastaturen) vorgesehen sind. Außerdem können Sie die Schriftarten in der Systemsteuerung für Schriftarten manuell ausblenden. Diese Funktion bedeutet, dass Benutzer nicht mehr mit langen Listen unzulässiger Schriftarten konfrontiert werden müssen und besonders wertvoll für internationale Benutzer sind, die in nicht lateinischen Skripts arbeiten.

In Windows 7 gibt es keine APIs für die direkte Abfrage der ausgeblendeten Schriftarten oder zum Ausblenden von Schriftarten. Dies bedeutet jedoch nicht, dass Sie dieses Feature nicht in Ihrer Anwendung nutzen können. Wenn Sie die Windows-Auswahl [**Schriftart**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) (Schriftart allgemein) verwenden, um die Schriftart Auswahl noch heute zu aktivieren, erhalten Sie das neue Verhalten kostenlos. Das neue Windows Scenic Menüband (Schriftart Steuerelemente), das in Windows 7 eingeführt wurde, unterstützt auch dieses Verhalten und bietet einen weiteren Grund für die "Debuggen" Ihrer Anwendungen. Ausführliche Informationen zur Verwendung von Schriftart Steuerelementen in Menüband und Auswahl **Schriftart** zum Anzeigen von Schriftarten beim Herausfiltern der ausgeblendeten Schriftarten finden Sie unter [internationale Schriftart Enumeration und-Auswahl](using-international-fonts-and-text.md).

Beachten Sie, dass das Ausblenden von Schriftarten nur Auswirkungen auf die Schriftart Auswahl Es wirkt sich nicht auf Zeichnungs-APIs aus. Wenn eine Schriftart in einen Gerätekontext ausgewählt wird, wirkt sich dies nicht auf das Zeichnen aus, da die Schriftart ausgeblendet ist. Die [**enumfontfamiliesex**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) -Funktion Listet weiterhin Schriftarten auf, die auf ausgeblendet festgelegt sind.

## <a name="gdi-font-embedding-and-subsetting"></a>GDI-Schriftart Einbettung und untergeordnete Einstellung

International Fonts Technology verwendet die Schriftart Einbettungs Dienst Bibliothek, um das Bündeln von TrueType-und OpenType-Schriftarten in ein Dokument oder eine Datei zu ermöglichen. Durch das Einbetten einer Schriftart in einer Datei wird sichergestellt, dass die Schriftart auf dem Computer vorhanden ist, der die Datei empfängt. Weitere Informationen finden Sie unter [Referenz zur Schriftart Einbettung](../gdi/font-embedding-reference.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internationale Schriftart Enumeration und-Auswahl](using-international-fonts-and-text.md)
</dt> <dt>

[Verwenden von MS Shell Dlg und MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md)
</dt> <dt>

[Referenz zur Schriftart Einbettung](../gdi/font-embedding-reference.md)
</dt> </dl>

 

 
