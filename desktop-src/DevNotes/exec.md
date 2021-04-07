---
description: HKLM \\ Software \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2711b2c8882f9af12de2f060810ccd4219faa5ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748760"
---
# <a name="exec"></a><span data-ttu-id="d5546-103">Exec</span><span class="sxs-lookup"><span data-stu-id="d5546-103">Exec</span></span>

<span data-ttu-id="d5546-104">**HKLM \\ Software \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**</span><span class="sxs-lookup"><span data-stu-id="d5546-104">**HKLM\\Software\\Microsoft\\Internet Explorer\\Extensions\\{e2e2dd38-d088-4134-82b7-f2ba38496583}**</span></span>



| <span data-ttu-id="d5546-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d5546-105">Data type</span></span> | <span data-ttu-id="d5546-106">Range</span><span class="sxs-lookup"><span data-stu-id="d5546-106">Range</span></span>                    | <span data-ttu-id="d5546-107">Standardwert</span><span class="sxs-lookup"><span data-stu-id="d5546-107">Default value</span></span> |
|-----------|--------------------------|---------------|
| <span data-ttu-id="d5546-108">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d5546-108">REG\_SZ</span></span>   | <span data-ttu-id="d5546-109">*Pfad zur ausführbaren Datei*</span><span class="sxs-lookup"><span data-stu-id="d5546-109">*Path to the executable*</span></span> |               |



 

## <a name="browser-integration-steps"></a><span data-ttu-id="d5546-110">Schritte zur Browser Integration</span><span class="sxs-lookup"><span data-stu-id="d5546-110">Browser Integration Steps</span></span>

1.  <span data-ttu-id="d5546-111">Verwenden Sie die [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) -Funktion, um zu bestimmen, ob die Netzwerk Diagnose installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d5546-111">Use the [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) function to determine whether the Network Diagnostic is installed.</span></span> <span data-ttu-id="d5546-112">Wenn Sie installiert ist, ist der Schlüssel **{e2e2dd38-d088-4134-82b7-f2ba38496583}** vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d5546-112">If it is installed, the **{e2e2dd38-d088-4134-82b7-f2ba38496583}** key is present.</span></span>
2.  <span data-ttu-id="d5546-113">Verwenden Sie die [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) -Funktion, um den Pfad der ausführbaren Datei für die Netzwerk Diagnose aus dem **exec** -Eintrag abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d5546-113">Use the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to retrieve the path of the Network Diagnostic executable file from the **Exec** entry.</span></span>
3.  <span data-ttu-id="d5546-114">Zeigen Sie die neue Fehlerseite an, wenn die Diagnose auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d5546-114">Display the new error page if the diagnostic is installed on the system.</span></span>
4.  <span data-ttu-id="d5546-115">Erstellen Sie eine Browser Erweiterung, mit der ein Standard Symbolleisten Element erstellt wird, wenn die Diagnose auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d5546-115">Create a browser extension that creates a standard toolbar item if the diagnostic is installed on the system.</span></span>
5.  <span data-ttu-id="d5546-116">Führen Sie die ausführbare Datei für die Netzwerk Diagnose mit dem in Schritt 2 abgerufenen Pfad aus</span><span class="sxs-lookup"><span data-stu-id="d5546-116">Execute the Network Diagnostic executable using the path retrieved in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5546-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d5546-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5546-118">Übersicht über die Features der Netzwerk Diagnose Tools</span><span class="sxs-lookup"><span data-stu-id="d5546-118">Network Diagnostics Tools Feature Overview</span></span>](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
