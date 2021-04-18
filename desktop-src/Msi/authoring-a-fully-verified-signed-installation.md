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
# <a name="authoring-a-fully-verified-signed-installation"></a><span data-ttu-id="d7aa6-103">Erstellen einer vollständig überprüften signierten Installation</span><span class="sxs-lookup"><span data-stu-id="d7aa6-103">Authoring a Fully Verified Signed Installation</span></span>

<span data-ttu-id="d7aa6-104">Sie können diese Richtlinien verwenden, um eine vollständige Windows Installer Installation durch eine digitale Signatur abzudecken.</span><span class="sxs-lookup"><span data-stu-id="d7aa6-104">You can use these guidelines to cover an entire Windows Installer installation by a digital signature.</span></span>

<span data-ttu-id="d7aa6-105">Autoren von Windows Installer Installationen müssen Folgendes einhalten, um sicherzustellen, dass alle Teile der Installation durch eine digitale Signatur abgedeckt werden:</span><span class="sxs-lookup"><span data-stu-id="d7aa6-105">Authors of Windows Installer installations must adhere to the following to ensure that all parts of the installation are covered by a digital signature:</span></span>

-   <span data-ttu-id="d7aa6-106">Verwenden Sie interne CAB-Dateien oder signierte externe CAB-Dateien, und erstellen Sie die [msidigitalsignature-Tabelle](msidigitalsignature-table.md) und die [msidigitalcertificate-Tabelle](msidigitalcertificate-table.md)ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="d7aa6-106">Use internal cabinet files, or use signed external cabinet files and correctly author the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span>
-   <span data-ttu-id="d7aa6-107">Verwenden Sie nur benutzerdefinierte Aktionen, die im Paket gespeichert sind oder mit dem Paket installiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7aa6-107">Use only custom actions stored within the package or installed with the package.</span></span>
-   <span data-ttu-id="d7aa6-108">Signieren Sie das Installationspaket.</span><span class="sxs-lookup"><span data-stu-id="d7aa6-108">Sign the installation package.</span></span>
-   <span data-ttu-id="d7aa6-109">Fügen Sie eine [MsiPatchCertificate-Tabelle](msipatchcertificate-table.md) in das Paket ein.</span><span class="sxs-lookup"><span data-stu-id="d7aa6-109">Include an [MsiPatchCertificate table](msipatchcertificate-table.md) in the package.</span></span> <span data-ttu-id="d7aa6-110">Um das [Patchen der Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md)zu aktivieren, muss diese Tabelle Informationen enthalten, die zum Identifizieren der Signatur Geber Zertifikate verwendet werden, mit denen Patches digital signiert</span><span class="sxs-lookup"><span data-stu-id="d7aa6-110">To enable [User Account Control (UAC) Patching](user-account-control--uac--patching.md), this table must contain information used to identify the signer certificates used to digitally sign patches.</span></span> <span data-ttu-id="d7aa6-111">Das UAC-Patchen ermöglicht es dem Autor des Installationspakets, Digital signierte Patches zu identifizieren, die in Zukunft von Benutzern ohne Administratorrechte angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d7aa6-111">UAC patching enables the author of the installation package to identify digitally-signed patches that can be applied in the future by non-administrator users.</span></span>

<span data-ttu-id="d7aa6-112">Ein Beispiel, das zeigt, wie eine signierte Installation mithilfe von Automation erstellt wird, finden [Sie unter Erstellen einer vollständig verifizierten signierten Installation mithilfe von Automation](authoring-a-fully-verified-signed-installation-using-automation.md)</span><span class="sxs-lookup"><span data-stu-id="d7aa6-112">For an example showing how to author a signed installation using automation, see [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span></span>

 

 



