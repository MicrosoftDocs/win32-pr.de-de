---
description: Ein Installer-Objekt muss anfänglich erstellt werden, um die Automatisierungsunterstützung zu laden, die für com den Zugriff auf die Installationsfunktionen benötigt. Dieses Objekt stellt Wrapper zum Erstellen der Objekte der obersten Ebene und zum Zugreifen auf ihre Methoden bereit.
ms.assetid: fefc3e39-073e-4869-86b7-27d20a3b337b
title: Installer-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4afddcce55a739ad322be10c736a6e9119f5c9eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367537"
---
# <a name="installer-object"></a>Installer-Objekt

Ein **Installer** -Objekt muss anfänglich erstellt werden, um die Automatisierungsunterstützung zu laden, die für com den Zugriff auf die Installationsfunktionen benötigt. Dieses Objekt stellt Wrapper zum Erstellen der Objekte der obersten Ebene und zum Zugreifen auf ihre Methoden bereit.

Sie können das **Installer** -Objekt aus der ProgID "WindowsInstaller. Installer" erstellen.

## <a name="members"></a>Member

Das **Installer** -Objekt verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Installer** -Objekt verfügt über diese Methoden.



| Methode                                                                   | BESCHREIBUNG                                                                                                                                                                                     |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addsource**](installer-addsource.md)                                 | Fügt der Liste der gültigen Netzwerk Quellen in der SourceList eine Quelle hinzu.<br/>                                                                                                                |
| [**Werbung Product**](installer-advertiseproduct.md)                   | Gibt ein Installationspaket an.<br/>                                                                                                                                                  |
| [**Werbung**](installer-advertisescript.md)                     | Gibt ein Installationspaket an. <br/>                                                                                                                                                 |
| [**Applymultiplepatches**](installer-applymultiplepatches.md)           | Wendet ein oder mehrere Patches auf Produkte an, die zum Empfangen des Patches berechtigt sind. Legt die [**patcheigenschaft**](patch.md) auf den Pfad der bereitgestellten Patchpakete fest.<br/>                          |
| [**Applypatch**](installer-applypatch.md)                               | Ruft eine-Installation auf und legt die [**Patch**](patch.md) -Eigenschaft auf den Pfad des Patchpakets für jedes Produkt fest, das im Patchpaket als berechtigt zum Empfangen des Patches aufgeführt ist.<br/> |
| [**Clearsourcelist**](installer-clearsourcelist.md)                     | Entfernt alle Netzwerk Quellen aus der SourceList.<br/>                                                                                                                                     |
| [**Collectuserinfo**](installer-collectuserinfo.md)                     | Ruft eine Sequenz des Assistenten für die Benutzeroberfläche auf, die Benutzerinformationen und den Produktcode sammelt und speichert.<br/>                                                                        |
| [**Konfigurieren von Features**](installer-configurefeature.md)                   | Konfiguriert den installierten Status eines Produkt Features.<br/>                                                                                                                                 |
| [**Konfigurieren von Produkten**](installer-configureproduct.md)                   | Installiert oder deinstalliert ein Produkt.<br/>                                                                                                                                                    |
| [**"Kreatewerbung"**](installer-createadvertisescript.md)         | Generiert ein Ankündigungs Skript.<br/>                                                                                                                                                       |
| [**"Kreaterecord"**](installer-createrecord.md)                           | Gibt ein neues [**Daten Satz**](record-object.md) Objekt mit der angeforderten Anzahl von Feldern zurück.<br/>                                                                                            |
| [**EnableLog**](installer-enablelog.md)                                 | Aktiviert die Protokollierung des ausgewählten Nachrichten Typs für alle nachfolgenden Installations Sitzungen im aktuellen Prozessbereich.<br/>                                                                  |
| [**Extractpatchxmldata**](installer-extractpatchxmldata.md)             | Extrahiert Informationen aus einem Patch als XML-Zeichenfolge.<br/>                                                                                                                                  |
| [**FileHash**](installer-filehash.md)                                   | Nimmt den Pfad zu einer Datei an und gibt einen 128-Bit-Hash dieser Datei zurück.<br/>                                                                                                                    |
| [**Filesignatureinfo**](installer-filesignatureinfo.md)                 | Nimmt den Pfad zu einer Datei an und gibt ein **SAFEARRAY** von Bytes zurück, das den Hash oder das codierte Zertifikat darstellt.<br/>                                                                   |
| [**FileSize**](installer-filesize.md)                                   | Gibt die Größe der angegebenen Datei zurück.<br/>                                                                                                                                              |
| [**FileVersion**](installer-fileversion.md)                             | Gibt die Versions Zeichenfolge oder die sprach Zeichenfolge des angegebenen Pfads zurück.<br/>                                                                                                                 |
| [**Forcesourcelistresolution**](installer-forcesourcelistresolution.md) | Erzwingt, dass das Installationsprogramm die Quell Liste nach einer gültigen Produkt Quelle durchsucht, wenn eine Quelle das nächste Mal benötigt wird.<br/>                                                                        |
| [**Installproduct**](installer-installproduct.md)                       | Öffnet ein Installer-Paket und Initialisiert eine Installationssitzung.<br/>                                                                                                                  |
| [**Lasterrorrecord**](installer-lasterrorrecord.md)                     | Gibt ein [**Daten Satz**](record-object.md) Objekt zurück, das Fehler Parameter für den letzten Fehler der Funktion enthält, die den Fehler Daten Satz erzeugt hat.<br/>                          |
| [**OpenDatabase**](installer-opendatabase.md)                           | Öffnet eine vorhandene Datenbank oder erstellt eine neue Datenbank.<br/>                                                                                                                                     |
| [**OpenPackage**](installer-openpackage.md)                             | Öffnet ein Installer-Paket für die Verwendung mit Funktionen, die auf die Produktdatenbank und die Installations-Engine zugreifen.<br/>                                                                               |
| [**Openproduct**](installer-openproduct.md)                             | Öffnet ein Installationspaket für ein installiertes Produkt mit dem Produktcode.<br/>                                                                                                          |
| [**ProvideAssembly**](installer-provideassembly.md)                     | Gibt den installierten Pfad einer Assembly zurück.<br/>                                                                                                                                           |
| [**Providecomponent**](installer-providecomponent.md)                   | Gibt den vollständigen Komponenten Pfad zurück und führt jede erforderliche Installation aus.<br/>                                                                                                             |
| [**Providequalifiedcomponent**](installer-providequalifiedcomponent.md) | Gibt den vollständigen Komponenten Pfad zurück und führt jede erforderliche Installation aus.<br/>                                                                                                             |
| [**REGISTRYVALUE**](installer-registryvalue.md)                         | Liest Informationen zu einem angegebenen Registrierungsschlüssel des-Werts.<br/>                                                                                                                           |
| [**Reinstallfeature**](installer-reinstallfeature.md)                   | Neuinstallation von Features oder Behebung von Problemen mit installierten Funktionen.<br/>                                                                                                                    |
| [**Reinstallproduct**](installer-reinstallproduct.md)                   | Installiert ein Produkt neu oder korrigiert Installationsprobleme in einem installierten Produkt.<br/>                                                                                                      |
| [**Removepatches**](installer-removepatches.md)                         | Entfernt einen oder mehrere Patches zu Produkten, die zum Empfangen des Patches berechtigt sind. <br/>                                                                                                              |
| [**Usefeature**](installer-usefeature.md)                               | Erhöht den Verwendungs Zähler für eine bestimmte Funktion und gibt den Installationsstatus für diese Funktion zurück.<br/>                                                                             |



 

