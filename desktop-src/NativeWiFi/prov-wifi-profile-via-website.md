---
title: Bereitstellen eines WLAN-Profils über eine Website
description: Ermöglichen Sie Ihren Benutzern, ein Profil von einer Website herunterzuladen und bereitzustellen.
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: e34c83fbee100316256293e27eac96dae685c37d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949088"
---
# <a name="provision-a-wi-fi-profile-via-a-website"></a><span data-ttu-id="66270-103">Bereitstellen eines WLAN-Profils über eine Website</span><span class="sxs-lookup"><span data-stu-id="66270-103">Provision a Wi-Fi profile via a website</span></span>

<span data-ttu-id="66270-104">Der in diesem Thema beschriebene Workflow wurde in Windows 10, Version 2004, eingeführt.</span><span class="sxs-lookup"><span data-stu-id="66270-104">The workflow described in this topic was introduced in Windows 10, version 2004.</span></span> <span data-ttu-id="66270-105">In diesem Thema wird gezeigt, wie Sie eine Website so konfigurieren, dass ein Benutzer ein Profil für ein passpoint-Netzwerk (oder für ein normales Netzwerk) bereitstellen kann, bevor es in den Bereich der entsprechenden Wi-Fi Zugriffspunkte verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="66270-105">This topic shows how to configure a website so that a user can provision a profile for a Passpoint network (or for a normal network) prior to moving into range of the corresponding Wi-Fi access points.</span></span> <span data-ttu-id="66270-106">Ein Beispielszenario ist, dass ein Benutzer, der möglicherweise plant, einen Flughafen oder eine Konferenz zum ersten Mal zu besuchen und sich vorab vorbereiten möchte, indem er ein Profil zu Hause herunterlädt und bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="66270-106">An example scenario is that of a user who might be planning to visit an airport or a conference for the first time, and they want to prepare in advance by downloading and provisioning a profile at home.</span></span>

<span data-ttu-id="66270-107">Als Entwickler aktivieren Sie den Workflow, indem Sie ein XML-Profil bereitstellen und eine Website konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="66270-107">As a developer, you enable the workflow by providing an XML profile, and configuring a website.</span></span> <span data-ttu-id="66270-108">Ihre Benutzer können dann ein Wi-Fi Profil bereitstellen, indem Sie es über einen Webbrowser von Ihrer Website herunterladen.</span><span class="sxs-lookup"><span data-stu-id="66270-108">Your users can then provision a Wi-Fi profile by downloading it from your website via a web browser.</span></span> <span data-ttu-id="66270-109">Auf dem Gerät des Benutzers wird das Wi-Fi Profil mithilfe der URI-Aktivierung und der Windows- **Einstellungs** -App bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="66270-109">On the user's device, the Wi-Fi profile is then provisioned by using URI activation and the Windows **Settings** app.</span></span>

<span data-ttu-id="66270-110">Dieser Workflow ersetzt den Mechanismus in Internet Explorer für die Bereitstellung Wi-Fi Profile, die von Microsoft-spezifischen JavaScript-APIs abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="66270-110">This workflow supersedes the mechanism in Internet Explorer for provisioning Wi-Fi profiles, which relies on Microsoft-specific JavaScript APIs.</span></span> <span data-ttu-id="66270-111">Es wird erwartet, dass dieser neue Workflow mit allen wichtigen Browsern funktioniert.</span><span class="sxs-lookup"><span data-stu-id="66270-111">This new workflow is expected to work with all major browsers.</span></span>

## <a name="the-workflow-in-more-detail"></a><span data-ttu-id="66270-112">Der Workflow ist ausführlicher.</span><span class="sxs-lookup"><span data-stu-id="66270-112">The workflow in more detail</span></span>

<span data-ttu-id="66270-113">Sie können diesen Workflow über einen Hyperlink aktivieren, der als Argument den Download-URI des XML-Bereitstellungs Dokuments enthält.</span><span class="sxs-lookup"><span data-stu-id="66270-113">You can activate this workflow from a hyperlink that includes as an argument the download URI of the provisioning XML document.</span></span>

```xml
ms-settings:wifi-provisioning?uri={download_uri}
```

