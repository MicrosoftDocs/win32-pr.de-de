---
description: Veranschaulicht, wie die Shell \_ NotifyIcon-und Shell \_ notifyikongetrect-APIs zum Anzeigen eines Benachrichtigungs Symbols verwendet werden.
title: NotificationIcon (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9F31DB2D-4B12-4f65-AC91-25B4B5B1CB46
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1569d162aef358130910081bee80354cb64f690d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979833"
---
# <a name="notificationicon-sample"></a><span data-ttu-id="dd3ac-103">NotificationIcon (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="dd3ac-103">NotificationIcon Sample</span></span>

<span data-ttu-id="dd3ac-104">Veranschaulicht, wie die [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) -und [**Shell \_ notifyikongetrect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) -APIs zum Anzeigen eines Benachrichtigungs Symbols verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd3ac-104">Demonstrates how to use the [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) and [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) APIs to display a notification icon.</span></span>

<span data-ttu-id="dd3ac-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="dd3ac-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="dd3ac-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd3ac-106">Description</span></span>](#description)
-   [<span data-ttu-id="dd3ac-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd3ac-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="dd3ac-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="dd3ac-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="dd3ac-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="dd3ac-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="dd3ac-110">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="dd3ac-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="dd3ac-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd3ac-111">Description</span></span>

<span data-ttu-id="dd3ac-112">Zusätzlich zur Verwendung von [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) und [**Shell \_ notifyikongetrect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) zum Anzeigen eines Benachrichtigungs Symbols wird in diesem Beispiel auch veranschaulicht, wie Sie ein umfangreiches Flyout-Fenster, ein Kontextmenü und eine Sprechblasen Benachrichtigung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="dd3ac-112">In addition to the use of [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) and [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) to display a notification icon, this sample also demonstrates how to display a rich flyout window, context menu, and balloon notification.</span></span>

> [!Note]  
> <span data-ttu-id="dd3ac-113">[**Shell \_ Notisyitrect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) ist nur unter Windows 7 und höheren Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dd3ac-113">[**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) is only available on Windows 7 and later versions.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dd3ac-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="dd3ac-114">Requirements</span></span>



| <span data-ttu-id="dd3ac-115">Produkt</span><span class="sxs-lookup"><span data-stu-id="dd3ac-115">Product</span></span>                                | <span data-ttu-id="dd3ac-116">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="dd3ac-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="dd3ac-117">Windows</span><span class="sxs-lookup"><span data-stu-id="dd3ac-117">Windows</span></span>                                | <span data-ttu-id="dd3ac-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dd3ac-118">Windows 7</span></span>               |
| <span data-ttu-id="dd3ac-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="dd3ac-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="dd3ac-120">7.0</span><span class="sxs-lookup"><span data-stu-id="dd3ac-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="dd3ac-121">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="dd3ac-121">Downloading the Sample</span></span>

| <span data-ttu-id="dd3ac-122">Standort</span><span class="sxs-lookup"><span data-stu-id="dd3ac-122">Location</span></span>      | <span data-ttu-id="dd3ac-123">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="dd3ac-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd3ac-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="dd3ac-124">GitHub</span></span>  | [<span data-ttu-id="dd3ac-125">Notificationicon-Beispiel</span><span class="sxs-lookup"><span data-stu-id="dd3ac-125">NotificationIcon sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NotificationIcon) |

## <a name="building-the-sample"></a><span data-ttu-id="dd3ac-126">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="dd3ac-126">Building the Sample</span></span>

<span data-ttu-id="dd3ac-127">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="dd3ac-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="dd3ac-128">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **notificationicon** .</span><span class="sxs-lookup"><span data-stu-id="dd3ac-128">Open the command prompt window and navigate to the **NotificationIcon** project directory.</span></span>
2.  <span data-ttu-id="dd3ac-129">Geben Sie `msbuild NotificationIcon.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="dd3ac-129">Enter `msbuild NotificationIcon.sln`.</span></span>

<span data-ttu-id="dd3ac-130">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="dd3ac-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="dd3ac-131">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **notificationicon** .</span><span class="sxs-lookup"><span data-stu-id="dd3ac-131">Open Windows Explorer and navigate to the **NotificationIcon** project directory.</span></span>
2.  <span data-ttu-id="dd3ac-132">Doppelklicken Sie auf das Symbol für die Datei notificationicon. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dd3ac-132">Double-click the icon for the NotificationIcon.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="dd3ac-133">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="dd3ac-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="dd3ac-134">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="dd3ac-134">Running the Sample</span></span>

1.  <span data-ttu-id="dd3ac-135">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="dd3ac-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="dd3ac-136">Geben Sie in der Befehlszeile ein `NotificationIcon.exe` .</span><span class="sxs-lookup"><span data-stu-id="dd3ac-136">At the command line, enter `NotificationIcon.exe`.</span></span> <span data-ttu-id="dd3ac-137">Alternativ können Sie in Windows-Explorer auf das Symbol für NotificationIcon.exe doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="dd3ac-137">Alternatively, from Windows Explorer double-click the icon for NotificationIcon.exe.</span></span>

> [!Note]  
> <span data-ttu-id="dd3ac-138">Benachrichtigungs Symbole, die mit einer GUID angegeben werden, werden vor Spoofing geschützt, indem überprüft wird, ob Sie nur von einer einzelnen Anwendung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="dd3ac-138">Notification icons specified with a GUID are protected against spoofing by validating that only a single application registers them.</span></span> <span data-ttu-id="dd3ac-139">Diese Registrierung wird ausgeführt, wenn Sie Shell \_ NotifyIcon (NIM \_ Add,...) zum ersten Mal aufrufen und der vollständige Pfadname der aufrufenden Anwendung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="dd3ac-139">This registration is performed the first time you call Shell\_NotifyIcon(NIM\_ADD, ...) and the full path name of the calling application is stored.</span></span> <span data-ttu-id="dd3ac-140">Wenn Sie die Binärdatei später an einen anderen Speicherort verschieben, lässt das System nicht zu, dass das Symbol erneut hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="dd3ac-140">If you later move your binary file to a different location, the system will not allow the icon to be added again.</span></span> <span data-ttu-id="dd3ac-141">Weitere Informationen finden Sie in der [**Shell \_ notityicon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) .</span><span class="sxs-lookup"><span data-stu-id="dd3ac-141">Please see [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) for more information.</span></span>

 

 

 



