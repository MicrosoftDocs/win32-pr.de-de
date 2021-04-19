---
description: In diesem Beispiel wird veranschaulicht, wie eine URL-basierte Installation eines Windows Installer Pakets erstellt wird.
ms.assetid: a38a1132-43b4-449d-b134-f351ce370223
title: URL-basiertes Windows Installer-Installationsbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a210eb1b93202930309223b49c737aa85b1812
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106355154"
---
# <a name="a-url-based-windows-installer-installation-example"></a>URL-basiertes Windows Installer-Installationsbeispiel

In diesem Beispiel wird veranschaulicht, wie eine URL-basierte Installation eines Windows Installer Pakets erstellt wird. Weitere Informationen zum Sichern von Installationen und zum Verwenden digitaler Zertifikate finden Sie unter [Richtlinien für die Erstellung sicherer Installationen](guidelines-for-authoring-secure-installations.md) und [digitaler Signaturen und Windows Installer](digital-signatures-and-windows-installer.md).

Um dieses Beispiel zu reproduzieren, benötigen Sie das [SignTool](../seccrypto/signtool.md) -Hilfsprogramm. Weitere Informationen finden Sie in der [Referenz zur CryptoAPI-Tools](../seccrypto/cryptoapi-tools-reference.md) im Microsoft Windows Software Development Kit (SDK). Außerdem benötigen Sie [Msistuff.exe](msistuff-exe.md) und Setup.exe Hilfsprogramme aus den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md). Weitere Informationen finden Sie unter [Internet Download Bootstrapping](internet-download-bootstrapping.md).

Das Beispiel enthält die folgenden Spezifikationen:

-   Wenn Benutzer Ihre Website besuchen und auf den Link "mySetup-Installation" klicken, wird Ihnen die Option zum Speichern oder ausführen an diesem Speicherort angezeigt. Wenn der Benutzer die Ausführung von diesem Speicherort aus auswählt, wird die-Version Windows Installer des-Setup.exe bei Bedarf auf dem Computer aktualisiert, die digitale Signatur des Installationspakets überprüft und das Paket auf dem Computer installiert.
-   Es gibt ein digitales Zertifikat, mycert. CER, das mit dem privaten Schlüssel mycert. pvk bereitgestellt wird.
-   Die URL der hypothetischen Website, die ein Kunde zum Installieren des Pakets besuchen würde, ist https: \/ /www.blueyonderairlines.com/Products/mySetup/mysetup.html.
-   Das Webserver Layout lautet wie folgt. 

    | URL                                                               | Datei        | BESCHREIBUNG                                    |
    |-------------------------------------------------------------------|-------------|------------------------------------------------|
    | https: \/ /www.blueyonderairlines.com/Products/mySetup/               | Setup.exe   | Setup.exe Bootstrapper.                        |
    | https: \/ /www.blueyonderairlines.com/Products/mySetup/               | MySetup.msi | Installationspaket                           |
    | https: \/ /www.blueyonderairlines.com/Products/mySetup/               | Cab1.cab    | Quelldatei CAB \# 1                        |
    | https: \/ /www.blueyonderairlines.com/Products/mySetup/               | Cab2.cab    | Quelldatei CAB \# 2                        |
    | https: \/ /www.blueyonderairlines.com/Products/Common/Instmsi/ANSI    | Instmsi.exe | ANSI Windows Installer 2,0 Redistributable.    |
    | https: \/ /www.blueyonderairlines.com/Products/Common/Instmsi/Unicode | Instmsi.exe | Unicode-Windows Installer 2,0 Redistributable. |

    

     

[Fortsetzen](configuring-the-setup-exe-resources.md)

 

 
