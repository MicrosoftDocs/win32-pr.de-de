---
description: Die Informationen in diesem Thema identifizieren die Ergänzungen und Änderungen, die in Windows Installer&\# 160; 5.0 verfügbar sind.
ms.assetid: c088c15b-0eef-4a92-bb65-e7fe871afbfe
title: Neues in Windows Installer 5,0
ms.topic: article
ms.date: 11/08/2019
ms.openlocfilehash: ae7986cec60341127ab00ad08a3032aad80209bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861891"
---
# <a name="whats-new-in-windows-installer-50"></a>Neues in Windows Installer 5,0

Die Informationen in diesem Thema identifizieren die Ergänzungen und Änderungen, die in Windows Installer 5,0 verfügbar sind.

Windows Installer 5,0 ist in den folgenden Versionen von Windows enthalten:

* Client: Windows 7 und alle späteren Versionen.
* Server: Windows Server 2008 R2 und alle späteren Versionen.

> [!NOTE]
> Es ist kein verteilbares für Windows Installer 5,0 vorhanden. Eine Liste der verteilbaren Komponenten, die für frühere Versionen von Windows Installer verfügbar sind, finden Sie unter [Windows Installer weiterverweiterungs Tabellen](windows-installer-redistributables.md). Eine umfassende Liste der Windows Installer Versionen finden Sie unter [veröffentlichte Versionen von Windows Installer](released-versions-of-windows-installer.md).

Diese Seite wird als Leitfaden für die-Dokumentation bereitgestellt. Informationen zu den tatsächlichen Betriebssystemanforderungen finden Sie im Abschnitt "Anforderungen" auf den Haupt Referenzseiten. Teile der Windows Installer, die von dieser Seite aus nicht verknüpft sind, sind möglicherweise in einer anderen Version des Windows Installer verfügbar. Weitere Informationen zu anderen Windows Installer Versionen finden Sie unter [What es New in Windows Installer](what-s-new-in-windows-installer.md).

[Standard Aktionen](standard-actions.md)

-   [Msikonfigurireservices](msiconfigureservices-action.md)

[Installer-Funktionen](installer-functions.md)