<span data-ttu-id="66270-114">Das folgende HTML-Markup enthält z. b. einen Link zum Installieren der Profile, die in einem hypothetischen Dokument gefunden werden `http://contoso.com/ProvisioningDoc.xml` .</span><span class="sxs-lookup"><span data-stu-id="66270-114">For example, the following HTML markup gives a link to install the profile(s) that are found in a hypothetical document `http://contoso.com/ProvisioningDoc.xml`.</span></span>

```html
<a href="ms-settings:wifi-provisioning?uri=http://contoso.com/ProvisioningDoc.xml">Install</a>
```

<span data-ttu-id="66270-115">Der XML-Code muss dem Bereitstellungs Schema entsprechen (siehe [Konto Bereitstellung](/windows-hardware/drivers/mobilebroadband/account-provisioning)).</span><span class="sxs-lookup"><span data-stu-id="66270-115">Your XML must adhere to the provisioning schema (see [Account provisioning](/windows-hardware/drivers/mobilebroadband/account-provisioning)).</span></span> <span data-ttu-id="66270-116">Der XML-Code muss auch ein oder mehrere [wlanprofile](./wlan-profileschema-wlanprofile-element.md)-   Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="66270-116">Your XML must also include one or more [WLANProfile](./wlan-profileschema-wlanprofile-element.md) elements.</span></span><span data-ttu-id="66270-117">Jedes Profil wird im Dialogfeld **Hinzufügen** angezeigt, das weiter unten beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="66270-117"> Each profile will be displayed in the **Add** dialog described next.</span></span>

<span data-ttu-id="66270-118">Wenn der Benutzer auf den HTML-Link klickt, wird der Installations Workflow in der App " **Einstellungen** " aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="66270-118">When the user clicks your HTML link, the installation workflow is invoked in the **Settings** app.</span></span> <span data-ttu-id="66270-119">Ihr Bereitstellungs-XML-Dokument wird von der App " **Einstellungen** " heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="66270-119">Your provisioning XML document is downloaded by the **Settings** app.</span></span> <span data-ttu-id="66270-120">Nach dem herunterladen werden Informationen zu den Profilen, der Signatur und dem Signatur Geber angezeigt (sofern das Dokument dem Schema folgt).</span><span class="sxs-lookup"><span data-stu-id="66270-120">Once it's downloaded, information about the profiles, signature, and signer are displayed (provided that the document adheres to the schema).</span></span>

![Die app "Einstellungen"](images/install-dialog.png)

<span data-ttu-id="66270-122">Die Schaltfläche **Hinzufügen** im Dialogfeld in der APP **Einstellungen** ist nur aktiviert, wenn die Bereitstellungs Datei signiert und vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="66270-122">The **Add** button in the dialog in the **Settings** app is enabled only if the provisioning file is signed and trusted.</span></span>

## <a name="in-your-web-page-determine-whether-this-workflow-is-supported"></a><span data-ttu-id="66270-123">Legen Sie auf der Webseite fest, ob dieser Workflow unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="66270-123">In your web page, determine whether this workflow is supported</span></span>

<span data-ttu-id="66270-124">Es gibt keine Möglichkeit in JavaScript, die genaue Buildversion von Windows zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="66270-124">There is no way in JavaScript to determine the exact build version of Windows.</span></span> <span data-ttu-id="66270-125">Wenn Ihr Benutzer jedoch den Microsoft Edge-Webbrowser verwendet, können Sie die Version von Edge ermitteln, indem Sie den Wert des-HTTP- `User-agent` Headers überprüfen.</span><span class="sxs-lookup"><span data-stu-id="66270-125">But if your user is using the Microsoft Edge web browser, then you can determine the version of Edge by inspecting the value of the `User-agent` HTTP header.</span></span> <span data-ttu-id="66270-126">Wenn die Version größer oder gleich ist `18.nnnnn` , wird der Workflow unterstützt.</span><span class="sxs-lookup"><span data-stu-id="66270-126">If the version is greater than or equal to `18.nnnnn`, then the workflow is supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66270-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="66270-127">Related topics</span></span>

* [<span data-ttu-id="66270-128">Konto Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="66270-128">Account provisioning</span></span>](/windows-hardware/drivers/mobilebroadband/account-provisioning)
* [<span data-ttu-id="66270-129">Wlanprofile-Element</span><span class="sxs-lookup"><span data-stu-id="66270-129">WLANProfile element</span></span>](./wlan-profileschema-wlanprofile-element.md)