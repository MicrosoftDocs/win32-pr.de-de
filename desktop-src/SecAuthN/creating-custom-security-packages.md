---
description: Erläutert, wie ein benutzerdefiniertes Sicherheitspaket erstellt wird.
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: Erstellen von benutzerdefinierten Sicherheitspaketen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2136775d18e9d33f59d1b1f44fd817b3f3271ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866016"
---
# <a name="creating-custom-security-packages"></a><span data-ttu-id="6b638-103">Erstellen von benutzerdefinierten Sicherheitspaketen</span><span class="sxs-lookup"><span data-stu-id="6b638-103">Creating Custom Security Packages</span></span>

## <a name="ssp-security-packages"></a><span data-ttu-id="6b638-104">SSP-Sicherheitspakete</span><span class="sxs-lookup"><span data-stu-id="6b638-104">SSP Security Packages</span></span>

<span data-ttu-id="6b638-105">Wenn ein Sicherheitspaket für benutzerdefinierte Security Support Provider (SSP) ausschließlich für die Unterstützung von Client-/Serversicherheit verwendet wird, kann es die Microsoft [Security Support Provider-Schnittstelle](sspi.md)implementieren.</span><span class="sxs-lookup"><span data-stu-id="6b638-105">If a custom security support provider (SSP) security package will be used exclusively for client/server security support it can implement the Microsoft [Security Support Provider Interface](sspi.md).</span></span>

<span data-ttu-id="6b638-106">Das sampssp-Beispiel, das im Platform Software Development Kit (SDK) enthalten ist, enthält ein Beispiel für eine SSP-Sicherheitspaket Implementierung.</span><span class="sxs-lookup"><span data-stu-id="6b638-106">The SampSSP sample shipped with the Platform Software Development Kit (SDK) contains a sample SSP security package implementation.</span></span>

## <a name="sspap-security-packages"></a><span data-ttu-id="6b638-107">SSP/AP-Sicherheitspakete</span><span class="sxs-lookup"><span data-stu-id="6b638-107">SSP/AP Security Packages</span></span>

<span data-ttu-id="6b638-108">Benutzerdefinierte [*Security Support Provider*](/windows/desktop/SecGloss/s-gly) / [*Authentifizierungs Pakete*](/windows/desktop/SecGloss/a-gly) (SSP/APS) enthalten Sicherheitspakete, die als Authentifizierungs Pakete (APS) und Security Support Provider (SSPs) fungieren.</span><span class="sxs-lookup"><span data-stu-id="6b638-108">Custom [*security support provider*](/windows/desktop/SecGloss/s-gly)/[*authentication packages*](/windows/desktop/SecGloss/a-gly) (SSP/APs) contain security packages that function as authentication packages (APs) and security support providers (SSPs).</span></span> <span data-ttu-id="6b638-109">Diese Pakete implementieren separate APIs, um die einzelnen Rollen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6b638-109">These packages implement separate APIs to support each role.</span></span>

<span data-ttu-id="6b638-110">Da es als AP fungiert, muss ein benutzerdefiniertes SSP/AP- [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly) Implementierungen für alle Funktionen bereitstellen, die [von Authentifizierungs Paketen implementiert](authentication-functions.md)werden.</span><span class="sxs-lookup"><span data-stu-id="6b638-110">Because it functions as an AP, a custom SSP/AP [*security package*](/windows/desktop/SecGloss/s-gly) must provide implementations for all of the [Functions Implemented by Authentication Packages](authentication-functions.md).</span></span>

<span data-ttu-id="6b638-111">Zum Bereitstellen integrierter Sicherheitsunterstützung muss ein benutzerdefiniertes SSP/AP-Sicherheitspaket Implementierungen für die [von SSP/APS implementierten Funktionen](authentication-functions.md)bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6b638-111">To provide integrated security support, a custom SSP/AP security package must provide implementations for the [Functions implemented by SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="6b638-112">[LSA-Funktionen, die von SSP/APS aufgerufen werden](authentication-functions.md) , beschreiben die Unterstützungsfunktionen, die für die SSP/AP-Entwickler zur Verfügung stehen, die mit der LSA interagieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6b638-112">[LSA Functions Called by SSP/APs](authentication-functions.md) describes the support functions available to the SSP/AP developers that want to interact with the LSA.</span></span>

<span data-ttu-id="6b638-113">SSP/AP-Sicherheitspakete, die sowohl als AP als auch als SSP ausgeführt werden, können als Teil des Betriebssystems und als Teil einer Benutzeranwendung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6b638-113">SSP/AP security packages, in order to perform as both an AP and an SSP, may execute as part of the operating system and as part of a user application.</span></span> <span data-ttu-id="6b638-114">Diese zwei Ausführungsmodi werden als LSA-Modus bzw. Benutzermodus bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6b638-114">These two modes of execution are known as LSA mode and user mode, respectively.</span></span> <span data-ttu-id="6b638-115">Ausführliche Informationen zu benutzerdefinierten Sicherheitspaketen im LSA-Modus finden Sie unter [LSA Mode Initialization](lsa-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="6b638-115">For details about custom security packages in LSA mode see [LSA Mode Initialization](lsa-mode-initialization.md).</span></span> <span data-ttu-id="6b638-116">Ausführliche Informationen zum Benutzermodus finden Sie unter [benutzermodusinitialisierung](user-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="6b638-116">For details about user mode, see [User Mode Initialization](user-mode-initialization.md).</span></span>

<span data-ttu-id="6b638-117">Wenn ein benutzerdefiniertes SSP/AP-Sicherheitspaket Dienste für Client/Server-Anwendungen bereitstellt, sollte es Implementierungen für die Funktionen bereitstellen, die unter [von Benutzermodus-SSP/APS implementierte](authentication-functions.md)Funktionen beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6b638-117">If a custom SSP/AP security package offers services for client/server applications it should provide implementations for the functions described in [Functions Implemented by User-mode SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="6b638-118">[LSA-Funktionen, die vom benutzermodussp/APS aufgerufen werden](authentication-functions.md) , beschreiben die Unterstützungsfunktionen, die für eine SSP/AP-Ausführung in einem Client-oder Server Prozess verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6b638-118">[LSA Functions Called By User-mode SSP/APs](authentication-functions.md) describes the support functions available to an SSP/AP executing in a client or server process.</span></span>

<span data-ttu-id="6b638-119">Informationen zum Registrieren einer SSP/AP-dll finden Sie unter [Registrieren von SSP/AP-DLLs](registering-ssp-ap-dlls.md).</span><span class="sxs-lookup"><span data-stu-id="6b638-119">For information about registering an SSP/AP DLL, see [Registering SSP/AP DLLs](registering-ssp-ap-dlls.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b638-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b638-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b638-121">Einschränkungen bei der Registrierung und Installation eines Sicherheitspakets</span><span class="sxs-lookup"><span data-stu-id="6b638-121">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
