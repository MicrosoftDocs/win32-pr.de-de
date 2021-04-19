---
description: In diesem Tutorial werden die verschiedenen Aspekte aufgezeigt, die Webentwickler beim Entwerfen von Seiten für den webautorisierungs Ablauf für Windows 8 berücksichtigen sollten. In diesem Abschnitt wird ein zweiseitiger Autorisierungs Fluss veranschaulicht.
ms.assetid: A26E09EF-6C7A-4F75-89A7-76086F63F3B1
title: Tutorial zum Authentifizieren von Webseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6fc6482c5e6dfaf89a9fc9732783f5f088b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351413"
---
# <a name="tutorial-for-authenticating-web-pages"></a><span data-ttu-id="eb808-104">Tutorial zum Authentifizieren von Webseiten</span><span class="sxs-lookup"><span data-stu-id="eb808-104">Tutorial for authenticating web pages</span></span>

<span data-ttu-id="eb808-105">In diesem Tutorial werden die verschiedenen Aspekte aufgezeigt, die Webentwickler beim Entwerfen von Seiten für den webautorisierungs Ablauf für Windows 8 berücksichtigen sollten.</span><span class="sxs-lookup"><span data-stu-id="eb808-105">This tutorial highlights the different aspects that web developers should care about when designing pages for the web authorization flow for Windows 8.</span></span> <span data-ttu-id="eb808-106">In diesem Abschnitt wird ein zweiseitiger Autorisierungs Fluss veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="eb808-106">This section This sample demonstrates a two-page authorization flow.</span></span>

<span data-ttu-id="eb808-107">**Ziel:** Das Ziel des Beispiels ist nicht, sich mit dem Layout oder visuellen Design vertraut zu gestalten, auf den jeder Anbieter sicherlich einen eindeutigen Einblick hat, aber um einige Bereiche aufzurufen, die in eine erstklassige Microsoft Design-Umgebung für Windows 8 investiert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="eb808-107">**Objective:** The goal of the sample is not to be prescriptive about the layout or visual design that each provider will certainly have a unique point of view on, but to call out a few areas worth investing in to have a first-class Microsoft design style experience for Windows 8.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eb808-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="eb808-108">Prerequisites</span></span>

<span data-ttu-id="eb808-109">Um Web Authentication Broker-APIs verwenden zu können, benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="eb808-109">In order to use web authentication broker APIs, you need:</span></span>

-   <span data-ttu-id="eb808-110">Windows 8 (nur x86 oder amd64)</span><span class="sxs-lookup"><span data-stu-id="eb808-110">Windows 8 (x86 or amd64 only)</span></span>
-   <span data-ttu-id="eb808-111">Microsoft Internetinformationsdienste (IIS) sollte in der Systemsteuerung unter "Programme und Funktionen" installiert werden und die Option "Windows-Funktionen ein-oder ausschalten" verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb808-111">Microsoft Internet Information Services (IIS) should be installed from the Control Panel under "Programs and Features" and using the "Turn Windows features on or off" option.</span></span>

<span data-ttu-id="eb808-112">**Gesamtzeit bis zum Abschluss:** 2 Minuten.</span><span class="sxs-lookup"><span data-stu-id="eb808-112">**Total time to complete:** 2 minutes.</span></span>

## <a name="where-to-go-from-here"></a><span data-ttu-id="eb808-113">Weiterführende Informationen</span><span class="sxs-lookup"><span data-stu-id="eb808-113">Where to go from here</span></span>

<span data-ttu-id="eb808-114">Nächste [Authentifizierung für Webseiten](authentication-for-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="eb808-114">Next [Authentication for web pages](authentication-for-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb808-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eb808-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb808-116">Überlegungen für die Webseitenentwicklung</span><span class="sxs-lookup"><span data-stu-id="eb808-116">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="eb808-117">Beispiel-App für das Web Authentication Broker SDK</span><span class="sxs-lookup"><span data-stu-id="eb808-117">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="eb808-118">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="eb808-118">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
