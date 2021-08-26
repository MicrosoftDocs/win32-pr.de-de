---
description: Eine Liste der Eigenschaften Windows Installer mit Werten, die unter dem Registrierungsschlüssel Deinstallieren geschrieben werden.
ms.assetid: f831cc62-4b19-4285-8bb1-6080567ac985
title: Windows Installer-Eigenschaften für den Registrierungsschlüssel deinstallieren
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: b898cd2a83a05783141ddf1fb4a7cbebb783bbcd7640526c5b653afa434d2175
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810319"
---
# <a name="windows-installer-properties-for-the-uninstall-registry-key"></a>Windows Installer-Eigenschaften für den Registrierungsschlüssel deinstallieren

Die folgenden Installereigenschaften enthalten die Werte, die unter dem Registrierungsschlüssel geschrieben werden:

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall**

Die Werte werden in einem Unterschlüssel gespeichert, der durch die Produktcode-GUID der Anwendung identifiziert wird.



| Wert               | Windows Installer-Eigenschaft                                                                                                                                                                                                                                                                                                                                           |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName         | [**ProductName-Eigenschaft**](productname.md)                                                                                                                                                                                                                                                                                                                          |
| DisplayVersion      | Abgeleitet von [**der ProductVersion-Eigenschaft**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Herausgeber           | [**Manufacturer-Eigenschaft**](manufacturer.md)                                                                                                                                                                                                                                                                                                                        |
| VersionMinor        | Abgeleitet von [**der ProductVersion-Eigenschaft**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| VersionMajor        | Abgeleitet von [**der ProductVersion-Eigenschaft**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Version             | Abgeleitet von [**der ProductVersion-Eigenschaft**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| HelpLink            | [**ARPHELPLINK-Eigenschaft**](arphelplink.md)                                                                                                                                                                                                                                                                                                                          |
| HelpTelephone       | [**ARPHELPTELEPHONE (Eigenschaft)**](arphelptelephone.md)                                                                                                                                                                                                                                                                                                                |
| InstallDate         | Der Zeitpunkt, zu dem dieses Produkt den Dienst zuletzt empfangen hat. Der Wert dieser Eigenschaft wird jedes Mal ersetzt, wenn ein Patch [](command-line-options.md) angewendet oder aus dem Produkt entfernt wird oder die /v-Befehlszeilenoption verwendet wird, um das Produkt zu reparieren. Wenn das Produkt keine Reparaturen oder Patches erhalten hat, enthält diese Eigenschaft den Zeitpunkt, zu dem dieses Produkt auf diesem Computer installiert wurde. |
| InstallLocation     | [**ARPINSTALLLOCATION (Eigenschaft)**](arpinstalllocation.md)                                                                                                                                                                                                                                                                                                            |
| InstallSource       | [**SourceDir-Eigenschaft**](sourcedir.md)                                                                                                                                                                                                                                                                                                                              |
| URLInfoAbout        | [**ARPURLINFOABOUT-Eigenschaft**](arpurlinfoabout.md)                                                                                                                                                                                                                                                                                                                  |
| URLUpdateInfo       | [**ARPURLUPDATEINFO-Eigenschaft**](arpurlupdateinfo.md)                                                                                                                                                                                                                                                                                                                |
| AuthorizedCDFPrefix | [**ARPAUTHORIZEDCDFPREFIX(Eigenschaft)**](arpauthorizedcdfprefix.md)                                                                                                                                                                                                                                                                                                    |
| Kommentare            | [**ARPCOMMENTS-Eigenschaft**](arpcomments.md) <br/> Kommentare, die in der **Systemsteuerung Programme hinzufügen oder** entfernen bereitgestellt werden.<br/>                                                                                                                                                                                                                                |
| Contact             | [**ARPCONTACT-Eigenschaft**](arpcontact.md) <br/> Kontakt, der in der **Systemsteuerung Programme hinzufügen oder** entfernen angegeben wird.<br/>                                                                                                                                                                                                                                   |
| EstimatedSize       | Wird vom Installationsprogramm für Windows festgelegt.                                                                                                                                                                                                                                                                                                                         |
| Sprache            | [**ProductLanguage (Eigenschaft)**](productlanguage.md)                                                                                                                                                                                                                                                                                                                  |
| ModifyPath          | Wird vom Installationsprogramm für Windows festgelegt.                                                                                                                                                                                                                                                                                                                         |
| Infodatei              | [**ARPREADME-Eigenschaft**](arpreadme.md) <br/> In der Systemsteuerung Programme hinzufügen oder entfernen **bereitgestellte** Readme.<br/>                                                                                                                                                                                                                                      |
| UninstallString     | Wird vom Installationsprogramm bestimmt Windows festgelegt.                                                                                                                                                                                                                                                                                                                             |
| SettingsIdentifier  | [**MSIARPSETTINGSIDENTIFIER(Eigenschaft)**](msiarpsettingsidentifier.md)                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Eigenschaften](about-properties.md)
</dt> <dt>

[Konfigurieren des Hinzufügens/Entfernens von Programmen mit Windows Installer](configuring-add-remove-programs-with-windows-installer.md)
</dt> <dt>

[Eigenschaftenverweis](property-reference.md)
</dt> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> </dl>

 

 




