---
title: Bedarfs gesteuerte Installation von Windows-Komponenten
description: Bedarfs gesteuerte Installation von Windows-Komponenten
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d2c3c3fee1cd12d7b12900e41dc006badcf53f
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104039738"
---
# <a name="windows-components-installed-on-demand"></a><span data-ttu-id="b8778-103">Bedarfs gesteuerte Installation von Windows-Komponenten</span><span class="sxs-lookup"><span data-stu-id="b8778-103">Windows components installed on demand</span></span>

## <a name="platform"></a><span data-ttu-id="b8778-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="b8778-104">Platform</span></span>

<span data-ttu-id="b8778-105">**Clients:** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b8778-105">**Clients -** Windows 8.1</span></span>  







## <a name="description"></a><span data-ttu-id="b8778-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8778-106">Description</span></span>

<span data-ttu-id="b8778-107">Zwei Windows-Komponenten werden Bedarfs gesteuert in Windows 8.1 installiert: DirectPlay und ntvdm.</span><span class="sxs-lookup"><span data-stu-id="b8778-107">Two Windows components will be installed on demand in Windows 8.1: DirectPlay and NTVDM.</span></span> <span data-ttu-id="b8778-108">Diese Komponenten werden in optionalen Komponenten unter dem Knoten "Legacy Komponenten" aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8778-108">These components are listed within Optional Components under the “Legacy Components” node.</span></span> <span data-ttu-id="b8778-109">Diese Komponenten werden lokal als Teil des Betriebssystems installiert und als optionale Komponenten komprimiert.</span><span class="sxs-lookup"><span data-stu-id="b8778-109">These components are installed locally as part of the operating system, and compressed as optional components.</span></span> <span data-ttu-id="b8778-110">Wenn eine APP auf eine dieser Komponenten verweist oder diese aufruft (in der Regel beim ersten Start der APP), wird die Installation automatisch ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b8778-110">When an app references or calls one of these components (usually at first launch of the app), installation is triggered automatically.</span></span> <span data-ttu-id="b8778-111">Benutzer werden benachrichtigt, dass die Komponente installiert wird, und Sie müssen die Aktion bestätigen, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="b8778-111">Users will be notified that the component will be installed, and they must confirm the action in order to proceed.</span></span> <span data-ttu-id="b8778-112">Eine Erhöhung ist erforderlich, damit dies erfolgreich ist, wenn der Benutzer kein Administrator ist.</span><span class="sxs-lookup"><span data-stu-id="b8778-112">Elevation is required for this to succeed if the user is not an administrator.</span></span> <span data-ttu-id="b8778-113">Nach der Erstinstallation muss der Benutzer keine weiteren Aktionen ausführen, um die Komponente erneut zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8778-113">After the initial installation, the user does not need to perform any other actions to use the component again.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b8778-114">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="b8778-114">Manifestation</span></span>

<span data-ttu-id="b8778-115">Wenn eine APP auf eine Legacy Komponente in optionalen Komponenten (beim ersten Start) verweist oder diese aufruft, wird die APP angehalten, und das Dialogfeld für die Bedarfs gesteuerte Funktion wird geöffnet, und die Benutzer Berechtigung zum Installieren der Komponente wird angefordert.</span><span class="sxs-lookup"><span data-stu-id="b8778-115">When an app references or calls a legacy component in optional components (at first launch), the app will be suspended and the Feature on Demand dialog will open, requesting user permission to install the component.</span></span> <span data-ttu-id="b8778-116">Wenn Benutzer auf OK klicken, wird möglicherweise auch eine Eingabeaufforderung für erhöhte Rechte angezeigt, in der Sie Ihre Anmelde Informationen eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="b8778-116">If users click OK, they may also see an elevation prompt where they must enter their credentials.</span></span> <span data-ttu-id="b8778-117">Die Komponente wird dann installiert, und die APP wird fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b8778-117">The component will then be installed and the app will resume.</span></span>

## <a name="mitigation"></a><span data-ttu-id="b8778-118">Minderung</span><span class="sxs-lookup"><span data-stu-id="b8778-118">Mitigation</span></span>

<span data-ttu-id="b8778-119">Um das Öffnen der Features für die Bedarfs gesteuerte Benutzeroberfläche zu gewährleisten, können Sie DirectPlay und NTVDM mithilfe von "dismus" oder der optionalen Komponenten-Benutzeroberfläche vorinstallieren.</span><span class="sxs-lookup"><span data-stu-id="b8778-119">To keep the Features on Demand UI from opening, you can pre-install DirectPlay and NTVDM using DISM or the Optional Components UI.</span></span>

## <a name="solution"></a><span data-ttu-id="b8778-120">Lösung</span><span class="sxs-lookup"><span data-stu-id="b8778-120">Solution</span></span>

<span data-ttu-id="b8778-121">Es wird dringend empfohlen, dass Sie in zukünftigen Versionen Ihrer APP nicht auf Komponenten verweisen oder diese aufrufen, die als optionale Legacy Komponenten in Windows aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b8778-121">You are strongly encouraged to avoid referencing or calling components that have been listed as Legacy Optional Components in Windows in future versions of your app.</span></span> <span data-ttu-id="b8778-122">Optionale Legacy Komponenten enthalten nur ältere, weniger genutzte Komponenten, die möglicherweise Leistungs-und Sicherheitsprobleme für Benutzer verursachen.</span><span class="sxs-lookup"><span data-stu-id="b8778-122">Legacy Optional Components will only include older, lesser-used components that could potentially cause performance and security issues for users.</span></span>

## <a name="tests"></a><span data-ttu-id="b8778-123">Tests</span><span class="sxs-lookup"><span data-stu-id="b8778-123">Tests</span></span>

<span data-ttu-id="b8778-124">Aus Kompatibilitätsgründen sind keine weiteren Test Unterkünfte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8778-124">No additional test accommodations are necessary for compatibility.</span></span> <span data-ttu-id="b8778-125">Beachten Sie, dass dieses Dialogfeld angezeigt wird, wenn die optionale Komponente aufgerufen wird oder referenziert wird. diese Installation erfordert eine Erhöhung der Rechte.</span><span class="sxs-lookup"><span data-stu-id="b8778-125">It is important to be aware that this dialog will appear when the optional component is called or referenced, and this installation requires elevation.</span></span>

 

 




