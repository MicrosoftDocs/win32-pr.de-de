---
description: Sie können alle Informationen bereitstellen, die zum Konfigurieren von Software in Systemsteuerung erforderlich sind, indem Sie die Werte bestimmter Installationseigenschaften im Windows Installer-Paket Ihrer Anwendung festlegen.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Konfigurieren von "Programme hinzufügen/entfernen" mit Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99e1393eb586cfe1067840e4622fddd777a84512f55f9e82f7c9fad3b1f5688f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638749"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a>Konfigurieren von "Programme hinzufügen/entfernen" mit Windows Installer

Sie können alle Informationen bereitstellen, die zum Konfigurieren von Software in Systemsteuerung erforderlich sind, indem Sie die Werte bestimmter Installationseigenschaften im Windows Installer-Paket Ihrer Anwendung festlegen. Durch Festlegen dieser Eigenschaften werden die entsprechenden Werte automatisch in die Registrierung geschrieben. Wenn das Installationsprogramm erkennt, dass das Produkt für die vollständige Entfernung markiert ist, werden dem Skript automatisch Vorgänge hinzugefügt, um den Ordner Software in Systemsteuerung Informationen für das Produkt zu entfernen.

Wenn eine Anwendung nicht registriert ist, wird sie unter Software in Systemsteuerung nicht aufgeführt. Weitere Informationen finden Sie unter [Hinzufügen und Entfernen einer Anwendung und Belassen einer Ablaufverfolgung in der Registrierung.](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)

Anwendungen, die im [Installationskontext](installation-context.md) pro Benutzer installiert wurden, werden in den Programmen zum Hinzufügen/Entfernen des aktuellen Benutzers angezeigt. Anwendungen, die im Installationskontext pro Computer installiert wurden, werden in den Programmen zum Hinzufügen/Entfernen aller Benutzer angezeigt. Anwendungen, die nicht pro Computer installiert wurden und nur als benutzerspezifische Anwendungen für andere Benutzer als den aktuellen Benutzer installiert wurden, werden nicht in den Programmen hinzufügen/entfernen des aktuellen Benutzers angezeigt.

Beachten Sie, dass Installationspakete, die die [**LIMITUI-Eigenschaft**](limitui.md) verwenden, auch [**ARPNOMODIFY**](arpnomodify.md)enthalten müssen. Dies ist erforderlich, damit ein Benutzer beim Versuch, ein Produkt zu konfigurieren, das richtige Verhalten von Software in Systemsteuerung Hilfsprogramm abrufen kann.

Das Installationsprogramm verwendet die folgenden [öffentlichen Eigenschaften,](public-properties.md) um Software in Systemsteuerung zu verwalten.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschaftenname</th>
<th>Kurze Beschreibung der Eigenschaft</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></td>
<td>URL des Updatekanals für die Anwendung. Der Wert, den das Installationsprogramm unter <a href="uninstall-registry-key.md">dem Registrierungsschlüssel deinstallieren</a>schreibt.</td>
</tr>
<tr class="even">
<td><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></td>
<td>Stellt Kommentare für das Hinzufügen/Entfernen von Programmen im Systemsteuerung bereit. Der Wert, den das Installationsprogramm unter <a href="uninstall-registry-key.md">dem Registrierungsschlüssel deinstallieren</a>schreibt.</td>
</tr>
<tr class="odd">
<td><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></td>
<td>Stellt den Kontakt für "Programme hinzufügen/entfernen" im Systemsteuerung bereit. Der Wert, den das Installationsprogramm unter <a href="uninstall-registry-key.md">dem Registrierungsschlüssel deinstallieren</a>schreibt.</td>
</tr>
<tr class="even">
<td><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></td>
<td>Vollqualifizierten Pfad zum primären Ordner der Anwendung. Der Wert, den das Installationsprogramm unter <a href="uninstall-registry-key.md">dem Registrierungsschlüssel deinstallieren</a>schreibt.</td>
</tr>
<tr class="odd">
<td><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></td>
<td>Internetadresse oder URL für technischen Support. Der Wert, den das Installationsprogramm unter <a href="uninstall-registry-key.md">dem Registrierungsschlüssel deinstallieren</a>schreibt.</td>
</tr>
<tr class="even">
<td><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></td>
<td>Telefonnummern des technischen Supports. Der Wert, den das Installationsprogramm unter <a href="uninstall-registry-key.md">dem Registrierungsschlüssel deinstallieren</a>schreibt.</td>
</tr>
<tr class="odd">
<td><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></td>
<td>Verhindert die Anzeige einer Änderungsschaltfläche für das Produkt unter Software im Systemsteuerung.
<blockquote>
<b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus. Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder die Programmierschnittstelle zu reparieren, bei Bedarf zu installieren und zu deinstallieren.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></td>
<td>Verhindert die Anzeige einer Schaltfläche Entfernen für das Produkt in den Programmen hinzufügen/entfernen im Systemsteuerung. Das Produkt kann weiterhin entfernt werden, indem Sie die Schaltfläche Ändern auswählen, wenn das Installationspaket mit einer Benutzeroberfläche erstellt wurde, die das Entfernen von Produkten als Option ermöglicht.
<blockquote>
<b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus. Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder die Programmierschnittstelle zu reparieren, bei Bedarf zu installieren und zu deinstallieren.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></td>
<td>Deaktiviert die Schaltfläche Reparieren in den Programmen hinzufügen/entfernen im Systemsteuerung.
<blockquote>
<b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus. Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder die Programmierschnittstelle zu reparieren, bei Bedarf zu installieren und zu deinstallieren.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></td>
<td>Identifiziert das Symbol, das unter Software angezeigt wird. Wenn diese Eigenschaft nicht definiert ist, gibt Add/Remove Programs das Anzeigesymbol an.</td>
</tr>
<tr class="odd">
<td><a href="arpreadme.md"><strong>ARPREADME</strong></a></td>
<td>Stellt die ReadMe für Software in Systemsteuerung bereit. Der Wert, den das Installationsprogramm unter <a href="uninstall-registry-key.md">dem Registrierungsschlüssel deinstallieren</a>schreibt.</td>
</tr>
<tr class="even">
<td><a href="arpsize.md"><strong>ARPSIZE</strong></a></td>
<td>Geschätzte Größe der Anwendung in KB.</td>
</tr>
<tr class="odd">
<td><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></td>
<td>Verhindert die Anzeige der Anwendung in der Programmliste der Software im Systemsteuerung.
<blockquote>
<b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus. Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder die Programmierschnittstelle zu reparieren, bei Bedarf zu installieren und zu deinstallieren.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></td>
<td>URL für die Startseite der Anwendung. Der Wert, den das Installationsprogramm unter <a href="uninstall-registry-key.md">dem Registrierungsschlüssel deinstallieren</a>schreibt.</td>
</tr>
<tr class="odd">
<td><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></td>
<td>URL für Anwendungsupdateinformationen. Der Wert, den das Installationsprogramm unter <a href="uninstall-registry-key.md">dem Registrierungsschlüssel deinstallieren</a>schreibt.</td>
</tr>
</tbody>
</table>

> [!Note]  
> Informationen zum Tool "Programm und Standardwerte festlegen" finden Sie im Abschnitt [Arbeiten mit Programmzugriff festlegen und Computerstandardeinstellungen.](/previous-versions//bb776877(v=vs.85))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deinstallieren des Registrierungsschlüssels](uninstall-registry-key.md)
</dt> </dl>
