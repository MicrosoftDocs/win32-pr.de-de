---
description: Erläutert, wie SignTool verwendet wird, um eine Datei Signatur zu überprüfen.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Verwenden von SignTool zum Überprüfen einer Datei Signatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8161d4c890400f3aa33b415e7ac16a5306aa094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348470"
---
# <a name="using-signtool-to-verify-a-file-signature"></a><span data-ttu-id="8fe31-103">Verwenden von SignTool zum Überprüfen einer Datei Signatur</span><span class="sxs-lookup"><span data-stu-id="8fe31-103">Using SignTool to Verify a File Signature</span></span>

<span data-ttu-id="8fe31-104">Mit dem folgenden Befehl wird die Signatur einer Datei mit dem Namen *MyControl.exe* überprüft:</span><span class="sxs-lookup"><span data-stu-id="8fe31-104">The following command verifies the signature of a file named *MyControl.exe*:</span></span>

<span data-ttu-id="8fe31-105">**SignTool-Überprüfung** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="8fe31-105">**SignTool verify** *MyControl.exe*</span></span>

<span data-ttu-id="8fe31-106">Wenn das vorherige Beispiel fehlschlägt, kann die Signatur ein Code Signaturzertifikat verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fe31-106">If the preceding example fails, it could be that the signature used a code-signing certificate.</span></span> <span data-ttu-id="8fe31-107">[SignTool](signtool.md) verwendet standardmäßig die Windows-Treiber Richtlinie für die Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="8fe31-107">[SignTool](signtool.md) defaults to the Windows driver policy for verification.</span></span>

<span data-ttu-id="8fe31-108">Mit dem folgenden Befehl wird die Signatur mit der Standard Richtlinie für die Authentifizierungs Überprüfung überprüft:</span><span class="sxs-lookup"><span data-stu-id="8fe31-108">The following command verifies the signature, using the Default Authentication Verification Policy:</span></span>

<span data-ttu-id="8fe31-109">**SignTool Verify/PA** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="8fe31-109">**SignTool verify /pa** *MyControl.exe*</span></span>

<span data-ttu-id="8fe31-110">Mit dem folgenden Befehl wird eine Systemdatei überprüft, die möglicherweise in einem Katalog signiert ist:</span><span class="sxs-lookup"><span data-stu-id="8fe31-110">The following command verifies a system file that may be signed in a catalog:</span></span>

<span data-ttu-id="8fe31-111">**SignTool Verify/a** *SysFile.dll*</span><span class="sxs-lookup"><span data-stu-id="8fe31-111">**SignTool verify /a** *SysFile.dll*</span></span>

<span data-ttu-id="8fe31-112">Mit dem folgenden Befehl wird eine Systemdatei überprüft, die in einem Katalog mit dem Namen *MyCat.cat* signiert ist:</span><span class="sxs-lookup"><span data-stu-id="8fe31-112">The following command verifies a system file that is signed in a catalog named *MyCat.cat*:</span></span>

<span data-ttu-id="8fe31-113">**SignTool Verify/c** *MyCat.catMyFile.ini*</span><span class="sxs-lookup"><span data-stu-id="8fe31-113">**SignTool verify /c** *MyCat.catMyFile.ini*</span></span>

<span data-ttu-id="8fe31-114">Für jede [SignTool](signtool.md) -Überprüfung können Sie den Signatur Geber des Zertifikats abrufen.</span><span class="sxs-lookup"><span data-stu-id="8fe31-114">For any [SignTool](signtool.md) verification, you can retrieve the signer of the certificate.</span></span> <span data-ttu-id="8fe31-115">Mit dem folgenden Befehl wird eine Systemdatei überprüft und das Signatur Geber Zertifikat angezeigt:</span><span class="sxs-lookup"><span data-stu-id="8fe31-115">The following command verifies a system file and displays the signer certificate:</span></span>

<span data-ttu-id="8fe31-116">**SignTool Verify/v** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="8fe31-116">**SignTool verify /v** *MyControl.exe*</span></span>

<span data-ttu-id="8fe31-117">[SignTool](signtool.md) gibt Befehlszeilen Text zurück, der das Ergebnis der Signatur Überprüfung angibt.</span><span class="sxs-lookup"><span data-stu-id="8fe31-117">[SignTool](signtool.md) returns command-line text that states the result of the signature check.</span></span> <span data-ttu-id="8fe31-118">Außerdem gibt SignTool den Exitcode 0 (null) für die erfolgreiche Ausführung zurück, einen für die fehlgeschlagene Ausführung und zwei für die Ausführung, die mit Warnungen abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="8fe31-118">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="8fe31-119">Weitere Informationen zu [SignTool](signtool.md)finden Sie unter [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="8fe31-119">For more information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 



