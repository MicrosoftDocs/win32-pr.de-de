---
description: Der letzte Schritt ist das Platzieren eines Verweises auf die Setup.exe auf der hypothetischen mySetup-Webseite (MySetup.html), die in einem URL-basierten Windows Installer-Installations Beispiel beschrieben wird.
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Erstellen eines HTML-Verweises auf Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c16e15f7f25c64467bcd38abf2941f6d99fc12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216369"
---
# <a name="establish-an-html-reference-to-setupexe"></a><span data-ttu-id="76fe8-103">Erstellen eines HTML-Verweises auf Setup.exe</span><span class="sxs-lookup"><span data-stu-id="76fe8-103">Establish an HTML Reference to Setup.exe</span></span>

<span data-ttu-id="76fe8-104">Der letzte Schritt ist das Platzieren eines Verweises auf die Setup.exe auf der hypothetischen mySetup-Webseite (MySetup.html), die in [einem URL-basierten Windows Installer-Installations Beispiel](a-url-based-windows-installer-installation-example.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="76fe8-104">The final step is to place a reference to the Setup.exe on the hypothetical MySetup webpage (MySetup.html) described in [A URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md).</span></span> <span data-ttu-id="76fe8-105">Verwenden Sie das folgende HTML-Skript:</span><span class="sxs-lookup"><span data-stu-id="76fe8-105">Use the following HTML script:</span></span>

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

<span data-ttu-id="76fe8-106">Durch Klicken auf den Link "mySetup-Installation" werden Benutzern die Option zum Speichern oder ausführen an diesem Speicherort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76fe8-106">Clicking on the "MySetup Installation" link presents users with the option to save or run from that location.</span></span> <span data-ttu-id="76fe8-107">Wenn der Benutzer die Option Ausführen von diesem Speicherort aus auswählt Setup.exe, wird die-Version der Windows Installer auf dem Computer aktualisiert, falls erforderlich, die digitale Signatur des Installationspakets überprüft und das Paket auf dem Computer installiert.</span><span class="sxs-lookup"><span data-stu-id="76fe8-107">If the user selects run from that location, the Setup.exe upgrades the version of Windows Installer on the computer, if necessary, verifies the digital signature on the installer package, and installs the package on their computer.</span></span>

<span data-ttu-id="76fe8-108">Dies schließt das Beispiel ab.</span><span class="sxs-lookup"><span data-stu-id="76fe8-108">This completes the example.</span></span>

 

 



