---
description: Windows Installer können mithilfe digitaler Signaturen beschädigte Ressourcen erkennen.
ms.assetid: 49f1c1f9-d342-47e0-8888-2eadc5dbd000
title: Digitale Signaturen und externe CAB-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f10e921b324a43a919a417f47953c0a44e4777ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866339"
---
# <a name="digital-signatures-and-external-cabinet-files"></a>Digitale Signaturen und externe CAB-Dateien

Windows Installer können mithilfe digitaler Signaturen beschädigte Ressourcen erkennen. Wenn eine externe Ressource installiert wird, kann das Signatur Geber Zertifikat, das zur Ressource gehört, anhand eines im Paket erstellten Referenz Signatur Geber Zertifikats überprüft werden. Der Installer kann keine Signaturen für interne Schränke überprüfen. Es können nur digitale Signaturen überprüft werden, indem die [msidigitalsignature-Tabelle](msidigitalsignature-table.md) und die [msidigitalcertificate-Tabelle](msidigitalcertificate-table.md)verwendet werden.

Windows Installer führt Folgendes aus, wenn eine in einer externen CAB-Datei gespeicherte Datei installiert wird:

-   Der Installer überprüft, ob der Medien Eintrag für diese externe CAB-Datei in der [Tabelle msidigitalsignature](msidigitalsignature-table.md)aufgeführt ist. Eine Datei, die in einer externen CAB-Datei gespeichert ist, wird durch einen Eintrag in der CAB-Spalte der [Medien Tabelle](media-table.md) identifiziert, der kein-Zeichen vorangestellt ist \# .
-   Bevor die externe CAB-Datei geöffnet wird, ruft der Installer WinVerifyTrust auf, um das aktuelle Zertifikat und die aktuellen Hash Informationen zu extrahieren. Wenn die aktuellen Signatur Informationen im CAB und die im Paket erstellten Signatur Informationen nicht übereinstimmen, tritt bei der Installation ein Fehler auf. Die Installation schlägt fehl, da die CAB-Version möglicherweise kompromittiert wurde und nicht vertrauenswürdig ist.

Weitere Informationen zur Verwendung digitaler Signaturen, digitaler Zertifikate und [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)finden Sie im Abschnitt " [Sicherheit](https://msdn.microsoft.com/library/cc527452.aspx) " des Microsoft Windows Software Development Kit (SDK).

Weitere Informationen finden Sie unter [**msigetfilesignatureinformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [msidigitalcertificate Table](msidigitalcertificate-table.md)und [msidigitalsignature Table](msidigitalsignature-table.md).

 

 