-   [**Msienumschlag**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
-   [**Msienumschlag clientsex**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
-   [**Msigetcomponentpathex**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)

[Spaltendatentypen](column-data-types.md)

-   [**Formattedsddltext**](formattedsddltext.md)

[Eigenschaften](properties.md)

-   [**Msifastinstall**](msifastinstall.md)
-   [**Msiinstallperuser**](msiinstallperuser.md)

[Eigenschaften von Zusammenfassungs Informationen](summary-information-stream-reference.md)

-   Die [**Vorlagen Zusammenfassung**](template-summary.md) enthält neue Werte, mit denen angegeben wird, dass die Datenbank mit Windows RT oder der Arm64-Plattform kompatibel ist.

[Datenbanktabellen](database-tables.md)

-   [Msiserviceconfig-Tabelle](msiserviceconfig-table.md)
-   [Msiserviceconfigfailureactions-Tabelle](msiserviceconfigfailureactions-table.md)
-   [Msishortcutproperty-Tabelle](msishortcutproperty-table.md)
-   [Msilockpermissionsex-Tabelle](msilockpermissionsex-table.md)

[ControlEvents](control-events.md)

-   [Msiprint ControlEvent](msiprint-controlevent.md)
-   [Msilaunchapp ControlEvent](msilaunchapp-controlevent.md)

[Steuerelemente](controls.md)

-   [Hyperlink-Steuerelement](hyperlink-control.md)

[Interne Konsistenz Auswertung-ICES](internal-consistency-evaluators-ices.md)

-   [ICE101](ice-101.md)
-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Automatisierungsschnittstelle](automation-interface.md)

-   Eigenschaften des [ **Installerobjekts**](installer-object.md)

    -   [**Installer. clientsex**](installer-clientsex.md)
    -   [**Installer. componentsex**](installer-componentsex.md)
    -   [**Installer. componentpathex**](installer-componentpathex.md)

-   Eigenschaften des [ **Komponenten Objekts**](components.md)

    -   [**Components. componentcode**](component-componentcode.md)
    -   [**Komponenten. UserSID**](component-usersid.md)
    -   [**Komponenten. Context**](component-context.md)

-   Eigenschaften des [ **Client Objekts**](client.md)

    -   [**Client. ProductCode**](client-productcode.md)
    -   [**Client. componentcode**](client-componentcode.md)
    -   [**Client. UserSID**](client-usersid.md)
    -   [**Client. Context**](client-context.md)

-   Eigenschaften des [**ComponentInfo**](componentinfo.md) -Objekts

    -   [**ComponentInfo. componentcode**](componentinfo-componentcode.md)
    -   [**ComponentInfo. Path**](componentinfo-path.md)
    -   [**ComponentInfo. State**](componentinfo-state.md)

## <a name="notes"></a>Notizen

Setup Entwickler können Windows Installer 5,0 verwenden, um ein einzelnes Installationspaket zu erstellen, das entweder pro Computer oder pro Benutzer Installation der Anwendung unterstützt wird. Weitere Informationen finden Sie unter [Erstellen eines einzelnen Pakets](single-package-authoring.md). Die interne Konsistenz Auswertung [ICE105](ice-105.md) überprüft, ob das Paket für die Installation in einem Benutzer bezogenen Kontext erstellt wurde. Eine Anwendung, die von einem Standardbenutzer ohne Rechte Erweiterung installiert, aktualisiert, ausgeführt und entfernt werden kann, wird als Per-User Anwendung (Pua) bezeichnet. Ein Pua kann eine bessere Benutzeroberfläche bereitstellen, die Auswirkungen auf das System und andere Benutzer des Computers minimieren und die UAC-Eingabeaufforderung für Situationen reserviert, in denen die Rechte des Benutzers tatsächlich erhöht werden müssen. Die einzelnen Paket Erstellungs Funktionen von Windows Installer 5,0 können die Entwicklung von Per-User Anwendungen vereinfachen.

Mit den Konfigurationsoptionen für Dienste kann ein Windows Installer Paket die [Dienste](../services/services.md) auf einem Computer anpassen. Weitere Informationen finden Sie unter [Verwenden der Dienst Konfiguration](using-services-configuration.md).

Ab Windows Installer 5,0 ist ein Windows Installer Paket in der Lage, neue Konten, Windows- [Dienste](../services/services.md), Dateien, Ordner und Registrierungsschlüssel zu sichern. Die [msilockpermissionsex](msilockpermissionsex-table.md) -Tabelle kann eine Sicherheits Beschreibung angeben, die Berechtigungen ablehnt, die Vererbung von Berechtigungen für eine übergeordnete Ressource angibt oder die Berechtigungen eines neuen Kontos angibt. Weitere Informationen finden Sie unter [Sichern von Ressourcen](securing-resources-.md).

Windows Installer 5,0 können alle auf dem Computer installierten Komponenten auflisten und den Schlüssel Pfad für die Komponente abrufen. Weitere Informationen finden Sie unter [Enumerieren von Komponenten](enumerating-components-.md).

Windows Installer 5,0, die unter Windows Server 2012 oder Windows 8 ausgeführt wird, unterstützt die Installation genehmigter apps auf Windows RT. Ein Windows Installer Paket, ein Patch oder eine Transformation, die nicht von Microsoft signiert wurde, kann unter Windows RT nicht installiert werden. Die [**Template-Übersichts**](template-summary.md) Eigenschaft gibt die Plattform an, die mit der Installations Datenbank kompatibel ist und den Wert für Windows RT enthalten sollte.

Windows Installer 5,0 unter Windows 10 auf Arm64-Prozessoren unterstützt die Installation von Anwendungen, die speziell für die Arm64-Plattform kompiliert wurden.  Die [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaft dieser Pakete muss den Wert Arm64 einschließen. 

 
