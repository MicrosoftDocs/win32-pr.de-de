---
description: Eine konfigurierbare ausführbare Bootstrapdatei (Setup.exe) und ein Konfigurationstool (Msistuff.exe) sind in den Windows SDK-Komponenten für Windows Installer-Entwickler enthalten.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Konfigurieren der Setup.exe-Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c181453f689b7f2c273ba8726097e5d1cd134d1b9675c8ffc42de42d902b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638729"
---
# <a name="configuring-the-setupexe-resources"></a>Konfigurieren der Setup.exe-Ressourcen

Eine konfigurierbare ausführbare Bootstrapdatei (Setup.exe) und ein Konfigurationstool ( [Msistuff.exe](msistuff-exe.md)) sind in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)enthalten. Mithilfe von Msistuff.exe zum Konfigurieren der Ressourcen in Setup.exe können Entwickler problemlos eine Webinstallation eines Windows Installer-Pakets erstellen. Weitere Informationen finden Sie unter [Internet Download Bootstrapping](internet-download-bootstrapping.md).

Wenn Sie die folgende Befehlszeile eingeben, werden die Ressourcen für das beispiel konfiguriert, das unter Beispiel für eine [URL-basierte Windows Installation des Installationsprogramms](a-url-based-windows-installer-installation-example.md)beschrieben wird.

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[Fortsetzen](sign-setup-exe-and-mysetup-msi.md)

 

 



