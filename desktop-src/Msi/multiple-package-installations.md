---
description: Windows Installer können mehrere Pakete mithilfe der Transaktionsverarbeitung installieren.
ms.assetid: c4a0f4d8-818d-4e60-908b-adaa2a54de95
title: Multiple-Package Installationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65fa30893f353d6661a7f77fe23fe55b4c9b22c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347923"
---
# <a name="multiple-package-installations"></a>Multiple-Package Installationen

Windows Installer können mehrere Pakete mithilfe der [*Transaktionsverarbeitung*](t-gly.md)installieren. Diese Funktion ist ab Windows Installer 4,5 verfügbar. Das Installationsprogramm installiert alle Pakete, die zu einer Transaktion mit mehreren Paketen gehören, oder keines der Pakete. Wenn alle Pakete in der Transaktion nicht erfolgreich installiert werden können oder wenn der Benutzer die Installation abbricht, kann die Windows Installer Änderungen zurücksetzen und den ursprünglichen Zustand des Computers wiederherstellen.

Ein Installationspaket mit mehreren Paketen kann eine [msiembeddedchainer-Tabelle](msiembeddedchainer-table.md) enthalten, die auf eine benutzerdefinierte Funktion verweist, die die [**msibegintransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona)-, [**msijointransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)-und [**msiendtransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) -Funktionen verwendet.

In der [Tabelle msipackagecertificate](msipackagecertificate-table.md) sind digitale Signatur Zertifikate aufgeführt, mit denen die Identität der Installationspakete überprüft wird, die eine Installation mit mehreren Paketen vornehmen. Sie können diese Tabelle verwenden, um zu reduzieren, wie oft bei der Installation mehrerer Pakete eine [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC) angezeigt wird, die von einem Administrator eine Antwort erfordert.

Die folgenden Windows Installer Funktionen können Änderungen am Computer des Benutzers vornehmen, wenn der Windows Installer Anwendungen installiert, repariert, aktualisiert oder entfernt. Ab Windows Installer 4,5 kann das Installationsprogramm Änderungen zurücksetzen, die von diesen Funktionen während der [*Transaktionsverarbeitung*](t-gly.md) einer Installation mit mehreren Paketen vorgenommen werden:

<dl>

[**Msiankündigen-Produkt**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)  
[**Msiankündigen-productex**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)  
[**Msiapplymultiplepatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)  
[**Msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)  
[**Msikonfigurierfeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)  
[**Msikonfigurireproduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)  
[**Msikonfigurireproduktions-ctex**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)  
[**Msiinstallmissingcomponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)  
[**Msiinstallmissingfile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)  
[**Msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)  
[**Msiproviabassembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)  
[**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)  
[**Msiprovidequalifiedcomponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)  
[**Msiprovide qualifiedcomponumtex**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)  
[**Msireinstallfeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)  
[**Msireinstallproduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)  
[**Msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)  
</dl>

Es gibt eine Ausnahme, wenn die Windows Installer ein Paket findet, das zu einer Installation mit mehreren Paketen gehört, die eine [ForceReboot](forcereboot-action.md) -oder [schedulereboot](schedulereboot-action.md) -Aktion enthält. In diesem Fall installiert Windows Installer nicht nur dieses Paket. Andere Pakete, die zur Installation mit mehreren Paketen gehören und keine ForceReboot-oder schedulereboot-Aktion enthalten, können installiert werden.

**[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md): * * die [*Transaktionsverarbeitung*](t-gly.md) von Windows Installer Installationen mit mehreren Paketen wird nicht unterstützt. Diese Versionen der Windows Installer können die Installation mehrerer Pakete nicht als einzelne Transaktion zurücksetzen.

**Windows Server 2008 R2 mit aktivierter [Remotedesktopdienste](../termserv/terminal-services-portal.md) Rolle:** Nicht unterstützt. Eine mehrfach Paketinstallation mithilfe der [msiembeddedchainer-Tabelle](msiembeddedchainer-table.md) schlägt fehl, wenn die [Remotedesktopdienste](../termserv/terminal-services-portal.md) Rolle aktiviert ist.

 

 
