---
description: Richtlinien für Webentwickler und Onlineanbieter zum Erstellen von Webseiten, die auf die Windows 8 Web Authentication Broker-APIs für SSO-Funktionen (Single Sign-On, einmaliges Anmelden) zugeschnitten sind.
ms.assetid: E2AECE26-9649-41CB-9808-4F8171C707C3
title: Leitfaden zu den ersten Schritte für Onlineanbieter, die in die Webauthentifizierungsbroker-APIs integriert sind
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bf0ce59cd92e32264823861aaef44e90b4f2c0
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353633"
---
# <a name="getting-started-guidance-for-online-providers-integrating-with-the-web-authentication-broker-apis"></a><span data-ttu-id="1602f-103">Leitfaden zu den ersten Schritte für Onlineanbieter, die in die Webauthentifizierungsbroker-APIs integriert sind</span><span class="sxs-lookup"><span data-stu-id="1602f-103">Getting started guidance for online providers integrating with the Web Authentication Broker APIs</span></span>

<span data-ttu-id="1602f-104">In diesem Abschnitt werden Webentwickler und Onlineanbieter beim Erstellen von Webseiten geführt, die auf die Windows 8 Web Authentication Broker-APIs zugeschnitten sind.</span><span class="sxs-lookup"><span data-stu-id="1602f-104">This section guides web developers and online providers for creating web pages tailored for the Windows 8 Web Authentication Broker APIs.</span></span> <span data-ttu-id="1602f-105">Es bietet die visuellen und interaktiven Empfehlungen für eine End-to-End-Benutzererfahrung der Webseite sowie informationen zum Aktivieren von SSO-Funktionen (Single Sign-On, einmaliges Anmelden).</span><span class="sxs-lookup"><span data-stu-id="1602f-105">It provides the visual and interactive recommendations for an end-to-end user experience of the web page as well as how to enable single sign-on (SSO) capabilities.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1602f-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="1602f-106">In this section</span></span>



| <span data-ttu-id="1602f-107">Thema</span><span class="sxs-lookup"><span data-stu-id="1602f-107">Topic</span></span>                                                                                                     | <span data-ttu-id="1602f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1602f-108">Description</span></span>                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1602f-109">Überlegungen für die Webseitenentwicklung</span><span class="sxs-lookup"><span data-stu-id="1602f-109">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)<br/> | <span data-ttu-id="1602f-110">Der Webauthentifizierungsbroker basiert auf denselben Technologien, die Internet Explorer in Windows unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1602f-110">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="1602f-111">Aufgrund eines sehr speziellen Zwecks dieser Komponente wurden einige Features der Internet Explorer jedoch deaktiviert oder für eine bestimmte Konfiguration gesperrt.</span><span class="sxs-lookup"><span data-stu-id="1602f-111">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <br/> |
| [<span data-ttu-id="1602f-112">Anpassen der Benutzeroberflächenelemente</span><span class="sxs-lookup"><span data-stu-id="1602f-112">How to customize the UI elements</span></span>](how-to-customize-the-ui-elements.md)<br/>                       | <span data-ttu-id="1602f-113">Eine Webseite passt die Benutzeroberfläche mit Titel, Symbol und Headerfarbe an, indem auf der Webseite definierte Metadatentags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1602f-113">A web page customizes the user interface (UI) with the title, icon, and header color by using metadata tags defined on the web page.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="1602f-114">Tutorial zum Authentifizieren von Webseiten</span><span class="sxs-lookup"><span data-stu-id="1602f-114">Tutorial for authenticating web pages</span></span>](tutorial-for-authenticating-web-pages.md)<br/>             |                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="1602f-115">Webauthentifizierungsprobleme</span><span class="sxs-lookup"><span data-stu-id="1602f-115">Web authentication problems</span></span>](web-authentication-problems.md)<br/>                                 | <span data-ttu-id="1602f-116">In diesem Thema werden Tipps zur Problembehandlung für die Verwendung der Webauthentifizierungsbroker-APIs für Ihre Webseiten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1602f-116">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="1602f-117">Häufig gestellte Fragen zum Webauthentifizierungsbroker</span><span class="sxs-lookup"><span data-stu-id="1602f-117">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.yml)<br/>                     | <span data-ttu-id="1602f-118">Häufig gestellte Fragen zum Webauthentifizierungsbroker.</span><span class="sxs-lookup"><span data-stu-id="1602f-118">Frequently asked questions for Web Authentication Broker.</span></span><br/>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="1602f-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1602f-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1602f-120">[Webauthentifizierungsbroker – Übersicht](/previous-versions/windows/apps/hh750287(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="1602f-120">[Web authentication broker overview](/previous-versions/windows/apps/hh750287(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="1602f-121">Webauthentifizierungsbroker-SDK-Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="1602f-121">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="1602f-122">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="1602f-122">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

