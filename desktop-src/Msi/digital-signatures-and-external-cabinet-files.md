---
description: Windows Das Installationsprogramm kann digitale Signaturen verwenden, um beschädigte Ressourcen zu erkennen.
ms.assetid: 49f1c1f9-d342-47e0-8888-2eadc5dbd000
title: Digitale Signaturen und externe Schränkdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40edd8527eb93a6b970b3a8ce18fec8cc81f4688804a4e18f7ec5cdd748f3eca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947464"
---
# <a name="digital-signatures-and-external-cabinet-files"></a>Digitale Signaturen und externe Schränkdateien

Windows Das Installationsprogramm kann digitale Signaturen verwenden, um beschädigte Ressourcen zu erkennen. Wenn Sie eine externe Ressource installieren, kann das zur Ressource gehörende Signierungszertifikat anhand eines im Paket erstellten Verweis-Signierungszertifikats überprüft werden. Das Installationsprogramm kann keine Signaturen für interne Schränke überprüfen. Digitale Signaturen können nur mithilfe der [Tabellen MsiDigitalSignature](msidigitalsignature-table.md) und [MsiDigitalCertificate überprüft werden.](msidigitalcertificate-table.md)

Windows Das Installationsprogramm führt folgende Schritte aus, wenn eine Datei installiert wird, die in einer externen Schränkung gespeichert ist:

-   Das Installationsprogramm überprüft, ob der Medieneintrag für diese externe Schränkung in der [Tabelle MsiDigitalSignature aufgeführt ist.](msidigitalsignature-table.md) Eine datei, die in einer externen Schränkung gespeichert ist, wird durch einen Eintrag in der Spalte "Cabinet" der [Media-Tabelle](media-table.md) identifiziert, dem kein Zeichen vom Präfix \# "" vorangestellt ist.
-   Vor dem Öffnen der externen Schränkung ruft das Installationsprogramm WinVerifyTrust auf, um das aktuelle Zertifikat und die Hashinformationen zu extrahieren. Wenn es einen Konflikt zwischen den aktuellen Signaturinformationen im Schränk und den im Paket erstellten Signaturinformationen gibt, schlägt die Installation fehl. Die Installation schlägt fehl, da die Schränkung möglicherweise kompromittiert wurde und nicht als vertrauenswürdig eingestuft werden kann.

Weitere Informationen zur Verwendung von digitalen Signaturen, digitalen Zertifikaten und [](https://msdn.microsoft.com/library/cc527452.aspx) [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)finden Sie im Abschnitt Sicherheit des Microsoft Windows Software Development Kit (SDK).

Weitere Informationen finden Sie unter [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [MsiDigitalCertificate table](msidigitalcertificate-table.md)und [MsiDigitalSignature table](msidigitalsignature-table.md).

 

 
