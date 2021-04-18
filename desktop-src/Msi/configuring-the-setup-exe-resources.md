---
description: In den Windows SDK Komponenten für Windows Installer Entwickler ist eine konfigurierbare Bootstrap-Datei (Setup.exe) und ein Konfigurationstool (Msistuff.exe) enthalten.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Konfigurieren der Setup.exe Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b7907310ff6efcf41e984bf132bbbaedf38b6a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106371875"
---
# <a name="configuring-the-setupexe-resources"></a>Konfigurieren der Setup.exe Ressourcen

In den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)ist eine konfigurierbare Bootstrap-Datei (Setup.exe) und ein Konfigurationstool ( [Msistuff.exe](msistuff-exe.md)) enthalten. Wenn Sie Msistuff.exe verwenden, um die Ressourcen in Setup.exe zu konfigurieren, können Entwickler problemlos eine Webinstallation eines Windows Installer Pakets erstellen. Weitere Informationen finden [Sie unter Internet Download Bootstrapping](internet-download-bootstrapping.md).

Wenn Sie die folgende Befehlszeile eingeben, werden die Ressourcen für das Beispiel konfiguriert, das in [einem URL-basierten Windows Installer Installations Beispiel](a-url-based-windows-installer-installation-example.md)beschrieben wird.

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[Fortsetzen](sign-setup-exe-and-mysetup-msi.md)

 

 



