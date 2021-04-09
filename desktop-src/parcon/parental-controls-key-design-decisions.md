---
description: Wichtige Entwurfsentscheidungen für Eltern Steuerelemente
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Wichtige Entwurfsentscheidungen für Eltern Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39cb4be775a3380cb9fe7aa677362df31a2dc453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050496"
---
# <a name="parental-controls-key-design-decisions"></a><span data-ttu-id="aefa7-103">Wichtige Entwurfsentscheidungen für Eltern Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="aefa7-103">Parental Controls Key Design Decisions</span></span>

<span data-ttu-id="aefa7-104">Wichtige Entwurfsentscheidungen bei der Entwicklung von Windows Vista-Jugendschutz-Steuerelementen:</span><span class="sxs-lookup"><span data-stu-id="aefa7-104">Major design decisions in the development of Windows Vista Parental Controls are:</span></span>

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a><span data-ttu-id="aefa7-105">Wesentliche Abhängigkeit von der Windows Vista-Benutzerkontensteuerung (User Account Control, UAC)</span><span class="sxs-lookup"><span data-stu-id="aefa7-105">Essential Dependency on Windows Vista User Account Control (UAC) Feature</span></span>

<span data-ttu-id="aefa7-106">Eine wichtige Entscheidung für die Jugendschutzbestimmungen in Windows Vista besteht darin, dass Sie sich auf die neue Benutzerkontensteuerung (User Account Control, UAC) stützen, um die eingeschränkten Rechte Konto Identitäten zu implementieren, die besonders für Offline Beschränkungen bei kontrollierten Benutzern</span><span class="sxs-lookup"><span data-stu-id="aefa7-106">A key decision for Windows Vista Parental Controls is to rely on the new User Account Control (UAC) feature to implement the reduced rights account identities especially needed for offline restrictions on controlled users.</span></span> <span data-ttu-id="aefa7-107">Weitere Informationen zur [Benutzerkontensteuerung finden Sie unter Windows Vista und Windows Server 2008 Developer Story: Anforderungen für die Windows Vista-Anwendungsentwicklung für die Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905330(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="aefa7-107">For more information about UAC, see [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)).</span></span> <span data-ttu-id="aefa7-108">Zusammenfassend gilt: jedes Konto mit Administratorrechten verfügt über Berechtigungen zum Ausführen der übergeordneten Rolle oder der Rolle "Wächter" zum Anzeigen von Protokolldaten und Festlegen von Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="aefa7-108">In summary, every account with administrator rights effectively has privileges to perform the parent or guardian role of viewing log data and setting policies.</span></span> <span data-ttu-id="aefa7-109">Eltern Steuerelemente können nur für Benutzer mit Standard rechten (früher als Benutzerkonten mit den geringsten Rechten bezeichnet) festgelegt werden, da Sie nur Protokolle und Einstellungen mit Access Control Listen ändern können, die nur für Administratoren konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="aefa7-109">Parental controls may only be set on standard-rights users (formerly called Least-privileged User Accounts, or LUAs), as only they cannot alter logs and settings with Access Control Lists (ACLs) configured only for administrators to write.</span></span> <span data-ttu-id="aefa7-110">Anders gesagt:</span><span class="sxs-lookup"><span data-stu-id="aefa7-110">In other words:</span></span>

-   <span data-ttu-id="aefa7-111">Eine übergeordnete Identität oder eine Überwachungs Identität ist implizit mit einem Konto mit rechten eines Administrators gleich.</span><span class="sxs-lookup"><span data-stu-id="aefa7-111">A parent or guardian identity implicitly equals an account that has rights of an administrator.</span></span>
-   <span data-ttu-id="aefa7-112">Der Benutzer muss Standardbenutzer sein.</span><span class="sxs-lookup"><span data-stu-id="aefa7-112">Parentally controlled users must be standard users.</span></span>

## <a name="nearly-all-settings-are-available-by-apis"></a><span data-ttu-id="aefa7-113">Fast alle Einstellungen sind über APIs verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aefa7-113">Nearly All Settings Are Available by APIs</span></span>

<span data-ttu-id="aefa7-114">Mit Ausnahme von Elementen wie z. b. Bewertungssystem Definitionen können von der Benutzeroberfläche für die Jugend Kontrollen verfügbare Einstellungen auch durch verfügbar gemachte APIs geändert werden.</span><span class="sxs-lookup"><span data-stu-id="aefa7-114">With the exception of items such as ratings system definitions, settings available for manipulation by the Parental Controls User Interface may also be modified by exposed APIs.</span></span> <span data-ttu-id="aefa7-115">Es ist erforderlich, dass Programme Erweiterungen in Administratorrechte implementieren, um die Einstellungen zu ändern, wie oben für die UAC erwähnt.</span><span class="sxs-lookup"><span data-stu-id="aefa7-115">It is necessary for programs to implement elevation to administrative rights in order to alter settings, as noted above for UAC.</span></span>

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a><span data-ttu-id="aefa7-116">Die Jugend Steuerungselemente von Windows Vista sind eine reine consumertechnologie.</span><span class="sxs-lookup"><span data-stu-id="aefa7-116">Windows Vista Parental Controls Is a Consumer-only Technology</span></span>

<span data-ttu-id="aefa7-117">Die Jugend Steuerungselemente von Windows Vista sind nicht für die Verwendung mit Domänen Konten vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="aefa7-117">Windows Vista Parental Controls are not intended to be used with domain accounts.</span></span> <span data-ttu-id="aefa7-118">Als consumertechnologie werden Eltern Kontrollen nicht in Geschäfts-SKUs von Windows Vista bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="aefa7-118">As a consumer technology, Parental Controls is not deployed in business SKUs of Windows Vista.</span></span> <span data-ttu-id="aefa7-119">Wenn ein Computer einer Domäne hinzugefügt wird, werden die Links für die Benutzeroberfläche der Familien Sicherheit unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="aefa7-119">If a computer is joined to a domain, the Family Safety user interface links will be suppressed.</span></span>

<span data-ttu-id="aefa7-120">Es wird ein Mechanismus bereitgestellt, um die Funktionalität für den in die Domäne eingebundenen Fall verfügbar zu machen, aber nur nicht-Domänen Benutzerkonten können mit Jugendschutz-Steuerelementen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="aefa7-120">A mechanism will be provided to expose the functionality for the domain-joined case, but only non-domain user accounts may be configured with Parental Controls.</span></span>

 

 
