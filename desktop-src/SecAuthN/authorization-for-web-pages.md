---
description: Die Autorisierung legt fest, auf welche Ressourcen Sie Zugriff haben.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Autorisierung für Webseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c26e9bc8333d74d18989c5c581cc54054a29ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863535"
---
# <a name="authorization-for-web-pages"></a><span data-ttu-id="535f1-103">Autorisierung für Webseiten</span><span class="sxs-lookup"><span data-stu-id="535f1-103">Authorization for web pages</span></span>

<span data-ttu-id="535f1-104">Die Autorisierung legt fest, auf welche Ressourcen Sie Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="535f1-104">Authorization sets what resources you have access to.</span></span>

<span data-ttu-id="535f1-105">**Ziel:** , Um Benutzern den Zugriff auf Ihre APP zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="535f1-105">**Objective:** To allow users access to your app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="535f1-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="535f1-106">Prerequisites</span></span>

<span data-ttu-id="535f1-107">Keine</span><span class="sxs-lookup"><span data-stu-id="535f1-107">None</span></span>

<span data-ttu-id="535f1-108">**Zeit bis zum Abschluss:** 2 Minuten.</span><span class="sxs-lookup"><span data-stu-id="535f1-108">**Time to complete:** 2 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="535f1-109">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="535f1-109">Instructions</span></span>

### <a name="1-authorization"></a><span data-ttu-id="535f1-110">1. Autorisierung</span><span class="sxs-lookup"><span data-stu-id="535f1-110">1. Authorization</span></span>

<span data-ttu-id="535f1-111">Wenn der Benutzer seine Anmelde Informationen eingibt und auf die Anmelde Schaltfläche klickt, wird die Seite Berechtigungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="535f1-111">When the user enters their credentials and clicks the Login button, the permissions page is shown.</span></span> <span data-ttu-id="535f1-112">Diese Seite ermöglicht es Benutzern, differenzierte Berechtigungen zu steuern, um der APP den Zugriff auf die Daten von "appto" zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="535f1-112">This page is best at allowing users to control granular permissions in granting the app to access to Contoso’s data.</span></span> ![Seite "Berechtigungen" für "Seite"](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a><span data-ttu-id="535f1-114">2. Verwenden des Beispiels</span><span class="sxs-lookup"><span data-stu-id="535f1-114">2. How to use the sample</span></span>

<span data-ttu-id="535f1-115">Sie müssen sich über die folgenden HTML-und CSS-Dateien informieren.</span><span class="sxs-lookup"><span data-stu-id="535f1-115">You need to know about the following HTML and CSS files.</span></span>

1.  <span data-ttu-id="535f1-116">Die folgenden HTML-Dateien entsprechen den beiden Seiten im webautorisierungs Fluss.</span><span class="sxs-lookup"><span data-stu-id="535f1-116">The following HTML files correspond to the two pages in the web authorization flow</span></span>
    -   <span data-ttu-id="535f1-117">WebAuthLogin.html – Beispiel-HTML für die Anmeldeseite</span><span class="sxs-lookup"><span data-stu-id="535f1-117">WebAuthLogin.html – sample HTML for the login page</span></span>
    -   <span data-ttu-id="535f1-118">WebAuthPermissions.html – Beispiel-HTML für die Seite "Berechtigungen"</span><span class="sxs-lookup"><span data-stu-id="535f1-118">WebAuthPermissions.html – sample HTML for the permissions page</span></span>
2.  <span data-ttu-id="535f1-119">Die CSS-Dateien enthalten Windows 8-Stile zum Erstellen einer Windows Store-App-Webseite.</span><span class="sxs-lookup"><span data-stu-id="535f1-119">The CSS files contain Windows 8 styles to help create a Windows Store app web page.</span></span>
    -   <span data-ttu-id="535f1-120">"UI-Light. CSS – dies wurde aus dem Basis Stylesheet für Windows 8-Steuerelemente abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="535f1-120">ui-light.css – this has been derived from the base style sheet for Windows 8 controls.</span></span>
    -   <span data-ttu-id="535f1-121">UI-webauth. CSS – diese Methode bietet inkrementelles formatieren zum Optimieren des Layouts für Webauthentifizierungs Seiten.</span><span class="sxs-lookup"><span data-stu-id="535f1-121">ui-webauth.css – this provides incremental styling for optimizing layout for web auth pages.</span></span>
    -   <span data-ttu-id="535f1-122">Theme-Colors. CSS – bietet das inkrementelle formatieren zum Überschreiben der Standard Akzentfarben von Steuerelementen mit der Markenfarbe des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="535f1-122">theme-colors.css – this provides the incremental styling to override default accent colors of controls with the provider’s brand color.</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="535f1-123">Zusammenfassung und nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="535f1-123">Summary and next steps</span></span>

<span data-ttu-id="535f1-124">Zusammenfassungs- [Tutorial zum Authentifizieren von Webseiten](tutorial-for-authenticating-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="535f1-124">Summary [Tutorial for authenticating web pages](tutorial-for-authenticating-web-pages.md)</span></span>

<span data-ttu-id="535f1-125">Nächste [bewährte Methoden für das Entwerfen von Authentifizierungs Webseiten](best-practices-for-designing-authentication-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="535f1-125">Next [Best practices for designing authentication web pages](best-practices-for-designing-authentication-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="535f1-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="535f1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="535f1-127">Überlegungen für die Webseitenentwicklung</span><span class="sxs-lookup"><span data-stu-id="535f1-127">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="535f1-128">Beispiel-App für das Web Authentication Broker SDK</span><span class="sxs-lookup"><span data-stu-id="535f1-128">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="535f1-129">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="535f1-129">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
