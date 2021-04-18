---
description: Verwenden Sie diese Richtlinien, um eine vollständige Windows Installer Installation durch eine digitale Signatur abzudecken.
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: Erstellen einer vollständig überprüften signierten Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e76bbfb77eab8b020cb1591847d2a36d09c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347545"
---
# <a name="authoring-a-fully-verified-signed-installation"></a>Erstellen einer vollständig überprüften signierten Installation

Sie können diese Richtlinien verwenden, um eine vollständige Windows Installer Installation durch eine digitale Signatur abzudecken.

Autoren von Windows Installer Installationen müssen Folgendes einhalten, um sicherzustellen, dass alle Teile der Installation durch eine digitale Signatur abgedeckt werden:

-   Verwenden Sie interne CAB-Dateien oder signierte externe CAB-Dateien, und erstellen Sie die [msidigitalsignature-Tabelle](msidigitalsignature-table.md) und die [msidigitalcertificate-Tabelle](msidigitalcertificate-table.md)ordnungsgemäß.
-   Verwenden Sie nur benutzerdefinierte Aktionen, die im Paket gespeichert sind oder mit dem Paket installiert werden.
-   Signieren Sie das Installationspaket.
-   Fügen Sie eine [MsiPatchCertificate-Tabelle](msipatchcertificate-table.md) in das Paket ein. Um das [Patchen der Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md)zu aktivieren, muss diese Tabelle Informationen enthalten, die zum Identifizieren der Signatur Geber Zertifikate verwendet werden, mit denen Patches digital signiert Das UAC-Patchen ermöglicht es dem Autor des Installationspakets, Digital signierte Patches zu identifizieren, die in Zukunft von Benutzern ohne Administratorrechte angewendet werden können.

Ein Beispiel, das zeigt, wie eine signierte Installation mithilfe von Automation erstellt wird, finden [Sie unter Erstellen einer vollständig verifizierten signierten Installation mithilfe von Automation](authoring-a-fully-verified-signed-installation-using-automation.md)

 

 



