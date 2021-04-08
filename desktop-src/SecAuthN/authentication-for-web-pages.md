---
description: Authentifizierung gibt an, wer Sie sind.
ms.assetid: 5B058197-67B3-40DD-80D8-7BD8EE084CC9
title: Authentifizierung für Webseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7c7bd37334f345ae16074c050b6b06c5fd644f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960390"
---
# <a name="authentication-for-web-pages"></a><span data-ttu-id="399ed-103">Authentifizierung für Webseiten</span><span class="sxs-lookup"><span data-stu-id="399ed-103">Authentication for web pages</span></span>

<span data-ttu-id="399ed-104">Authentifizierung gibt an, wer Sie sind.</span><span class="sxs-lookup"><span data-stu-id="399ed-104">Authentication is proving who you are.</span></span>

<span data-ttu-id="399ed-105">**Ziel:** , Damit der Webauthentifizierungs Broker als Teil ihrer App angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="399ed-105">**Objective:** To have the web authentication broker appear as part of your app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="399ed-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="399ed-106">Prerequisites</span></span>

<span data-ttu-id="399ed-107">Keine</span><span class="sxs-lookup"><span data-stu-id="399ed-107">None</span></span>

<span data-ttu-id="399ed-108">**Zeit bis zum Abschluss:** 15 Minuten.</span><span class="sxs-lookup"><span data-stu-id="399ed-108">**Time to complete:** 15 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="399ed-109">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="399ed-109">Instructions</span></span>

### <a name="1-getting-started"></a><span data-ttu-id="399ed-110">1. Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="399ed-110">1. Getting started</span></span>

<span data-ttu-id="399ed-111">Starten Sie die Setup Datei, um eine Website von "Configuration Manager" in Internetinformationsdienste 8 auf dem lokalen Computer zu installieren und die HTML-und CSS-Beispieldateien zu hosten.</span><span class="sxs-lookup"><span data-stu-id="399ed-111">Launch the setup file to install a Contoso website in Internet Information Services 8 on the local machine to host the sample HTML and CSS files.</span></span>

1.  <span data-ttu-id="399ed-112">HTML-und CSS-Beispieldateien werden im Verzeichnis "Programme" unter Microsoft Configuration Manager installiert \\ .</span><span class="sxs-lookup"><span data-stu-id="399ed-112">Sample HTML and CSS files will be installed to the program files directory under Microsoft\\Contoso.</span></span>
2.  <span data-ttu-id="399ed-113">Außerdem wird die Windows Store-App "Fabrikam Social" auf den Desktop entpackt.</span><span class="sxs-lookup"><span data-stu-id="399ed-113">In addition a "Fabrikam Social"Windows Store app will be unpackaged to the desktop.</span></span>

### <a name="2-getting-familiar"></a><span data-ttu-id="399ed-114">2. kennenlernen</span><span class="sxs-lookup"><span data-stu-id="399ed-114">2. Getting familiar</span></span>

<span data-ttu-id="399ed-115">Öffnen Sie die Projektmappendatei von Fabrikam Social Visual Studio 11 im Ordner "Fabrikam Social" auf dem Desktop, um ein Gefühl für das Aussehen der Beispielseiten im Web Authentication Broker zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="399ed-115">To get a feel for what the sample pages look like in the Web Authentication Broker, open the Fabrikam Social Visual Studio 11 solution file in the "Fabrikam Social" folder on the desktop.</span></span>

1.  <span data-ttu-id="399ed-116">Führen Sie die Anwendung aus, und öffnen Sie "starten", um die Beispielseiten im Webauthentifizierungs Broker anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="399ed-116">Run the application and hit "Launch" to bring up the sample pages in the Web Authentication Broker.</span></span>
2.  <span data-ttu-id="399ed-117">Die Größe der APP kann auf eine Seite geändert oder durch Freigeben einiger Daten für die Anwendung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="399ed-117">The app can be resized to one side or activated by sharing some data to the application.</span></span>

### <a name="3-authentication"></a><span data-ttu-id="399ed-118">3. Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="399ed-118">3. Authentication</span></span>

<span data-ttu-id="399ed-119">Wenn die Webauthentifizierungs-API von der zugrunde liegenden app aufgerufen wird, um eine Verbindung mit dem Anbieter "" zu erhalten, wird die Anmeldeseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="399ed-119">When the Web Auth API is invoked by the underlying app to connect to the provider, "Contoso Social", the login page is shown.</span></span> <span data-ttu-id="399ed-120">Diese Seite ist so konzipiert, dass Sie für eine schnelle und fließende Anmeldung am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="399ed-120">This page is designed to be best at a fast and fluid login experience.</span></span> <span data-ttu-id="399ed-121">Außerdem werden Einstiegspunkte für einige andere gängige Benutzeraktionen bereitgestellt, wie z. b. das Abrufen von Kenn Wort Details, das Registrieren für ein Konto und das Lesen von Anweisungen zum Datenschutz und zu den Bestimmungen, die im Browser abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="399ed-121">It also provides entry points to some other common user actions such as retrieving password details, signing up for an account, and reading statements on privacy and terms and conditions that are completed in the browser.</span></span> ![Anmeldeseite von "" von ""](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a><span data-ttu-id="399ed-123">Zusammenfassung und nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="399ed-123">Summary and next steps</span></span>

<span data-ttu-id="399ed-124">Zusammenfassungs- [Tutorial zum Authentifizieren von Webseiten](tutorial-for-authenticating-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="399ed-124">Summary [Tutorial for authenticating web pages](tutorial-for-authenticating-web-pages.md)</span></span>

<span data-ttu-id="399ed-125">Nächste [Autorisierung für Webseiten](authorization-for-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="399ed-125">Next [Authorization for web pages](authorization-for-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="399ed-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="399ed-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="399ed-127">Überlegungen für die Webseitenentwicklung</span><span class="sxs-lookup"><span data-stu-id="399ed-127">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="399ed-128">Beispiel-App für das Web Authentication Broker SDK</span><span class="sxs-lookup"><span data-stu-id="399ed-128">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="399ed-129">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="399ed-129">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
