---
description: Windows Das Installationsprogramm kann mehrere Pakete mithilfe der Transaktionsverarbeitung installieren.
ms.assetid: c4a0f4d8-818d-4e60-908b-adaa2a54de95
title: Multiple-Package Installationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d525c2904d25fb06403f85914f2b04fce2ebc57f22801a2413b2f09ad1c396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943411"
---
# <a name="multiple-package-installations"></a>Multiple-Package Installationen

Windows Das Installationsprogramm kann mehrere Pakete mithilfe der [*Transaktionsverarbeitung installieren.*](t-gly.md) Diese Funktion ist ab Windows Installer 4.5 verfügbar. Das Installationsprogramm installiert alle Pakete, die zu einer Transaktion mit mehreren Paketen oder keinem der Pakete gehören. Wenn nicht alle Pakete in der Transaktion erfolgreich installiert werden können oder der Benutzer die Installation abbricht, kann der Windows Installer ein Rollback der Änderungen ausführen und den ursprünglichen Zustand des Computers wiederherstellen.

Ein Installationspaket mit mehreren Paketen kann eine [MsiEmbeddedChainer-Tabelle](msiembeddedchainer-table.md) enthalten, die auf eine benutzerdefinierte Funktion verweist, die die [**Funktionen MsiBeginTransaction,**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona) [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)und [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) verwendet.

In [der Tabelle MsiPackageCertificate](msipackagecertificate-table.md) sind digitale Signaturzertifikate aufgeführt, mit denen die Identität der Installationspakete überprüft wird, die eine Installation mit mehreren Paketen ausführen. Sie können diese Tabelle verwenden, um zu reduzieren, wie oft ihre Installation mit mehreren Paketen eine Eingabeaufforderung zur Benutzerkontensteuerung (User [*Account Control,*](u-gly.md) UAC) anzeigt, die eine Antwort eines Administrators erfordert.

Die folgenden Windows Installer-Funktionen können Änderungen am Computer des Benutzers vornehmen, wenn der Windows Installer Anwendungen installiert, repariert, aktualisiert oder entfernt. Ab Windows Installer 4.5 kann das Installationsprogramm ein Rollback für [](t-gly.md) Änderungen ausführen, die von diesen Funktionen während der Transaktionsverarbeitung einer Installation mit mehreren Paketen vorgenommen wurden:

<dl>

[**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)  
[**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)  
[**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)  
[**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)  
[**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)  
[**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)  
[**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)  
[**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)  
[**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)  
[**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)  
[**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)  
[**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)  
[**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)  
[**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)  
[**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)  
[**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)  
[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)  
</dl>

Es gibt eine Ausnahme, wenn der Windows Installer auf ein Paket stößt, das zu einer Installation mit mehreren Paketen gehört, die eine [ForceReboot-](forcereboot-action.md) oder [ScheduleReboot-Aktion](schedulereboot-action.md) enthält. In diesem Fall installiert Windows Installer nicht nur dieses Paket. Andere Pakete, die zur Installation mehrerer Pakete gehören und keine ForceReboot- oder ScheduleReboot-Aktion enthalten, können installiert werden.

**[Windows Installer 4.0 und](not-supported-in-windows-installer-4-0.md)früher: **[*Die*](t-gly.md) Transaktionsverarbeitung mehrerer Pakete Windows Installer-Installationen wird nicht unterstützt. Diese Versionen des Windows Installers können kein Rollback für die Installation mehrerer Pakete als einzelne Transaktion ausführen.

**Windows Server 2008 R2 mit [aktivierter Remotedesktopdienste-Rolle:](../termserv/terminal-services-portal.md)** Nicht unterstützt. Eine Installation mehrerer Pakete mithilfe der [MsiEmbeddedChainer-Tabelle](msiembeddedchainer-table.md) schlägt fehl, wenn [die](../termserv/terminal-services-portal.md) Remotedesktopdienste aktiviert ist.

 

 
