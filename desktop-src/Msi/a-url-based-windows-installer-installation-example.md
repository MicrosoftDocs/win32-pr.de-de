---
description: Dieses Beispiel veranschaulicht das Erstellen einer URL-basierten Installation eines Windows Installer-Pakets.
ms.assetid: a38a1132-43b4-449d-b134-f351ce370223
title: URL-basiertes Windows Installer-Installationsbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c25fb4f84ff3507505be7f16675b8da39afd349cb1b4c78520ee3de004df749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013328"
---
# <a name="a-url-based-windows-installer-installation-example"></a>URL-basiertes Windows Installer-Installationsbeispiel

Dieses Beispiel veranschaulicht das Erstellen einer URL-basierten Installation eines Windows Installer-Pakets. Weitere Informationen zum Sichern von Installationen und zum Verwenden digitaler Zertifikate finden Sie unter Richtlinien für die Erstellung sicherer [Installationen](guidelines-for-authoring-secure-installations.md) und digitaler Signaturen [und Windows Installer](digital-signatures-and-windows-installer.md).

Um dieses Beispiel zu reproduzieren, benötigen Sie [das Hilfsprogramm SignTool.](../seccrypto/signtool.md) Weitere Informationen finden Sie in der [CryptoAPI-Tools-Referenz](../seccrypto/cryptoapi-tools-reference.md) im Microsoft Windows Software Development Kit (SDK). Außerdem benötigen Sie [Msistuff.exe](msistuff-exe.md) und Setup.exe-Hilfsprogramme aus den [Windows SDK-Komponenten für Windows Installer-Entwickler.](platform-sdk-components-for-windows-installer-developers.md) Weitere Informationen finden Sie unter [Internet Download Bootstrapping](internet-download-bootstrapping.md).

Das Beispiel hat die folgenden Spezifikationen:

-   Wenn Benutzer Ihre Website besuchen und auf den Link "MySetup-Installation" klicken, wird ihnen die Option zum Speichern oder Ausführen an diesem Speicherort zur Verfügung stehen. Wenn der Benutzer die Ausführung von diesem Speicherort auswählt, aktualisiert der Setup.exe die Version des Windows-Installers auf dem Computer, sofern erforderlich, überprüft die digitale Signatur im Installationspaket und installiert das Paket auf dem Computer.
-   Das digitale Zertifikat Mycert.cer wird mit dem privaten Schlüssel Mycert.pvk bereitgestellt.
-   Die URL der hypothetischen Website, die ein Kunde zum Installieren des Pakets besuchen würde, ist https: \/ /www.blueyonderairlines.com/Products/MySetup/mysetup.html.
-   Das Webserverlayout lautet wie folgt. 

    | URL                                                               | Datei        | BESCHREIBUNG                                    |
    |-------------------------------------------------------------------|-------------|------------------------------------------------|
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Setup.exe   | Setup.exe Bootstrapper.                        |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | MySetup.msi | Installationspaket                           |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Cab1.cab    | Quelldatei-Schränk \# 1                        |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Cab2.cab    | Quelldatei-Schaltschränk \# 2                        |
    | https: \/ /www.blueyonderairlines.com/Products/Common/InstMsi/Ansi    | Instmsi.exe | ANSI Windows Installer 2.0 redistributable.    |
    | https: \/ /www.blueyonderairlines.com/Products/Common/InstMsi/Unicode | Instmsi.exe | Unicode Windows Installer 2.0 redistributable. |

    

     

[Fortsetzen](configuring-the-setup-exe-resources.md)

 

 
