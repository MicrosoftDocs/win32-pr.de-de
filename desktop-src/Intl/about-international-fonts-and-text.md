---
description: In den Themen in diesem Abschnitt werden die grundlegenden Funktionen von Internationalen Schriftarten behandelt.
ms.assetid: a47303b5-f49b-4d6c-b061-9d6475530e83
title: Internationale Schriftverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4c44661b234a95abb4d40f2204382b3d074bf1d7c0bb1c68a241345211695f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083050"
---
# <a name="international-font-management"></a>Internationale Schriftverwaltung

In den Themen in diesem Abschnitt werden die grundlegenden Funktionen von Internationalen Schriftarten behandelt. Anweisungen zur Verwendung der internationalen Schrifttechnologie in Ihren Anwendungen finden Sie unter [International Font Enumeration and Selection (Internationale Schriftartenenumeration und -auswahl)](using-international-fonts-and-text.md) und Using MS Shell [Dlg and MS Shell Dlg 2 (Verwenden von MS Shell Dlg und MS Shell Dlg 2).](using-ms-shell-dlg-and-ms-shell-dlg-2.md)

## <a name="font-management-infrastructure"></a>Schriftverwaltungsinfrastruktur

Ab Windows 7 unterstützt die Schriftartverwaltungsinfrastruktur das Ausblenden von Schriftarten, die für die Schriftartauswahllisten eines Benutzers nicht geeignet sind. In den Standardsystemeinstellungen werden Schriftarten automatisch ausgeblendet, die nicht für die Eingabesprache(n) (Tastaturen) konzipiert sind, die auf dem Betriebssystemsystem aktiviert sind. Darüber hinaus können Benutzer festlegen, dass Schriftarten im Systemsteuerung Schriftarten manuell ausgeblendet werden sollen. Dieses Feature bedeutet, dass Benutzer nicht mehr mit langen Listen ungeeigneter Schriftarten konfrontiert werden müssen, und ist besonders nützlich für internationale Benutzer, die in nicht lateinischen Skripts arbeiten.

In Windows 7 gibt es keine APIs zum direkten Abfragen der ausgeblendeten Schriftarten oder zum Festlegen der ausgeblendeten Schriftarten. Dies bedeutet jedoch nicht, dass Sie dieses Feature nicht in Ihrer Anwendung nutzen können. Wenn Sie die Windows [**ChooseFont-API**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) (Allgemeines Dialogfeld Schriftart) verwenden, um die Schriftartauswahl zu aktivieren, erhalten Sie das neue Verhalten kostenlos. Das neue Windows Ribbon (Font Controls), das in Windows 7 eingeführt wurde, unterstützt dieses Verhalten ebenfalls und bietet einen weiteren Grund, Ihre Anwendungen mit einem Menüband zu versehen. Ausführliche Informationen zur Verwendung von Schriftartsteuerelementen im Menüband und **ChooseFont** zum Anzeigen von Schriftarten beim Herausfiltern der ausgeblendeten Schriftarten finden Sie unter [Internationale Schriftartenenumeration und -auswahl.](using-international-fonts-and-text.md)

Beachten Sie, dass sich das Ausblenden von Schriftarten nur auf die Benutzeroberfläche für die Schriftartauswahl auswirkt. Dies wirkt sich nicht auf das Zeichnen von APIs aus. Wenn eine Schriftart in einem Gerätekontext ausgewählt wird, hat dies keine Auswirkungen auf das Zeichnen, da die Schriftart ausgeblendet ist. Die [**EnumFontFamiliesEx-Funktion**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) führt weiterhin eine Aufzählung von Schriftarten durch, die auf ausgeblendet festgelegt sind.

## <a name="gdi-font-embedding-and-subsetting"></a>Einbetten und Untersetzen von GDI-Schriftarten

Die Technologie für internationale Schriftarten nutzt die Bibliothek der Schriftarteinbettungsdienste, damit Sie TrueType- und OpenType-Schriftarten in einem Dokument oder einer Datei bündeln können. Durch das Einbetten einer Schriftart in eine Datei wird sichergestellt, dass die Schriftart auf dem Computer vorhanden ist, der die Datei empfängt. Weitere Informationen finden Sie unter [Referenz zum Einbetten von Schriftarten.](../gdi/font-embedding-reference.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internationale Schriftartenenumeration und -auswahl](using-international-fonts-and-text.md)
</dt> <dt>

[Verwenden von MS Shell Dlg und MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md)
</dt> <dt>

[Referenz zum Einbetten von Schriftarten](../gdi/font-embedding-reference.md)
</dt> </dl>

 

 
