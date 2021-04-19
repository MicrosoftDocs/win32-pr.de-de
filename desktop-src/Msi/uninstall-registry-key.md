---
description: Eine Liste der Windows Installer Eigenschaften, die Werte unter dem Deinstallations Registrierungsschlüssel enthalten.
ms.assetid: f831cc62-4b19-4285-8bb1-6080567ac985
title: Windows Installer Eigenschaften für den Registrierungsschlüssel "deinstallieren"
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: 90174cabed7a1d9ff0ca21b532c459a1026787a6
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/30/2021
ms.locfileid: "106365450"
---
# <a name="windows-installer-properties-for-the-uninstall-registry-key"></a>Windows Installer Eigenschaften für den Registrierungsschlüssel "deinstallieren"

Die folgenden Installer-Eigenschaften haben die Werte, die unter dem Registrierungsschlüssel geschrieben werden:

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall**

Die Werte werden in einem Unterschlüssel gespeichert, der durch die Produktcode-GUID der Anwendung identifiziert wird.



| Wert               | Windows Installer-Eigenschaft                                                                                                                                                                                                                                                                                                                                           |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName         | [**ProductName**](productname.md) -Eigenschaft                                                                                                                                                                                                                                                                                                                          |
| DisplayVersion      | Abgeleitet von der [**ProductVersion**](productversion.md) -Eigenschaft                                                                                                                                                                                                                                                                                                       |
| Publisher           | [**Hersteller**](manufacturer.md) Eigenschaft                                                                                                                                                                                                                                                                                                                        |
| VersionMinor        | Abgeleitet von der [**ProductVersion**](productversion.md) -Eigenschaft                                                                                                                                                                                                                                                                                                       |
| VersionMajor        | Abgeleitet von der [**ProductVersion**](productversion.md) -Eigenschaft                                                                                                                                                                                                                                                                                                       |
| Version             | Abgeleitet von der [**ProductVersion**](productversion.md) -Eigenschaft                                                                                                                                                                                                                                                                                                       |
| HelpLink            | [**Arphelplink**](arphelplink.md) (Eigenschaft)                                                                                                                                                                                                                                                                                                                          |
| Helpdesk       | [**Arphelptelephone**](arphelptelephone.md) (Eigenschaft)                                                                                                                                                                                                                                                                                                                |
| InstallDate         | Der letzte Zeitpunkt, zu dem dieser Produkt Dienst empfangen hat. Der Wert dieser Eigenschaft wird bei jedem anwenden oder Entfernen eines Patches aus dem Produkt ersetzt, oder die [Befehlszeilen Option](command-line-options.md) /v wird verwendet, um das Produkt zu reparieren. Wenn das Produkt keine Reparaturen oder Patches erhalten hat, enthält diese Eigenschaft den Zeitpunkt, zu dem dieses Produkt auf diesem Computer installiert wurde. |
| InstallLocation     | [**Arpinstalllocation**](arpinstalllocation.md) (Eigenschaft)                                                                                                                                                                                                                                                                                                            |
| InstallSource       | [**SourceDir**](sourcedir.md) -Eigenschaft                                                                                                                                                                                                                                                                                                                              |
| Urlinfoabout        | [**Arpurlinfoabout**](arpurlinfoabout.md) (Eigenschaft)                                                                                                                                                                                                                                                                                                                  |
| Urlupdateinfo       | [**Arpurlupdateinfo**](arpurlupdateinfo.md) (Eigenschaft)                                                                                                                                                                                                                                                                                                                |
| AuthorizedCDFPrefix | [**Arpauthorizedcdfprefix**](arpauthorizedcdfprefix.md) (Eigenschaft)                                                                                                                                                                                                                                                                                                    |
| Kommentare            | [**Arpcomments**](arpcomments.md) -Eigenschaft <br/> Kommentare, die in **der System** Steuerung "Software" bereitgestellt werden.<br/>                                                                                                                                                                                                                                |
| Kontakt             | [**Arpcontact**](arpcontact.md) (Eigenschaft) <br/> Kontakt **in der System** Steuerungs Option "Software" bereitgestellt.<br/>                                                                                                                                                                                                                                   |
| EstimatedSize       | Wird vom Windows Installer festgelegt und festgelegt.                                                                                                                                                                                                                                                                                                                         |
| Sprache            | [**Productlanguage**](productlanguage.md) -Eigenschaft                                                                                                                                                                                                                                                                                                                  |
| Modifypath          | Wird vom Windows Installer festgelegt und festgelegt.                                                                                                                                                                                                                                                                                                                         |
| Infodatei              | [**Arpreadme**](arpreadme.md) (Eigenschaft) <br/> Info zur bereit **Stellung der System** Steuerungs Option "Software".<br/>                                                                                                                                                                                                                                      |
| UninstallString     | Wird von Windows Installer festgelegt und festgelegt.                                                                                                                                                                                                                                                                                                                             |
| Settingsidentifier  | [**Msiarpsettingsidentifier**](msiarpsettingsidentifier.md) (Eigenschaft)                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Eigenschaften](about-properties.md)
</dt> <dt>

[Konfigurieren von "Programme hinzufügen/entfernen" mit Windows Installer](configuring-add-remove-programs-with-windows-installer.md)
</dt> <dt>

[Eigenschafts Verweis](property-reference.md)
</dt> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> </dl>

 

 




