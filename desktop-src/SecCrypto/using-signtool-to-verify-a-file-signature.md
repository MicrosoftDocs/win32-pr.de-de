---
description: Erläutert die Verwendung von SignTool zum Überprüfen einer Dateisignatur.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Verwenden von SignTool zum Überprüfen einer Dateisignatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e91df7a64a8db48d04ceba9df5fbc3fd358058
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "107954923"
---
# <a name="using-signtool-to-verify-a-file-signature"></a><span data-ttu-id="4f3fc-103">Verwenden von SignTool zum Überprüfen einer Dateisignatur</span><span class="sxs-lookup"><span data-stu-id="4f3fc-103">Using SignTool to Verify a File Signature</span></span>

<span data-ttu-id="4f3fc-104">Der folgende Befehl überprüft die Signatur einer Datei mit dem Namen *MyControl.exe*:</span><span class="sxs-lookup"><span data-stu-id="4f3fc-104">The following command verifies the signature of a file named *MyControl.exe*:</span></span>

<span data-ttu-id="4f3fc-105">**SignTool verify** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="4f3fc-105">**SignTool verify** *MyControl.exe*</span></span>

<span data-ttu-id="4f3fc-106">Wenn im vorherigen Beispiel ein Fehler auftritt, könnte es sein, dass die Signatur ein Codesignaturzertifikat verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="4f3fc-106">If the preceding example fails, it could be that the signature used a code-signing certificate.</span></span> <span data-ttu-id="4f3fc-107">[SignTool](signtool.md) verwendet zur Überprüfung standardmäßig die Windows-Treiberrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="4f3fc-107">[SignTool](signtool.md) defaults to the Windows driver policy for verification.</span></span>

<span data-ttu-id="4f3fc-108">Der folgende Befehl überprüft die Signatur mithilfe der Standardauthentifizierungsüberprüfungsrichtlinie:</span><span class="sxs-lookup"><span data-stu-id="4f3fc-108">The following command verifies the signature, using the Default Authentication Verification Policy:</span></span>

<span data-ttu-id="4f3fc-109">**SignTool verify /pa** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="4f3fc-109">**SignTool verify /pa** *MyControl.exe*</span></span>

<span data-ttu-id="4f3fc-110">Der folgende Befehl überprüft eine Systemdatei, die möglicherweise in einem Katalog signiert ist:</span><span class="sxs-lookup"><span data-stu-id="4f3fc-110">The following command verifies a system file that may be signed in a catalog:</span></span>

<span data-ttu-id="4f3fc-111">**SignTool verify /a** *SysFile.dll*</span><span class="sxs-lookup"><span data-stu-id="4f3fc-111">**SignTool verify /a** *SysFile.dll*</span></span>

<span data-ttu-id="4f3fc-112">Der folgende Befehl überprüft eine Systemdatei, die in einem Katalog mit dem Namen *MyCat.cat* signiert ist:</span><span class="sxs-lookup"><span data-stu-id="4f3fc-112">The following command verifies a system file that is signed in a catalog named *MyCat.cat*:</span></span>

<span data-ttu-id="4f3fc-113">**SignTool verify /c** *MyCat.cat* *MyFile.ini*</span><span class="sxs-lookup"><span data-stu-id="4f3fc-113">**SignTool verify /c** *MyCat.cat* *MyFile.ini*</span></span>

<span data-ttu-id="4f3fc-114">Für jede [SignTool-Überprüfung](signtool.md) können Sie den Signierer des Zertifikats abrufen.</span><span class="sxs-lookup"><span data-stu-id="4f3fc-114">For any [SignTool](signtool.md) verification, you can retrieve the signer of the certificate.</span></span> <span data-ttu-id="4f3fc-115">Der folgende Befehl überprüft eine Systemdatei und zeigt das Signaturgeberzertifikat an:</span><span class="sxs-lookup"><span data-stu-id="4f3fc-115">The following command verifies a system file and displays the signer certificate:</span></span>

<span data-ttu-id="4f3fc-116">**SignTool verify /v** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="4f3fc-116">**SignTool verify /v** *MyControl.exe*</span></span>

<span data-ttu-id="4f3fc-117">[SignTool](signtool.md) gibt Befehlszeilentext zurück, der das Ergebnis der Signaturüberprüfung angibt.</span><span class="sxs-lookup"><span data-stu-id="4f3fc-117">[SignTool](signtool.md) returns command-line text that states the result of the signature check.</span></span> <span data-ttu-id="4f3fc-118">Darüber hinaus gibt SignTool für eine erfolgreiche Ausführung den Exitcode 0 (null) zurück, einen für eine fehlgeschlagene Ausführung und zwei für die Ausführung, die mit Warnungen abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="4f3fc-118">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="4f3fc-119">Weitere Informationen zu [SignTool](signtool.md)finden Sie unter [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="4f3fc-119">For more information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 



