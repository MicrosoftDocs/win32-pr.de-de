---
description: Auf 64-Bit-Fenstern werden Teile der Registrierungseinträge separat für die 32-Bit-Anwendung und 64-Bit-Anwendungen gespeichert und mithilfe des registrierungsredirectors und der Registrierungs Reflektion separaten logischen Registrierungs Sichten zugeordnet, da die 64-Bit-Version einer Anwendung andere Registrierungsschlüssel und-Werte als die 32-Bit-Version verwenden kann. Es gibt auch freigegebene Registrierungsschlüssel, die nicht umgeleitet oder reflektiert werden.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: 32-Bit-und 64-Bit-Anwendungsdaten in der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc82dfbf9b22cf90866e13109aeea2bcdb10e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865396"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a><span data-ttu-id="924f3-104">32-Bit-und 64-Bit-Anwendungsdaten in der Registrierung</span><span class="sxs-lookup"><span data-stu-id="924f3-104">32-bit and 64-bit Application Data in the Registry</span></span>

<span data-ttu-id="924f3-105">Auf 64-Bit-Fenstern werden Teile der Registrierungseinträge separat für die 32-Bit-Anwendung und 64-Bit-Anwendungen gespeichert und mithilfe des [registrierungsredirectors](/windows/desktop/WinProg64/registry-redirector) und der [Registrierungs Reflektion](/windows/desktop/WinProg64/registry-reflection)separaten logischen Registrierungs Sichten zugeordnet, da die 64-Bit-Version einer Anwendung andere Registrierungsschlüssel und-Werte als die 32-Bit-Version verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="924f3-105">On 64-bit Windows, portions of the registry entries are stored separately for 32-bit application and 64-bit applications and mapped into separate logical registry views using the [registry redirector](/windows/desktop/WinProg64/registry-redirector) and [registry reflection](/windows/desktop/WinProg64/registry-reflection), because the 64-bit version of an application may use different registry keys and values than the 32-bit version.</span></span> <span data-ttu-id="924f3-106">Es gibt auch frei [gegebene Registrierungsschlüssel](/windows/desktop/WinProg64/shared-registry-keys) , die nicht umgeleitet oder reflektiert werden.</span><span class="sxs-lookup"><span data-stu-id="924f3-106">There are also [shared registry keys](/windows/desktop/WinProg64/shared-registry-keys) that are not redirected or reflected.</span></span>

<span data-ttu-id="924f3-107">Das übergeordnete Element der einzelnen 64-Bit-Registrierungs Knoten ist der Image-Specific Knoten oder isn.</span><span class="sxs-lookup"><span data-stu-id="924f3-107">The parent of each 64-bit registry node is the Image-Specific Node or ISN.</span></span> <span data-ttu-id="924f3-108">Der Registrierungs Redirector leitet den Registrierungs Zugriff einer Anwendung auf den entsprechenden isn-unter Knoten transparent um.</span><span class="sxs-lookup"><span data-stu-id="924f3-108">The registry redirector transparently directs an application's registry access to the appropriate ISN subnode.</span></span> <span data-ttu-id="924f3-109">Umleitungs unter Knoten in der Registrierungs Struktur werden automatisch von der WOW64-Komponente mit dem Namen **Wow6432Node** erstellt.</span><span class="sxs-lookup"><span data-stu-id="924f3-109">Redirection subnodes in the registry tree are created automatically by the WOW64 component using the name **Wow6432Node**.</span></span> <span data-ttu-id="924f3-110">Daher ist es von entscheidender Bedeutung, keinen Registrierungsschlüssel zu benennen, den Sie **Wow6432Node** erstellen.</span><span class="sxs-lookup"><span data-stu-id="924f3-110">As a result, it is essential not to name any registry key you create **Wow6432Node**.</span></span>

<span data-ttu-id="924f3-111">Die \_ Flags Key WOW64 \_ 64key und Key \_ WOW64 \_ 32key ermöglichen expliziten Zugriff auf die 64-Bit-Registrierungs Ansicht bzw. die 32-Bit-Sicht.</span><span class="sxs-lookup"><span data-stu-id="924f3-111">The KEY\_WOW64\_64KEY and KEY\_WOW64\_32KEY flags enable explicit access to the 64-bit registry view and the 32-bit view, respectively.</span></span> <span data-ttu-id="924f3-112">Weitere Informationen finden Sie unter [zugreifen auf eine Alternative Registrierungs Ansicht](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).</span><span class="sxs-lookup"><span data-stu-id="924f3-112">For more information, see [Accessing an Alternate Registry View](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).</span></span>

<span data-ttu-id="924f3-113">Um die Registrierungs Reflektion für einen bestimmten Schlüssel zu deaktivieren und zu aktivieren, verwenden Sie die Funktionen [**regdisablereflectionkey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) und [**regenablereflectionkey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) .</span><span class="sxs-lookup"><span data-stu-id="924f3-113">To disable and enable registry reflection for a particular key, use the [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) and [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) functions.</span></span> <span data-ttu-id="924f3-114">Anwendungen sollten die Reflektion nur für die von Ihnen erstellten Registrierungsschlüssel deaktivieren und nicht versuchen, die Reflektion für die vordefinierten Schlüssel zu deaktivieren, wie z. b. **HKEY \_ local \_ Machine** oder **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="924f3-114">Applications should disable reflection only for the registry keys that they create and not attempt to disable reflection for the predefined keys such as **HKEY\_LOCAL\_MACHINE** or **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="924f3-115">Verwenden Sie die [**regqueryreflectionkey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) -Funktion, um zu bestimmen, welche Schlüssel in der reflektionsliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="924f3-115">To determine which keys are on the reflection list, use the [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="924f3-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="924f3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="924f3-117">Registrierungs Redirector</span><span class="sxs-lookup"><span data-stu-id="924f3-117">registry redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[<span data-ttu-id="924f3-118">Registrierungs Reflektion</span><span class="sxs-lookup"><span data-stu-id="924f3-118">registry reflection</span></span>](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
