---
title: Wichtige Änderungen seit Windows 7, um die Kompatibilität zu gewährleisten
description: Wichtige Änderungen seit Windows 7, um die Kompatibilität zu gewährleisten
ms.assetid: 6930AA8C-B9AE-44C0-BC7F-12342DBBEB5E
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ee24b18be55ff498d6c3870f77a32270df68284
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310848"
---
# <a name="key-changes-since-windows-7-to-ensure-compatibility"></a><span data-ttu-id="5546d-103">Wichtige Änderungen seit Windows 7, um die Kompatibilität zu gewährleisten</span><span class="sxs-lookup"><span data-stu-id="5546d-103">Key changes since Windows 7 to ensure compatibility</span></span>

<span data-ttu-id="5546d-104">Kompatibilität hat für Entwickler einen hohen Stellenwert.</span><span class="sxs-lookup"><span data-stu-id="5546d-104">We understand that compatibility matters to developers.</span></span> <span data-ttu-id="5546d-105">ISVs und Entwickler möchten sicherstellen, dass ihre Apps unter allen unterstützten Versionen des Windows-Betriebssystems erwartungsgemäß ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5546d-105">ISVs and developers want to ensure their apps will run as expected on all supported versions of the Windows OS.</span></span> <span data-ttu-id="5546d-106">Verbraucher und Unternehmen haben ebenfalls ein Interesse daran, dass die von ihnen erworbenen Apps weiterhin funktionieren.</span><span class="sxs-lookup"><span data-stu-id="5546d-106">Consumers and businesses have a key investment here—they want to ensure that the apps they have paid for will continue to work.</span></span> <span data-ttu-id="5546d-107">Wir wissen, dass Kompatibilität das Hauptkriterium für die Kaufentscheidung ist.</span><span class="sxs-lookup"><span data-stu-id="5546d-107">We know that compatibility is the primary criteria for purchase decisions.</span></span> <span data-ttu-id="5546d-108">Apps, die basierend auf bewährten Methoden ordnungsgemäß geschrieben werden, führen zu einer deutlich geringeren Codeänderung, wenn eine neue Windows-Version veröffentlicht wird. Dadurch wird die Fragmentierung reduziert – diese apps haben eine reduzierte Entwicklungs Investition und eine schnellere Markteinführungszeit.</span><span class="sxs-lookup"><span data-stu-id="5546d-108">Apps that are well written based on best practices will lead to much less code churn when a new Windows version is released, and will reduce fragmentation—these apps have a reduced engineering investment to maintain, and a faster time to market.</span></span>

<span data-ttu-id="5546d-109">Zu Zeiten von Windows 7 ging es vielmehr darum, auf Kompatibilitätsprobleme zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="5546d-109">In the Windows 7 timeframe, compatibility was very much a reactive approach.</span></span> <span data-ttu-id="5546d-110">In Windows 8 haben wir umgedacht und direkt innerhalb des Windows-Betriebssystems und nicht erst im Nachhinein für Kompatibilität gesorgt.</span><span class="sxs-lookup"><span data-stu-id="5546d-110">In Windows 8, we started looking at this differently, working within Windows to ensure that compatibility was by design rather than an afterthought.</span></span> <span data-ttu-id="5546d-111">Windows 10 ist entwurfsbedingt die bisher kompatibelste Betriebssystemversion.</span><span class="sxs-lookup"><span data-stu-id="5546d-111">Windows 10 is the most compatible-by-design version of the OS to date.</span></span> <span data-ttu-id="5546d-112">Einige wichtige Aspekte, die uns bei der Umsetzung geholfen haben:</span><span class="sxs-lookup"><span data-stu-id="5546d-112">Here are some key ways we accomplished this:</span></span>

-   <span data-ttu-id="5546d-113">App-Telemetrie: Dies hilft uns, die Beliebtheit von apps im Windows-Ökosystem zu verstehen, um Kompatibilitätstests zu informieren.</span><span class="sxs-lookup"><span data-stu-id="5546d-113">App telemetry: this helps us understand app popularity in the Windows ecosystem to inform compatibility testing.</span></span>
-   <span data-ttu-id="5546d-114">ISV-Partnerschaften: Arbeiten Sie direkt mit externen Partnern zusammen, um Ihnen Daten bereitzustellen und Probleme zu beheben, die unsere Benutzer haben.</span><span class="sxs-lookup"><span data-stu-id="5546d-114">ISV partnerships: work directly with external partners to provide them with data and help fix issues that our users experience.</span></span>
-   <span data-ttu-id="5546d-115">Entwurfs Überprüfungen, Upstream-Erkennung: Partner mit Featureteams, um die Anzahl der wichtigen Änderungen in Windows zu verringern.</span><span class="sxs-lookup"><span data-stu-id="5546d-115">Design reviews, upstream detection: partner with feature teams to reduce the number of breaking changes in Windows.</span></span> <span data-ttu-id="5546d-116">Kompatibilitätsprüfungen sind für jedes Featureteam ein Muss.</span><span class="sxs-lookup"><span data-stu-id="5546d-116">Compatibility review is a gate that our feature teams must pass.</span></span>
-   <span data-ttu-id="5546d-117">Strengere Kontrolle über API-Änderungen & verbesserte Kommunikation</span><span class="sxs-lookup"><span data-stu-id="5546d-117">Tighter control over API changes & improved communication</span></span>
-   <span data-ttu-id="5546d-118">Flighting-und Feedback Schleife: die Windows Insider Population erhält geflistete Builds, die zur Verbesserung unserer Fähigkeit zum Auffinden von Kompatibilitätsproblemen beitragen, bevor ein endgültiger Build für Kunden veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="5546d-118">Flighting and feedback loop: The Windows Insider population receives flighted builds that help improve our ability to find compatibility issues before a final build is released to customers.</span></span> <span data-ttu-id="5546d-119">Unser Feedbackverfahren sorgt nicht nur für die Fehlererkennung, sondern auch dafür, dass Benutzer die Features erhalten, die sie brauchen.</span><span class="sxs-lookup"><span data-stu-id="5546d-119">This feedback process not only exposes bugs, but ensures we are shipping features our users want.</span></span>

 

 