### <a name="properties"></a>Eigenschaften

Das **Installer** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                    | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clientsex**](installer-components.md)<br/>                        |                       | Gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das Produkte auflistet, die eine angegebene installierte Komponente verwenden.<br/> **[Windows Installer 4,5 und früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.<br/>       |
| [**Componentclients**](installer-componentclients.md)<br/>           |                       | Gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das den Satz von Clients einer angegebenen Komponente auflistet.<br/>                                                                                                                           |
| [**Componentpath**](installer-componentpath.md)<br/>                 |                       | Gibt den vollständigen Pfad zu einer installierten Komponente zurück.<br/>                                                                                                                                                                                            |
| [**Componentpathex**](installer-componentpathex.md)<br/>             |                       | Gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das den vollständigen Pfad einer angegebenen installierten Komponente enthält. <br/> **[Windows Installer 4,5 und früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.<br/>       |
| [**Componentqualifizierer**](installer-componentqualifiers.md)<br/>     |                       | Gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das den Satz registrierter Qualifizierer für die angegebene Komponente aufzählt.<br/>                                                                                                          |
| [**Komponenten**](installer-components.md)<br/>                       |                       | Gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das den Satz der installierten Komponenten für alle Produkte auflistet.<br/>                                                                                                                      |
| [**Componentsex**](installer-componentsex.md)<br/>                   |                       | Gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das installierte Komponenten auflistet.<br/> **[Windows Installer 4,5 und früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.<br/>                                    |
| [**Umgebung**](installer-environment.md)<br/>                     | Lesen/Schreiben<br/> | Der Zeichen folgen Wert für eine Umgebungsvariable des aktuellen Prozesses.<br/>                                                                                                                                                                        |
| [**Featuwiederent**](installer-featureparent.md)<br/>                 |                       | Gibt die übergeordnete Funktion einer Funktion an.<br/>                                                                                                                                                                                                  |
| [**Aspekte**](installer-features.md)<br/>                           |                       | Gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das den Satz veröffentlichter Funktionen für das angegebene Produkt auflistet.<br/>                                                                                                               |
| [**Featurestate**](installer-featurestate.md)<br/>                   |                       | Gibt den installierten Zustand einer Funktion zurück.<br/>                                                                                                                                                                                                   |
| [**Featureusagecount**](installer-featureusagecount.md)<br/>         |                       | Gibt an, wie oft die Funktion verwendet wurde.<br/>                                                                                                                                                                                 |
| [**Featureusagedate**](installer-featureusagedate.md)<br/>           |                       | Gibt das Datum zurück, an dem die angegebene Funktion zuletzt verwendet wurde.<br/>                                                                                                                                                                                  |
| [**File Attributes**](installer-fileattributes.md)<br/>               |                       | Gibt eine Zahl zurück, die die kombinierten Dateiattribute für den angegebenen Pfad zu einer Datei oder einem Ordner darstellt.<br/>                                                                                                                                  |
| [**Pat**](installer-patches.md)<br/>                             |                       | Gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das alle auf das Produkt angewendeten Patches enthält.<br/>                                                                                                                              |
| [**Patchesex**](installer-patchesex.md)<br/>                         |                       | Listet eine Auflistung von [**Patch**](patch-object.md) -Objekten auf.<br/>                                                                                                                                                                           |
| [**Patchdateien**](installer-patchfiles.md)<br/>                       |                       | Gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das eine Liste von Dateien enthält, die durch die bereitgestellte Liste der Patches aktualisiert werden können.<br/>                                                                                                 |
| [**Patchinfo**](installer-patchinfo.md)<br/>                         |                       | Gibt Informationen zu einem Patch zurück.<br/>                                                                                                                                                                                                          |
| [**Patchtransformationen**](installer-patchtransforms.md)<br/>             |                       | Gibt die durch Semikolons getrennte Liste von Transformationen zurück, die sich im angegebenen Patchpaket befinden und auf das angegebene Produkt angewendet werden.<br/>                                                                                                            |
| [**Productelevated**](installer-productelevated.md)<br/>             |                       | Gibt true zurück, wenn das Produkt verwaltet wird, oder false, wenn das Produkt nicht verwaltet wird.<br/>                                                                                                                                                              |
| [**ProductInfo**](installer-productinfo.md)<br/>                     |                       | Gibt den Wert des angegebenen Attributs für ein installiertes oder veröffentlichtes Produkt zurück.<br/>                                                                                                                                                         |
| [**Productinfofromscript**](installer-productinfofromscript.md)<br/> |                       | Gibt den Wert des angegebenen Attributs zurück, das in einem Ankündigungs Skript gespeichert ist.<br/>                                                                                                                                                         |
| [**Produkte**](installer-products.md)<br/>                           |                       | Gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das den Satz aller Produkte auflistet, die für den aktuellen Benutzer und Computer installiert oder angekündigt wurden. <br/>                                                                                     |
| [**Productsex**](installer-productsex.md)<br/>                       |                       | Listet eine Auflistung von [**Product**](product-object.md) -Objekten auf.<br/>                                                                                                                                                                       |
| [**ProductState**](installer-productstate-property.md)<br/>          |                       | Gibt die Installations Zustandsinformationen für ein Produkt zurück.<br/>                                                                                                                                                                                        |
| [**Qualifierdescription**](installer-qualifierdescription.md)<br/>   |                       | Gibt eine Text Zeichenfolge zurück, die die qualifizierte Komponente beschreibt.<br/>                                                                                                                                                                               |
| [**RelatedProducts ein**](installer-relatedproducts.md)<br/>             |                       | Gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das den Satz aller Produkte auflistet, die für den aktuellen Benutzer und Computer mit einer angegebenen [**UpgradeCode**](upgradecode.md) -Eigenschaft in der Eigenschaften Tabelle installiert oder angekündigt wurden.<br/> |
| [**ShortcutTarget**](installer-shortcuttarget.md)<br/>               |                       | Untersucht eine Verknüpfung und gibt das Produkt, den Funktionsnamen und die Komponente zurück, falls verfügbar.<br/>                                                                                                                                                       |
| [**SummaryInformation**](installer-summaryinformation.md)<br/>       |                       | Gibt ein [**SummaryInfo**](summaryinfo-object.md) -Objekt zurück, das zum Überprüfen, aktualisieren und Hinzufügen von Eigenschaften zum Zusammenfassungs Informationsdaten Strom eines Pakets oder einer Transformation verwendet werden kann.<br/>                                                              |
| [**UILevel**](installer-uilevel.md)<br/>                             | Lesen/Schreiben<br/> | Gibt den Typ der Benutzeroberfläche an, die verwendet werden soll, wenn nachfolgende Pakete im aktuellen Prozessbereich geöffnet und verarbeitet werden.<br/>                                                                                                           |
| [**Version**](installer-version.md)<br/>                             |                       | Gibt die Zeichen folgen Darstellung der aktuellen Version von Windows Installer zurück.<br/>                                                                                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden der Automatisierungsschnittstelle](using-the-automation-interface.md)
</dt> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




