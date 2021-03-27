---
description: In dieser Schnellstartanleitung wird veranschaulicht, wie eine Popup Benachrichtigung aus einer Desktop-App erhoben wird.
title: Senden einer Popupbenachrichtigung vom Desktop
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 36f9da25c20d99da74be30046fc5f9f4789dfd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866148"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a><span data-ttu-id="d28bb-103">Schnellstart: Senden einer Popup Benachrichtigung vom Desktop</span><span class="sxs-lookup"><span data-stu-id="d28bb-103">Quickstart: Sending a toast notification from the desktop</span></span>

<span data-ttu-id="d28bb-104">In dieser Schnellstartanleitung wird veranschaulicht, wie eine Popup Benachrichtigung aus einer Desktop-App erhoben wird.</span><span class="sxs-lookup"><span data-stu-id="d28bb-104">This quickstart shows how to raise a toast notification from a desktop app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d28bb-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d28bb-105">Prerequisites</span></span>

-   <span data-ttu-id="d28bb-106">Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="d28bb-106">Libraries</span></span>
    -   <span data-ttu-id="d28bb-107">C++: Runtime. Object. lib</span><span class="sxs-lookup"><span data-stu-id="d28bb-107">C++: Runtime.object.lib</span></span>
    -   <span data-ttu-id="d28bb-108">C \# : Windows. winmd</span><span class="sxs-lookup"><span data-stu-id="d28bb-108">C\#: Windows.Winmd</span></span>
-   <span data-ttu-id="d28bb-109">Auf dem Start Bildschirm muss eine Verknüpfung mit der APP mit [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md)installiert sein.</span><span class="sxs-lookup"><span data-stu-id="d28bb-109">A shortcut to your app, with a [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), must be installed to the Start screen.</span></span> <span data-ttu-id="d28bb-110">Beachten Sie jedoch, dass es nicht an den Start Bildschirm angeheftet werden muss.</span><span class="sxs-lookup"><span data-stu-id="d28bb-110">Note, however, that it does not need to be pinned to the Start screen.</span></span> <span data-ttu-id="d28bb-111">Weitere Informationen finden Sie unter Aktivieren von desktoppopup [-Benachrichtigungen über eine appusermodelid](enable-desktop-toast-with-appusermodelid.md).</span><span class="sxs-lookup"><span data-stu-id="d28bb-111">For more information, see [How to enable desktop toast notifications through an AppUserModelID](enable-desktop-toast-with-appusermodelid.md).</span></span>
-   <span data-ttu-id="d28bb-112">Eine Version von Microsoft Visual Studio, die mindestens Windows 8 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d28bb-112">A version of Microsoft Visual Studio that supports at least Windows 8</span></span>

## <a name="instructions"></a><span data-ttu-id="d28bb-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="d28bb-113">Instructions</span></span>

### <a name="1-create-your-toast-content"></a><span data-ttu-id="d28bb-114">1. Erstellen Sie den Popup Inhalt.</span><span class="sxs-lookup"><span data-stu-id="d28bb-114">1. Create your toast content</span></span>

> [!Note]  
> <span data-ttu-id="d28bb-115">Beachten Sie, dass Desktop-Apps nur lokale Images verwenden können, wenn Sie eine Popup Vorlage angeben, die ein Bild enthält. webimages werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d28bb-115">When you specify a toast template that includes an image, be aware that desktop apps can use only local images; web images are not supported.</span></span> <span data-ttu-id="d28bb-116">Außerdem muss der Pfad zur lokalen Bilddatei als absoluter (nicht relativer) Pfad angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d28bb-116">Also, the path to the local image file must be provided as an absolute (not relative) path.</span></span>

 


```csharp
// Get a toast XML template
XmlDocument toastXml = ToastNotificationManager.GetTemplateContent(ToastTemplateType.ToastImageAndText04);

// Fill in the text elements
XmlNodeList stringElements = toastXml.GetElementsByTagName("text");
for (int i = 0; i < stringElements.Length; i++)
{
    stringElements[i].AppendChild(toastXml.CreateTextNode("Line " + i));
}

// Specify the absolute path to an image
String imagePath = "file:///" + Path.GetFullPath("toastImageAndText.png");
XmlNodeList imageElements = toastXml.GetElementsByTagName("image");

ToastNotification toast = new ToastNotification(toastXml);
```



### <a name="2-create-and-attach-the-event-handlers"></a><span data-ttu-id="d28bb-117">2. erstellen und Anfügen von Ereignis Handlern</span><span class="sxs-lookup"><span data-stu-id="d28bb-117">2. Create and attach the event handlers</span></span>

