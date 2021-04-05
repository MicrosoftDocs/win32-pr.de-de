---
description: Crypt32.dll ist das Modul, das viele der CryptoAPI-Funktionen implementiert.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Crypt32.dll Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b55d78b3ff3654e4bf3e5956917dd8de20eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750921"
---
# <a name="crypt32dll-versions"></a><span data-ttu-id="47034-103">Crypt32.dll Versionen</span><span class="sxs-lookup"><span data-stu-id="47034-103">Crypt32.dll Versions</span></span>

<span data-ttu-id="47034-104">Crypt32.dll ist das Modul, das viele der Zertifikat-und kryptografienachrichtenfunktionen in der CryptoAPI implementiert, z. [**b. cryptsignmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span><span class="sxs-lookup"><span data-stu-id="47034-104">Crypt32.dll is the module that implements many of the Certificate and Cryptographic Messaging functions in the CryptoAPI, such as [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span></span> <span data-ttu-id="47034-105">Crypt32.dll ist ein Modul, das in den Betriebssystemen Windows und Windows Server enthalten ist, aber unterschiedliche Versionen dieser DLL bieten unterschiedliche Funktionen.</span><span class="sxs-lookup"><span data-stu-id="47034-105">Crypt32.dll is a module that comes with the Windows and Windows Server operating systems, but different versions of this DLL provide different capabilities.</span></span> <span data-ttu-id="47034-106">Es gibt keine API, um die verwendete kryptoapi-Version zu bestimmen, Sie können jedoch die Version von Crypt32.dll bestimmen, die derzeit verwendet wird, indem Sie die Funktionen [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) und [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) verwenden.</span><span class="sxs-lookup"><span data-stu-id="47034-106">There is no API to determine the version of CryptoAPI that is in use, but you can determine the version of Crypt32.dll that is currently in use by using the [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) and [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) functions.</span></span>

<span data-ttu-id="47034-107">Im Allgemeinen werden die Versions Bereiche von Crypt32.dll den Betriebssystemversionen zugeordnet, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="47034-107">In general, the version ranges of Crypt32.dll map to the operating system versions as shown in the following table.</span></span> <span data-ttu-id="47034-108">Diese Tabelle sollte jedoch nur als Richtlinie verwendet werden, da es in anderen Aktualisierungsmöglichkeiten möglich ist, dass sich die Crypt32.dll Version von der in der Tabelle aufgeführten unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="47034-108">However, this table should be used as a guideline only because it is possible, through other update avenues, that the Crypt32.dll version will differ from the one indicated in the table.</span></span>

| <span data-ttu-id="47034-109">Crypt32.dll Version</span><span class="sxs-lookup"><span data-stu-id="47034-109">Crypt32.dll version</span></span>                               | <span data-ttu-id="47034-110">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="47034-110">Operating system</span></span>                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47034-111">*Version* >= 5.131.3790.0</span><span class="sxs-lookup"><span data-stu-id="47034-111">*version* >= 5.131.3790.0</span></span>                      | <span data-ttu-id="47034-112">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="47034-112">Windows Server 2003</span></span>                                                                                                                                                             |
| <span data-ttu-id="47034-113">*Version* >= 5.131.2600.1243</span><span class="sxs-lookup"><span data-stu-id="47034-113">*version* >= 5.131.2600.1243</span></span>                   | <span data-ttu-id="47034-114">Windows XP mit Service Pack 2 (SP2) Windows XP mit Service Pack 1 (SP1) mit Hotfix [Q329433](https://support.microsoft.com/kb/329433)</span><span class="sxs-lookup"><span data-stu-id="47034-114">Windows XP with Service Pack 2 (SP2)Windows XP with Service Pack 1 (SP1) with hotfix [Q329433](https://support.microsoft.com/kb/329433)</span></span><br/> <span data-ttu-id="47034-115">Windows XP</span><span class="sxs-lookup"><span data-stu-id="47034-115">Windows XP</span></span><br/> |
| <span data-ttu-id="47034-116">5.131.2600.0 <= *Version* < 5.131.2600.1243</span><span class="sxs-lookup"><span data-stu-id="47034-116">5.131.2600.0 <= *version* < 5.131.2600.1243</span></span> | <span data-ttu-id="47034-117">Windows XP mit SP1Windows XP</span><span class="sxs-lookup"><span data-stu-id="47034-117">Windows XP with SP1Windows XP</span></span><br/>                                                                                                                                        |



 

 

 
