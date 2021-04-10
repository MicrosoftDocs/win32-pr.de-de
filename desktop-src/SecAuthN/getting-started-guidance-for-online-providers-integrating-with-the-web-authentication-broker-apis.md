---
description: Richtlinien für Webentwickler und Online Anbieter zum Erstellen von Webseiten, die auf die Windows 8-Webauthentifizierungs Broker-APIs für Single Sign-on (SSO)-Funktionen zugeschnitten sind.
ms.assetid: E2AECE26-9649-41CB-9808-4F8171C707C3
title: Leitfaden zu den ersten Schritten für Online Anbieter, die in die Web Authentication Broker-APIs integrieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842f3c562d2ad288efaecec82f8da8ca771886a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867264"
---
# <a name="getting-started-guidance-for-online-providers-integrating-with-the-web-authentication-broker-apis"></a><span data-ttu-id="0fce4-103">Leitfaden zu den ersten Schritten für Online Anbieter, die in die Web Authentication Broker-APIs integrieren</span><span class="sxs-lookup"><span data-stu-id="0fce4-103">Getting started guidance for online providers integrating with the Web Authentication Broker APIs</span></span>

<span data-ttu-id="0fce4-104">In diesem Abschnitt wird erläutert, wie Webentwickler und Online Anbieter Webseiten erstellen, die auf die Windows 8-Webauthentifizierungs Broker-APIs zugeschnitten sind.</span><span class="sxs-lookup"><span data-stu-id="0fce4-104">This section guides web developers and online providers for creating web pages tailored for the Windows 8 Web Authentication Broker APIs.</span></span> <span data-ttu-id="0fce4-105">Es bietet die visuellen und interaktiven Empfehlungen für eine End-to-End-Benutzer Darstellung der Webseite sowie zum Aktivieren von Single Sign-on (SSO)-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="0fce4-105">It provides the visual and interactive recommendations for an end-to-end user experience of the web page as well as how to enable single sign-on (SSO) capabilities.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0fce4-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0fce4-106">In this section</span></span>



| <span data-ttu-id="0fce4-107">Thema</span><span class="sxs-lookup"><span data-stu-id="0fce4-107">Topic</span></span>                                                                                                     | <span data-ttu-id="0fce4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fce4-108">Description</span></span>                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0fce4-109">Überlegungen für die Webseitenentwicklung</span><span class="sxs-lookup"><span data-stu-id="0fce4-109">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)<br/> | <span data-ttu-id="0fce4-110">Der Webauthentifizierungs Broker basiert auf den gleichen Technologien wie Internet Explorer in Windows.</span><span class="sxs-lookup"><span data-stu-id="0fce4-110">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="0fce4-111">Aufgrund eines besonderen zwecks dieser Komponente wurden einige Features von Internet Explorer jedoch deaktiviert oder für eine bestimmte Konfiguration gesperrt.</span><span class="sxs-lookup"><span data-stu-id="0fce4-111">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <br/> |
| [<span data-ttu-id="0fce4-112">Anpassen der Benutzeroberflächenelemente</span><span class="sxs-lookup"><span data-stu-id="0fce4-112">How to customize the UI elements</span></span>](how-to-customize-the-ui-elements.md)<br/>                       | <span data-ttu-id="0fce4-113">Eine Webseite passt die Benutzeroberfläche (UI) mit dem Titel, dem Symbol und der Header Farbe an, indem Metadatentags verwendet werden, die auf der Webseite definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0fce4-113">A web page customizes the user interface (UI) with the title, icon, and header color by using metadata tags defined on the web page.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="0fce4-114">Tutorial zum Authentifizieren von Webseiten</span><span class="sxs-lookup"><span data-stu-id="0fce4-114">Tutorial for authenticating web pages</span></span>](tutorial-for-authenticating-web-pages.md)<br/>             |                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="0fce4-115">Webauthentifizierungsprobleme</span><span class="sxs-lookup"><span data-stu-id="0fce4-115">Web authentication problems</span></span>](web-authentication-problems.md)<br/>                                 | <span data-ttu-id="0fce4-116">In diesem Thema werden Tipps zur Problembehandlung für die Verwendung der Webauthentifizierungs Broker-APIs für Ihre Webseiten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0fce4-116">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="0fce4-117">Häufig gestellte Fragen zum Webauthentifizierungs Broker</span><span class="sxs-lookup"><span data-stu-id="0fce4-117">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)<br/>                     | <span data-ttu-id="0fce4-118">Häufig gestellte Fragen zum Webauthentifizierungs Broker.</span><span class="sxs-lookup"><span data-stu-id="0fce4-118">Frequently asked questions for Web Authentication Broker.</span></span><br/>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="0fce4-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0fce4-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0fce4-120">[Übersicht über den Webauthentifizierungs Broker](/previous-versions/windows/apps/hh750287(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="0fce4-120">[Web authentication broker overview](/previous-versions/windows/apps/hh750287(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="0fce4-121">Beispiel-App für das Web Authentication Broker SDK</span><span class="sxs-lookup"><span data-stu-id="0fce4-121">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="0fce4-122">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="0fce4-122">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