<span data-ttu-id="d28bb-118">Registrieren von Handlern für die Popup Ereignisse: aktiviert, verworfen und fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="d28bb-118">Register handlers for the toast events: Activated, Dismissed, and Failed.</span></span> <span data-ttu-id="d28bb-119">Eine Desktop-App muss das aktivierte Ereignis zumindest abonnieren, damit Sie die erwartete Aktivierung der APP vom Toast aus verarbeiten kann, wenn der Benutzer Sie auswählt.</span><span class="sxs-lookup"><span data-stu-id="d28bb-119">A desktop app must at least subscribe to the Activated event so that it can handle the expected activation of the app from the toast when the user selects it.</span></span>


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a><span data-ttu-id="d28bb-120">3. den Toast senden</span><span class="sxs-lookup"><span data-stu-id="d28bb-120">3. Send the toast</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d28bb-121">Sie müssen die [appusermodelid](../properties/props-system-appusermodel-id.md) der Verknüpfung ihrer App auf dem Start Bildschirm jedes Mal einschließen, wenn Sie " [**foratetoastnotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d28bb-121">You must include the [AppUserModelID](../properties/props-system-appusermodel-id.md) of your app's shortcut on the Start screen each time that you call [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041).</span></span> <span data-ttu-id="d28bb-122">Wenn Sie dies nicht tun, wird der Toast nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d28bb-122">If you fail to do this, your toast will not be displayed.</span></span>

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a><span data-ttu-id="d28bb-123">4. behandeln Sie die Rückrufe.</span><span class="sxs-lookup"><span data-stu-id="d28bb-123">4. Handle the callbacks</span></span>

<span data-ttu-id="d28bb-124">Bringen Sie das Fenster ihrer app in den Vordergrund, wenn ein "aktivierter" Rückruf von der Popup Benachrichtigung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="d28bb-124">Bring your app's window to the foreground if it receives an "activated" callback from the toast notification.</span></span> <span data-ttu-id="d28bb-125">Wenn ein Benutzer einen Toast auswählt, wird erwartet, dass die app in einer Ansicht mit dem Inhalt dieses Popups gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d28bb-125">When a user selects a toast, the expectation is that the app will be launched to a view related to the content of that toast..</span></span>

## <a name="related-topics"></a><span data-ttu-id="d28bb-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d28bb-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d28bb-127">Beispiel zum Senden von Toastbenachrichtigungen aus Desktop-Apps</span><span class="sxs-lookup"><span data-stu-id="d28bb-127">Sending toast notifications from desktop apps sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[<span data-ttu-id="d28bb-128">Aktivieren von Desktoppopupbenachrichtigungen über eine AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="d28bb-128">How to enable desktop toast notifications through an AppUserModelID</span></span>](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[<span data-ttu-id="d28bb-129">Popup-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="d28bb-129">Toast XML schema</span></span>](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

<span data-ttu-id="d28bb-130">[Übersicht über Popup Benachrichtigungen](/previous-versions/windows/apps/hh779727(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d28bb-130">[Toast notification overview](/previous-versions/windows/apps/hh779727(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="d28bb-131">[Schnellstart: Senden einer Popup Benachrichtigung](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d28bb-131">[Quickstart: Sending a toast notification](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="d28bb-132">[Schnellstart: Senden einer Popup-Pushbenachrichtigung](/previous-versions/windows/hh761487(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d28bb-132">[Quickstart: Sending a toast push notification](/previous-versions/windows/hh761487(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="d28bb-133">Richtlinien und Prüfliste für Popup Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="d28bb-133">Guidelines and checklist for toast notifications</span></span>](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

<span data-ttu-id="d28bb-134">[Auswählen und Verwenden einer Popup Vorlage](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d28bb-134">[How to choose and use a toast template](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="d28bb-135">[Behandeln der Aktivierung über eine Popup Benachrichtigung](/previous-versions/windows/apps/hh761468(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d28bb-135">[How to handle activation from a toast notification](/previous-versions/windows/apps/hh761468(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="d28bb-136">[Abonnieren von Popup Benachrichtigungen](/previous-versions/windows/apps/hh781238(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d28bb-136">[How to opt in for toast notifications](/previous-versions/windows/apps/hh781238(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="d28bb-137">[Auswählen einer Popup Vorlage](/previous-versions/windows/apps/hh761494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d28bb-137">[Choosing a toast template](/previous-versions/windows/apps/hh761494(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="d28bb-138">[Popup-Audiooptionen](/previous-versions/windows/apps/hh761492(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d28bb-138">[Toast audio options](/previous-versions/windows/apps/hh761492(v=win.10))</span></span>
</dt> </dl>

 

 
