---
description: Sie können alle Informationen, die zum Konfigurieren von Software in Systemsteuerung erforderlich sind, durch Festlegen der Werte bestimmter Installereigenschaften im Paket Windows Installer Ihrer Anwendung zur Verfügung stellen.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Konfigurieren des Hinzufügens/Entfernens von Programmen mit Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48ad8499d395ffc4a5aad5491883f9c3161b78a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465487"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a>Konfigurieren des Hinzufügens/Entfernens von Programmen mit Windows Installer

Sie können alle Informationen, die zum Konfigurieren von Software in Systemsteuerung erforderlich sind, durch Festlegen der Werte bestimmter Installereigenschaften im Paket Windows Installer Ihrer Anwendung zur Verfügung stellen. Wenn Sie diese Eigenschaften festlegen, werden die entsprechenden Werte automatisch in die Registrierung schreibt. Wenn das Installationsprogramm erkennt, dass das Produkt zum vollständigen Entfernen markiert ist, werden dem Skript automatisch Vorgänge hinzugefügt, um den Ordner Programme hinzufügen/entfernen in Systemsteuerung Informationen für das Produkt zu entfernen.

Wenn eine Anwendung nicht registriert ist, wird sie nicht unter Programme hinzufügen/entfernen in Systemsteuerung. Weitere Informationen finden Sie unter [Hinzufügen und Entfernen einer Anwendung und Verlassen einer Ablaufverfolgung in der Registrierung.](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)

Anwendungen, die im Benutzerinstallationskontext [](installation-context.md) installiert wurden, werden in den Add/Remove-Programmen des aktuellen Benutzers angezeigt. Anwendungen, die im Installationskontext pro Computer installiert wurden, werden in den Add/Remove-Programmen aller Benutzer angezeigt. Anwendungen, die nicht pro Computer installiert wurden und nur als benutzerspezifische Anwendungen für andere Benutzer als den aktuellen Benutzer installiert wurden, werden nicht in den Add/Remove-Programmen des aktuellen Benutzers angezeigt.

Beachten Sie, dass Installationspakete, die die [**LIMITUI-Eigenschaft**](limitui.md) verwenden, auch [**ARPNOMODIFY enthalten müssen.**](arpnomodify.md) Dies ist erforderlich, damit ein Benutzer beim Versuch, ein Produkt zu konfigurieren, das richtige Verhalten von "Programme hinzufügen/entfernen" in Systemsteuerung-Hilfsprogramm abrufen kann.

Das Installationsprogramm verwendet die folgenden [öffentlichen Eigenschaften,](public-properties.md) um Das Hinzufügen/Entfernen von Programmen in Systemsteuerung.


| Eigenschaftenname | Kurze Beschreibung der Eigenschaft | 
|---------------|-------------------------------|
| <a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a> | URL des Updatekanals für die Anwendung. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Registrierungsschlüssel deinstallieren schreibt.</a> | 
| <a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a> | Stellt Kommentare für das Hinzufügen/Entfernen von Programmen im Systemsteuerung. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Registrierungsschlüssel deinstallieren schreibt.</a> | 
| <a href="arpcontact.md"><strong>ARPCONTACT</strong></a> | Stellt den Kontakt zum Hinzufügen/Entfernen von Programmen im Systemsteuerung. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Registrierungsschlüssel deinstallieren schreibt.</a> | 
| <a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a> | Vollqualifizierter Pfad zum primären Ordner der Anwendung. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Registrierungsschlüssel deinstallieren schreibt.</a> | 
| <a href="arphelplink.md"><strong>ARPHELPLINK</strong></a> | Internetadresse oder URL für technischen Support. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Registrierungsschlüssel deinstallieren schreibt.</a> | 
| <a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a> | Telefonnummern des technischen Support. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Registrierungsschlüssel deinstallieren schreibt.</a> | 
| <a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a> | Verhindert die Anzeige einer Schaltfläche "Ändern" für das Produkt in "Programme hinzufügen/entfernen" im Systemsteuerung.<blockquote><b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus. Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder die Programmierschnittstelle zu reparieren, bei Bedarf zu installieren und zu deinstallieren.</blockquote><br /> | 
| <a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a> | Verhindert die Anzeige einer Schaltfläche Entfernen für das Produkt im Bereich Programme hinzufügen/entfernen im Systemsteuerung. Das Produkt kann weiterhin entfernt werden, indem Sie auf die Schaltfläche Ändern klicken, wenn das Installationspaket mit einer Benutzeroberfläche erstellt wurde, die das Entfernen von Produkten als Option ermöglicht.<blockquote><b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus. Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder die Programmierschnittstelle zu reparieren, bei Bedarf zu installieren und zu deinstallieren.</blockquote><br /> | 
| <a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a> | Deaktiviert die Schaltfläche Reparieren im Bereich Programme hinzufügen/entfernen im Systemsteuerung.<blockquote><b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus. Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder die Programmierschnittstelle zu reparieren, bei Bedarf zu installieren und zu deinstallieren.</blockquote><br /> | 
| <a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a> | Identifiziert das Symbol, das unter Programme hinzufügen/entfernen angezeigt wird. Wenn diese Eigenschaft nicht definiert ist, gibt Software das Anzeigesymbol an. | 
| <a href="arpreadme.md"><strong>ARPREADME</strong></a> | Stellt die ReadMe für Das Hinzufügen/Entfernen von Programmen in Systemsteuerung. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Registrierungsschlüssel deinstallieren schreibt.</a> | 
| <a href="arpsize.md"><strong>ARPSIZE</strong></a> | Geschätzte Größe der Anwendung in KB. | 
| <a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a> | Verhindert die Anzeige der Anwendung in der Programmliste der Programme im Systemsteuerung.<blockquote><b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus. Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder die Programmierschnittstelle zu reparieren, bei Bedarf zu installieren und zu deinstallieren.</blockquote><br /> | 
| <a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a> | URL für die Startseite der Anwendung. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Registrierungsschlüssel deinstallieren schreibt.</a> | 
| <a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a> | URL für Informationen zum Anwendungsupdate. Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Registrierungsschlüssel deinstallieren schreibt.</a> | 


> [!Note]  
> Informationen zum Set Program and Defaults-Tool finden Sie im Abschnitt Working with Set Program Access and Computer Defaults (Arbeiten mit Set [Program Access and Computer Defaults).](/previous-versions//bb776877(v=vs.85))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deinstallieren des Registrierungsschlüssels](uninstall-registry-key.md)
</dt> </dl>
