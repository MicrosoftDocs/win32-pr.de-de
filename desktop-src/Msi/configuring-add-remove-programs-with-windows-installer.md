---
description: Sie können alle Informationen bereitstellen, die zum Konfigurieren von Software in der Systemsteuerung erforderlich sind, indem Sie die Werte bestimmter Installer-Eigenschaften im Windows Installer Paket der Anwendung festlegen.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Konfigurieren von "Programme hinzufügen/entfernen" mit Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6850163e18af94aa9cceaf6c4bb2e8059dcf2121
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/30/2021
ms.locfileid: "106372535"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a>Konfigurieren von "Programme hinzufügen/entfernen" mit Windows Installer

Sie können alle Informationen bereitstellen, die zum Konfigurieren von Software in der Systemsteuerung erforderlich sind, indem Sie die Werte bestimmter Installer-Eigenschaften im Windows Installer Paket der Anwendung festlegen. Durch Festlegen dieser Eigenschaften werden die entsprechenden Werte automatisch in die Registrierung geschrieben. Wenn das Installationsprogramm erkennt, dass das Produkt zum Abschluss der Löschung markiert ist, werden die Vorgänge automatisch dem Skript hinzugefügt, um den Ordner Software in den System Steuerungsinformationen für das Produkt zu entfernen.

Wenn eine Anwendung nicht registriert ist, wird Sie in der Systemsteuerung unter Software nicht aufgeführt. Weitere Informationen finden Sie unter [Hinzufügen und Entfernen einer Anwendung und belassen der Registrierung in der Registrierung](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).

Anwendungen, die im Einzelbenutzer [Installations Kontext](installation-context.md) installiert wurden, werden in der Option Software des aktuellen Benutzers angezeigt. Anwendungen, die im Installations Kontext pro Computer installiert wurden, werden in den Programmen Software aller Benutzer angezeigt. Anwendungen, die nicht pro Computer installiert wurden und nur als benutzerspezifische Anwendungen für andere Benutzer als den aktuellen Benutzer installiert wurden, werden nicht in den Programmen zum Hinzufügen/Entfernen des aktuellen Benutzers angezeigt.

Beachten Sie, dass Installationspakete, die die [**limitui**](limitui.md) -Eigenschaft verwenden, auch das [**arpnomodify**](arpnomodify.md)-Objekt enthalten müssen. Dies ist erforderlich, damit ein Benutzer das richtige Verhalten von der System Steuerungs Option "Software" beim Versuch, ein Produkt zu konfigurieren, erhält.

Das Installationsprogramm verwendet die folgenden [öffentlichen Eigenschaften](public-properties.md) zum Verwalten von Software in der Systemsteuerung.

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
<td><a href="arpauthorizedcdfprefix.md"><strong>Arpauthorizedcdfprefix</strong></a></td>
<td>Die URL des Aktualisierungs Kanals für die Anwendung. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</td>
</tr>
<tr class="even">
<td><a href="arpcomments.md"><strong>Arpcomments</strong></a></td>
<td>Enthält Kommentare für die Option Software in der Systemsteuerung. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</td>
</tr>
<tr class="odd">
<td><a href="arpcontact.md"><strong>Arpcontact</strong></a></td>
<td>Stellt den Kontakt zum Hinzufügen/Entfernen von Programmen in der Systemsteuerung bereit. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</td>
</tr>
<tr class="even">
<td><a href="arpinstalllocation.md"><strong>Arpinstalllocation</strong></a></td>
<td>Voll qualifizierter Pfad zum primären Ordner der Anwendung. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</td>
</tr>
<tr class="odd">
<td><a href="arphelplink.md"><strong>Arphelplink</strong></a></td>
<td>Internet Adresse (URL), um technischen Support zu erhalten. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</td>
</tr>
<tr class="even">
<td><a href="arphelptelephone.md"><strong>Arphelptelefon</strong></a></td>
<td>Telefonnummern für technischen Support. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</td>
</tr>
<tr class="odd">
<td><a href="arpnomodify.md"><strong>Arpnomodify</strong></a></td>
<td>Verhindert, dass die Schaltfläche "ändern" für das Produkt in der Systemsteuerung unter "Software" angezeigt wird.
<blockquote>
<b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus. Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder über die Programmierschnittstelle zu reparieren, zu installieren und zu deinstallieren.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></td>
<td>Verhindert die Anzeige einer Entfernungs Schaltfläche für das Produkt in den Programmen "Software" in der Systemsteuerung. Das Produkt kann trotzdem entfernt werden, indem Sie die Schaltfläche ändern auswählen, wenn das Installationspaket mit einer Benutzeroberfläche erstellt wurde, die das Produkt entfernen als Option ermöglicht.
<blockquote>
<b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus. Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder über die Programmierschnittstelle zu reparieren, zu installieren und zu deinstallieren.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="arpnorepair.md"><strong>Arpnorepair</strong></a></td>
<td>Deaktiviert die Schaltfläche reparieren in der Systemsteuerung unter Software.
<blockquote>
<b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus. Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder über die Programmierschnittstelle zu reparieren, zu installieren und zu deinstallieren.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpproducticon.md"><strong>Arpproducticon</strong></a></td>
<td>Identifiziert das Symbol, das unter "Software" angezeigt wird. Wenn diese Eigenschaft nicht definiert ist, gibt Add/Remove Software das Anzeige Symbol an.</td>
</tr>
<tr class="odd">
<td><a href="arpreadme.md"><strong>Arpreadme</strong></a></td>
<td>Stellt die Info für "Software" in der Systemsteuerung bereit. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</td>
</tr>
<tr class="even">
<td><a href="arpsize.md"><strong>Arpsize</strong></a></td>
<td>Geschätzte Größe der Anwendung in KB.</td>
</tr>
<tr class="odd">
<td><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></td>
<td>Verhindert, dass die Anwendung in der Liste Programme der Option Software in der Systemsteuerung angezeigt wird.
<blockquote>
<b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus. Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder über die Programmierschnittstelle zu reparieren, zu installieren und zu deinstallieren.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpurlinfoabout.md"><strong>Arpurlinfoabout</strong></a></td>
<td>URL für die Startseite der Anwendung. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</td>
</tr>
<tr class="odd">
<td><a href="arpurlupdateinfo.md"><strong>Arpurlupdateinfo</strong></a></td>
<td>URL für Anwendungs Update Informationen. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</td>
</tr>
</tbody>
</table>

> [!Note]  
> Weitere Informationen zum Tool Set Program und defaults finden Sie im Abschnitt [Arbeiten mit Festlegen des Programm Zugriffs und der Standardeinstellungen für Computer](/previous-versions//bb776877(v=vs.85)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierungsschlüssel deinstallieren](uninstall-registry-key.md)
</dt> </dl>
