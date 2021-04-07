---
title: Aufrufen von WDS von Webseiten
description: Sie können Microsoft Windows Desktop Search (WDS) von jeder beliebigen Webseite, die Sie erstellen oder verwalten, mit dem Browserhilfsobjekt (BHO) und Windows Internet Explorer abrufen.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e7ca8b529c8f69b1f36d44decfae44895e4ec
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "104038662"
---
# <a name="calling-wds-from-web-pages"></a><span data-ttu-id="6099c-103">Aufrufen von WDS von Webseiten</span><span class="sxs-lookup"><span data-stu-id="6099c-103">Calling WDS from Web Pages</span></span>

> [!NOTE]
> <span data-ttu-id="6099c-104">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="6099c-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="6099c-105">Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="6099c-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="6099c-106">Sie können Microsoft Windows Desktop Search (WDS) von jeder beliebigen Webseite, die Sie erstellen oder verwalten, mit dem Browserhilfsobjekt (BHO) und Windows Internet Explorer abrufen.</span><span class="sxs-lookup"><span data-stu-id="6099c-106">You can call Microsoft Windows Desktop Search (WDS) from any webpage you create or maintain using the Browser Helper Object (BHO) and Windows Internet Explorer.</span></span> <span data-ttu-id="6099c-107">Sie können sehen, wie dies auf der MSN-Webseite funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6099c-107">You can see how this works on the MSN webpage.</span></span> <span data-ttu-id="6099c-108">Über dem Suchfeld für https://www.msn.com gibt es mehrere Suchtypen: Web, News, Bilder, Desktop, Encarta und local.</span><span class="sxs-lookup"><span data-stu-id="6099c-108">Above the search box on https://www.msn.com are several search types: Web, News, Images, Desktop, Encarta, and Local.</span></span> <span data-ttu-id="6099c-109">Wenn Sie auf Desktop klicken, werden die Suchparameter an die Windows-Desktop Suche übermittelt, die den Katalog durchsucht und Ergebnisse in der WDS-Benutzeroberfläche anzeigt.</span><span class="sxs-lookup"><span data-stu-id="6099c-109">If you click Desktop, the search parameters are passed to Windows Desktop Search, which searches the catalog and displays results in the WDS user interface.</span></span> <span data-ttu-id="6099c-110">Damit Benutzer eine Desktop Suche von ihren Webseiten aus starten können, muss wdsbho auf Ihren Systemen installiert und aktiviert sein. Ihre Webseiten müssen als zulässige URL bei WDS registriert sein, und Sie müssen einen Link erstellen, um die vom Benutzer getaktete Abfrage an WDS zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="6099c-110">For users to start a desktop search from your webpage(s), the WDSBHO must be installed and enabled on their systems, your webpage(s) must be registered with WDS as an allowed URL, and you must create a link to pass the user-enetered query to WDS.</span></span>

## <a name="enabling-the-wds-browser-help-object"></a><span data-ttu-id="6099c-111">Aktivieren des Hilfe Objekts für den WDS-Browser</span><span class="sxs-lookup"><span data-stu-id="6099c-111">Enabling the WDS Browser Help Object</span></span>

<span data-ttu-id="6099c-112">Der BHO wird bei der Installation von WDS standardmäßig in Internet Explorer installiert und aktiviert, aber Sie können problemlos überprüfen, ob er deaktiviert oder deinstalliert wurde.</span><span class="sxs-lookup"><span data-stu-id="6099c-112">The BHO is installed and enabled within Internet Explorer by default when you install WDS, but you can easily verify that it hasn't been disabled or uninstalled.</span></span> <span data-ttu-id="6099c-113">Öffnen Sie im System eines Benutzers Internet Explorer, wählen Sie **im Menü Extras die** **Option Internetoptionen** aus, klicken Sie auf die Registerkarte **Programme** , und klicken Sie dann auf **Add-ons verwalten**.</span><span class="sxs-lookup"><span data-stu-id="6099c-113">On a user's system, open Internet Explorer , select **Internet Options** from the **Tools** menu, click the **Programs** tab, and then click **Manage Add-Ons**.</span></span> <span data-ttu-id="6099c-114">Suchen Sie in der Liste der Add-ons nach der Klasse dsweballowbho, und stellen Sie sicher, dass Sie aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6099c-114">In your list of add-ons, look for the dsWebAllowBHO Class and make sure it is enabled.</span></span> <span data-ttu-id="6099c-115">Wenn BHO deaktiviert ist, funktionieren die WDS weiterhin ordnungsgemäß. Es ist jedoch nicht möglich, den Desktop auf einer Webseite zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="6099c-115">When the BHO is disabled, WDS will continue to work normally; however, you will not be able to search the desktop from a webpage.</span></span>

