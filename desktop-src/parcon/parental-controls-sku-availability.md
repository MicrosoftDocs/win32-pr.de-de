---
description: Verfügbarkeit der Jugend Steuerungs SKU
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: Verfügbarkeit der Jugend Steuerungs SKU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b858bc62e8f10a3b06313befd99d67e497b8d442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349194"
---
# <a name="parental-controls-sku-availability"></a><span data-ttu-id="a1f84-103">Verfügbarkeit der Jugend Steuerungs SKU</span><span class="sxs-lookup"><span data-stu-id="a1f84-103">Parental Controls SKU Availability</span></span>

<span data-ttu-id="a1f84-104">Die Jugend Schnittstellen, Features und APIs, die in diesem Abschnitt beschrieben werden, sind zurzeit nur für kundenorientierte SKUs verfügbar, wie z. b.:</span><span class="sxs-lookup"><span data-stu-id="a1f84-104">The Parental Controls user interfaces, features, and APIs described in this section are currently planned to be available only on consumer-focused SKUs such as:</span></span>

-   <span data-ttu-id="a1f84-105">Windows Vista Starter</span><span class="sxs-lookup"><span data-stu-id="a1f84-105">Windows Vista Starter</span></span>
-   <span data-ttu-id="a1f84-106">Windows Vista Home Basic</span><span class="sxs-lookup"><span data-stu-id="a1f84-106">Windows Vista Home Basic</span></span>
-   <span data-ttu-id="a1f84-107">Windows Vista Home Premium</span><span class="sxs-lookup"><span data-stu-id="a1f84-107">Windows Vista Home Premium</span></span>
-   <span data-ttu-id="a1f84-108">Windows Vista Ultimate</span><span class="sxs-lookup"><span data-stu-id="a1f84-108">Windows Vista Ultimate</span></span>

<span data-ttu-id="a1f84-109">Elterliche Kontrollen werden nur auf diesen SKUs installiert.</span><span class="sxs-lookup"><span data-stu-id="a1f84-109">Parental Controls only installs on these SKUs.</span></span> <span data-ttu-id="a1f84-110">Lösungen, die eine Anforderung für die Bereitstellung auf Geschäfts-SKUs haben, müssen Folgendes erfüllen:</span><span class="sxs-lookup"><span data-stu-id="a1f84-110">Solutions having a requirement to deploy onto business SKUs will need to either:</span></span>

-   <span data-ttu-id="a1f84-111">Erkennen Sie die Funktionen der Jugend Steuerungsfunktionen auf Geschäfts-SKUs</span><span class="sxs-lookup"><span data-stu-id="a1f84-111">Detect and not provide parental controls functionality on business SKUs.</span></span>
-   <span data-ttu-id="a1f84-112">Erkennen und Bereitstellen alternativer Konfigurations-, Protokollierungs-und Einschränkungs Möglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="a1f84-112">Detect and provide an alternative means of configuration, logging, and restrictions.</span></span>

<span data-ttu-id="a1f84-113">Es wird empfohlen, dass Lösungen die Verfügbarkeit der Jugend Steuerungs Infrastruktur erkennen, indem Sie den Erfolg von com cokreateinstance für die Konformitäts-API überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a1f84-113">It is recommended that solutions detect availability of the Parental Controls Infrastructure by checking for success of COM CoCreateInstance on the Compliance API.</span></span>

<span data-ttu-id="a1f84-114">Elterliche Steuerelemente: abhängig von der Windows Vista-Infrastruktur können auch alle Benutzeroberflächen unterdrückt werden, die Einstellungen oder andere Funktionen verfügbar machen, wenn die Benutzeroberfläche für die Jugend Steuerungsmöglichkeiten auf einer unterstützten SKU unterdrückt wird.</span><span class="sxs-lookup"><span data-stu-id="a1f84-114">Parental Controls-aware applications depending on the Windows Vista infrastructure may also want to suppress any of their own UI exposing settings or other functionality when Parental Controls UI is suppressed on a supported SKU.</span></span> <span data-ttu-id="a1f84-115">Eine Funktion wird zur Sichtbarkeits Bestimmung bereitgestellt, die Fälle wie z. b. eine in die Domäne eingebundenen Unterdrückung</span><span class="sxs-lookup"><span data-stu-id="a1f84-115">A function is provided for visibility determination that covers cases such as domain-joined suppression.</span></span>

 

 



