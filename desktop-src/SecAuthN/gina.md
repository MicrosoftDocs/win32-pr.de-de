---
description: Der Zweck einer Gina-DLL besteht darin, anpassbare benutzeridentifizierungs-und Authentifizierungsverfahren bereitzustellen. Die Standard-Gina übernimmt dies durch Delegieren der SAS-Ereignisüberwachung an Winlogon, das CTL + ALT + ENTF-Taste (Secure Monitoring Sequenzen, SASs) empfängt und verarbeitet.
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: Gina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084a65ad42bdbe030e697481501a4dc60e54baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758268"
---
# <a name="gina"></a><span data-ttu-id="aef35-104">Gina</span><span class="sxs-lookup"><span data-stu-id="aef35-104">GINA</span></span>

<span data-ttu-id="aef35-105">Die [*Gina*](/windows/desktop/SecGloss/g-gly) arbeitet im [*Kontext*](/windows/desktop/SecGloss/c-gly) des [*Winlogon*](/windows/desktop/SecGloss/w-gly) -Prozesses, sodass die Gina-DLL sehr früh im Startvorgang geladen wird.</span><span class="sxs-lookup"><span data-stu-id="aef35-105">The [*GINA*](/windows/desktop/SecGloss/g-gly) operates in the [*context*](/windows/desktop/SecGloss/c-gly) of the [*Winlogon*](/windows/desktop/SecGloss/w-gly) process and, as such, the GINA DLL is loaded very early in the boot process.</span></span> <span data-ttu-id="aef35-106">Die Gina-DLL muss Regeln befolgen, damit die Integrität des Systems beibehalten wird, insbesondere in Bezug auf die Interaktion mit dem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="aef35-106">The GINA DLL must follow rules so that the integrity of the system is maintained, particularly with respect to interaction with the user.</span></span>

> [!Note]  
> <span data-ttu-id="aef35-107">Gina-DLLs werden in Windows Vista ignoriert.</span><span class="sxs-lookup"><span data-stu-id="aef35-107">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="aef35-108">Die Gina wird häufig verwendet, um mit einem externen Gerät wie z. b. einem [*Smartcardleser*](/windows/desktop/SecGloss/r-gly)zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="aef35-108">The most common use of the GINA is to communicate with an external device such as a smart-card [*reader*](/windows/desktop/SecGloss/r-gly).</span></span> <span data-ttu-id="aef35-109">Es ist von entscheidender Bedeutung, den Startparameter für den Gerätetreiber auf System (WinNT. h: Service \_ System \_ Start) festzulegen, um sicherzustellen, dass der Treiber zum Zeitpunkt des aufgerufenen von Gina geladen wird.</span><span class="sxs-lookup"><span data-stu-id="aef35-109">It is essential to set the start parameter for the device driver to system (Winnt.h: SERVICE\_SYSTEM\_START) to ensure that the driver is loaded by the time the GINA is invoked.</span></span>

<span data-ttu-id="aef35-110">Der Zweck einer Gina-DLL besteht darin, anpassbare benutzeridentifizierungs-und Authentifizierungsverfahren bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="aef35-110">The purpose of a GINA DLL is to provide customizable user identification and authentication procedures.</span></span> <span data-ttu-id="aef35-111">Die Standard-Gina übernimmt dies durch Delegieren der SAS-Ereignisüberwachung an Winlogon, das CTL + ALT + ENTF-Taste ( [*Secure Monitoring Sequenzen*](/windows/desktop/SecGloss/s-gly) , SASs) empfängt und verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="aef35-111">The default GINA does this by delegating SAS event monitoring to Winlogon, which receives and processes CTL+ALT+DEL [*secure attention sequences*](/windows/desktop/SecGloss/s-gly) (SASs).</span></span> <span data-ttu-id="aef35-112">Eine benutzerdefinierte Gina ist dafür verantwortlich, sich selbst für das Empfangen von SAS-Ereignissen (außer der standardmäßigen Taste STRG + ALT + ENTF) und die Benachrichtigung von Winlogon, wenn SAS-Ereignisse auftreten, einzurichten.</span><span class="sxs-lookup"><span data-stu-id="aef35-112">A custom GINA is responsible for setting itself up to receive SAS events (other than the default CTRL+ALT+DEL SAS event) and notifying Winlogon when SAS events occur.</span></span> <span data-ttu-id="aef35-113">Winlogon wertet seinen Status aus, um zu bestimmen, was für die Verarbeitung der benutzerdefinierten Gina-SAS erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="aef35-113">Winlogon will evaluate its state to determine what is required to process the custom GINA's SAS.</span></span> <span data-ttu-id="aef35-114">Diese Verarbeitung beinhaltet in der Regel Aufrufe der SAS-Verarbeitungsfunktionen von Gina.</span><span class="sxs-lookup"><span data-stu-id="aef35-114">This processing usually includes calls to the GINA's SAS processing functions.</span></span>

<span data-ttu-id="aef35-115">Informationen zu bestimmten Gina-Exportfunktionen finden Sie unter [Gina-Exportfunktionen](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="aef35-115">For information about specific GINA export functions, see [GINA Export Functions](authentication-functions.md).</span></span> <span data-ttu-id="aef35-116">Informationen zum Verwenden von Gina-Strukturen zum Übergeben von Informationen finden Sie unter [Gina-Strukturen](authentication-structures.md).</span><span class="sxs-lookup"><span data-stu-id="aef35-116">For information about using GINA structures to pass information, see [GINA Structures](authentication-structures.md).</span></span>



| <span data-ttu-id="aef35-117">Thema</span><span class="sxs-lookup"><span data-stu-id="aef35-117">Topic</span></span>                                                                             | <span data-ttu-id="aef35-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aef35-118">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="aef35-119">Laden und Ausführen einer Gina-dll</span><span class="sxs-lookup"><span data-stu-id="aef35-119">Loading and Running a GINA DLL</span></span>](loading-and-running-a-gina-dll.md)<br/>   | <span data-ttu-id="aef35-120">Welcher Registrierungsschlüssel Wert geändert wird, um eine benutzerdefinierte GINA-DLL zu laden und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="aef35-120">Which registry key value to alter to load and run a custom GINA DLL.</span></span><br/> |
| [<span data-ttu-id="aef35-121">Entwickeln und Testen einer Gina-dll</span><span class="sxs-lookup"><span data-stu-id="aef35-121">Building and Testing a GINA DLL</span></span>](building-and-testing-a-gina-dll.md)<br/> | <span data-ttu-id="aef35-122">So testen Sie eine Gina-DLL.</span><span class="sxs-lookup"><span data-stu-id="aef35-122">How to test a GINA DLL.</span></span><br/>                                              |



 

 