<span data-ttu-id="6099c-116">Bei beiden der folgenden Optionen zum Zulassen einer Desktop Suche wird die Suche lokal mit der registrierten Suchanwendung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6099c-116">Both of the following options for allowing a desktop search will execute the search locally with the registered search application.</span></span>

## <a name="registering-web-page-urls"></a><span data-ttu-id="6099c-117">Registrieren von Webseiten-URLs</span><span class="sxs-lookup"><span data-stu-id="6099c-117">Registering Web Page URLs</span></span>

<span data-ttu-id="6099c-118">Die Registrierung enthält eine Liste der "zulässigen" Domänen-URLs, von denen WDS aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6099c-118">The Registry includes a list of "allowed" domain URLs from which WDS can be called.</span></span> <span data-ttu-id="6099c-119">Wenn Sie Ihre Webseiten einschließen möchten, müssen Sie Ihre Domänen-URL (s) als reg \_ SZ in der Registrierung wie folgt auflisten:</span><span class="sxs-lookup"><span data-stu-id="6099c-119">To include your webpage(s), you need to list your domain URL(s) as REG\_SZ in the Registry as follows:</span></span>

<span data-ttu-id="6099c-120">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows-Desktop Suche** \\ **DSW** \\ **zulässig**\\*<number>* = <domainURL></span><span class="sxs-lookup"><span data-stu-id="6099c-120">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows Desktop Search**\\**DSW**\\**Allowed**\\*<number>* = <domainURL></span></span>

<span data-ttu-id="6099c-121">Dabei **<number>** ist sequenziell nummeriert, und **<domainURL>** ist die URL der Webseite, von der Sie WDS suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="6099c-121">Where **<number>** is sequentially numbered, and **<domainURL>** is the URL of the Web Page you want to allow WDS searches from.</span></span> <span data-ttu-id="6099c-122">Diese URL-Zeichenfolge kann das Platzhalter Sternchen \* am Anfang oder Ende der URL enthalten.</span><span class="sxs-lookup"><span data-stu-id="6099c-122">This URL string can include the wildcard asterisk \* at the beginning or end of the URL.</span></span> <span data-ttu-id="6099c-123">Wenn die Zeichenfolge z \* . b. ". mydomain.com" lautet, können Sie eine WDS-Suche sowohl von https://www.mydomain.com als auch von Starten https://mydomain.com .</span><span class="sxs-lookup"><span data-stu-id="6099c-123">For example, if the string is "\*.mydomain.com", then you can start a WDS search from both https://www.mydomain.com and https://mydomain.com.</span></span>

## <a name="enabling-desktop-search-by-url"></a><span data-ttu-id="6099c-124">Aktivieren der Desktop Suche per URL</span><span class="sxs-lookup"><span data-stu-id="6099c-124">Enabling Desktop Search by URL</span></span>

<span data-ttu-id="6099c-125">Eine weitere Option, die keinen Zugriff auf die Registrierung erfordert, ist die Verwendung der folgenden URL auf Ihren Webseiten:</span><span class="sxs-lookup"><span data-stu-id="6099c-125">Another option that does not require access to the Registry is to use the following URL on your webpage(s):</span></span>

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

<span data-ttu-id="6099c-126">Where **Query** ist die URL-codierte Zeichenfolge, nach der der Benutzer sucht, einschließlich der [erweiterten Abfrage Syntax](-search-2x-wds-aqsreference.md) Begriffe.</span><span class="sxs-lookup"><span data-stu-id="6099c-126">where **QUERY** is the URL-encoded string the user is searching on, including any [Advanced Query Syntax](-search-2x-wds-aqsreference.md) terms.</span></span>

 

 




