---
description: Verwenden Sie diese Richtlinien, um eine gesamte Installation Windows Installers durch eine digitale Signatur abzudecken.
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: Erstellen einer vollständig überprüften signierten Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d105b06e3f063d8cbeb1fac579beb12258b20062bf5cbae2cc6d08e9be6e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066180"
---
# <a name="authoring-a-fully-verified-signed-installation"></a>Erstellen einer vollständig überprüften signierten Installation

Sie können diese Richtlinien verwenden, um eine gesamte installation Windows Installer durch eine digitale Signatur abzudecken.

Autoren Windows Installationsprogramme müssen Folgendes einhalten, um sicherzustellen, dass alle Teile der Installation durch eine digitale Signatur abgedeckt werden:

-   Verwenden Sie interne Cab-Dateien, oder verwenden Sie signierte externe Cab-Dateien, und erstellen Sie die [Tabelle MsiDigitalSignature](msidigitalsignature-table.md) und die [Tabelle MsiDigitalCertificate](msidigitalcertificate-table.md)ordnungsgemäß.
-   Verwenden Sie nur benutzerdefinierte Aktionen, die im Paket gespeichert oder mit dem Paket installiert sind.
-   Signieren Sie das Installationspaket.
-   Schließen Sie eine [MsiPatchCertificate-Tabelle](msipatchcertificate-table.md) in das Paket ein. Um [das Patchen der Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md)zu aktivieren, muss diese Tabelle Informationen enthalten, mit denen die Signaturgeberzertifikate identifiziert werden, die zum digitalen Signieren von Patches verwendet werden. UAC-Patches ermöglichen es dem Autor des Installationspakets, digital signierte Patches zu identifizieren, die in Zukunft von Benutzern ohne Administratorrechte angewendet werden können.

Ein Beispiel für das Erstellen einer signierten Installation mithilfe von Automatisierung finden Sie unter [Erstellen einer vollständig überprüften signierten Installation mithilfe von Automation.](authoring-a-fully-verified-signed-installation-using-automation.md)

 

 



