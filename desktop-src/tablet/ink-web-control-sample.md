---
description: In diesem Beispiel wird gezeigt, wie ein frei Hand fähiges Steuerelement für die Verwendung in einem Webbrowser erstellt wird. Im Beispiel wird das ursprüngliche Formular Beispiel für automatische Ansprüche übernommen und in ein Steuerelement umgewandelt, das auf einer Webseite abgelegt ist.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Ink-websteuer Element-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101537c4cc7b42181cf8d9ff177a5854c5b84054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353059"
---
# <a name="ink-web-control-sample"></a><span data-ttu-id="401a3-104">Ink-websteuer Element-Beispiel</span><span class="sxs-lookup"><span data-stu-id="401a3-104">Ink Web Control Sample</span></span>

<span data-ttu-id="401a3-105">In diesem Beispiel wird gezeigt, wie ein frei Hand fähiges Steuerelement für die Verwendung in einem Webbrowser erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="401a3-105">This sample shows how to create an ink-enabled control for use in a Web browser.</span></span> <span data-ttu-id="401a3-106">Im Beispiel wird das ursprüngliche [Formular Beispiel für automatische Ansprüche](auto-claims-form-sample.md) übernommen und in ein Steuerelement umgewandelt, das auf einer Webseite abgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="401a3-106">The sample takes the original [Auto Claims Form Sample](auto-claims-form-sample.md) and turns it into a control that is put on a Web page.</span></span>

<span data-ttu-id="401a3-107">Weitere Informationen zur Verwendung von frei Hand Eingaben im Web finden Sie unter frei Hand Eingaben [im Web](ink-on-the-web.md).</span><span class="sxs-lookup"><span data-stu-id="401a3-107">For more information about using ink on the Web, see [Ink on the Web](ink-on-the-web.md).</span></span>

## <a name="modifications-to-the-original-sample-project"></a><span data-ttu-id="401a3-108">Änderungen am ursprünglichen Beispiel Projekt</span><span class="sxs-lookup"><span data-stu-id="401a3-108">Modifications to the Original Sample Project</span></span>

<span data-ttu-id="401a3-109">Dieses Beispiel besteht aus einer Projekt Mappe, die zwei Projekte und eine HTML-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="401a3-109">This sample consists of a solution that includes two projects and an HTML file.</span></span> <span data-ttu-id="401a3-110">Das erste Projekt, autoclaims, ist ein Microsoft Visual C- \# Steuerelement Bibliothek-Projekt (ein Benutzer Steuerelement).</span><span class="sxs-lookup"><span data-stu-id="401a3-110">The first project, AutoClaims, is a Microsoft Visual C\# Control Library project (a User Control).</span></span> <span data-ttu-id="401a3-111">Der Quellcode für dieses Steuerelement ist beinahe identisch mit dem des Beispiels "autoclaims" mit zwei unterschieden:</span><span class="sxs-lookup"><span data-stu-id="401a3-111">The source code for this control is almost identical to that of the AutoClaims sample with two differences:</span></span>

-   <span data-ttu-id="401a3-112">Die- `AutoClaims` Klasse in diesem Beispiel erbt von der [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) -Klasse und nicht von der [Formular](/dotnet/api/system.windows.forms.form?view=netcore-3.1) Klasse.</span><span class="sxs-lookup"><span data-stu-id="401a3-112">The `AutoClaims` class in this sample inherits from the [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class rather than the [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class.</span></span>

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   <span data-ttu-id="401a3-113">Die autoclaims-Klasse in diesem Beispiel verfügt über eine hinzugefügte öffentliche Methode, die die internen untergeordneten Steuer `DisposeResources` Elemente zum Sammeln von frei Hand Eingaben freigibt.</span><span class="sxs-lookup"><span data-stu-id="401a3-113">The AutoClaims Class in this sample has an added public method, `DisposeResources` that disposes of the internal child controls used for collecting ink.</span></span> <span data-ttu-id="401a3-114">Diese Methode muss von der Webpage aufgerufen werden, die das-Steuerelement verwendet, wenn diese Seite die Verwendung des-Steuer Elements beendet.</span><span class="sxs-lookup"><span data-stu-id="401a3-114">This method must be called by thewebpageon which the control is used when that page is finished using the control.</span></span>

## <a name="referencing-the-control-in-html"></a><span data-ttu-id="401a3-115">Verweisen auf das Steuerelement in HTML</span><span class="sxs-lookup"><span data-stu-id="401a3-115">Referencing the Control in HTML</span></span>

<span data-ttu-id="401a3-116">Die Lösung enthält eine HTML-Datei, default.htm.</span><span class="sxs-lookup"><span data-stu-id="401a3-116">The solution includes an HTML file, default.htm.</span></span> <span data-ttu-id="401a3-117">Diese Datei ist die Seite, zu der der Browser navigiert, um das Steuerelement zu laden.</span><span class="sxs-lookup"><span data-stu-id="401a3-117">This file is the page that the browser navigates to in order to load the control.</span></span> <span data-ttu-id="401a3-118">Die Datei enthält ein- <object> Tag, das auf das-Steuerelement verweist.</span><span class="sxs-lookup"><span data-stu-id="401a3-118">The file contains an <object> tag that references the control.</span></span> <span data-ttu-id="401a3-119">Sie enthält auch ein Skript, das aufgerufen wird, wenn die Seite entladen wird, wie durch das vorhanden sein des OnLoad = " `OnUnload()` "-Attributs im</span><span class="sxs-lookup"><span data-stu-id="401a3-119">It also includes a script that is called when the page unloads, as indicated by the presence of the onload=" `OnUnload()` " attribute in the</span></span> <body> <span data-ttu-id="401a3-120">ein.</span><span class="sxs-lookup"><span data-stu-id="401a3-120">tag.</span></span> <span data-ttu-id="401a3-121">Diese Funktion Ruft die-Methode des-Steuer Elements auf `DisposeResources` , um sicherzustellen, dass alle Ressourcen beim Herunterfahren ordnungsgemäß freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="401a3-121">This function calls the `DisposeResources` method on the control to make sure that all resources are properly released at shutdown.</span></span>


```C++
<html>
    <script language="jscript">
        // Release any resources held by the AutoClaims control
        function OnUnload()
        {
            autoClaimsControl.DisposeResources();
        }
    </script>
    <head>
        <title>AutoClaims (Web Control)</title>
    </head>
    <body onunload="OnUnload()">
        <object 
          id="autoClaimsControl" 
          classid="AutoClaims.dll#AutoClaims.AutoClaims">
        </object>
    </body>
</html> 
```



<span data-ttu-id="401a3-122">Beachten Sie das Format des ClassID-Attribut Werts für das <object> Tag.</span><span class="sxs-lookup"><span data-stu-id="401a3-122">Notice the format of the classid attribute value for the <object> tag.</span></span> <span data-ttu-id="401a3-123">Sie benennt die Assembly, gefolgt von einem \# Vorzeichen Trennzeichen, und dann den Namespace, der das Steuerelement enthält, und dann den Klassennamen des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="401a3-123">It names the assembly, followed with a \# sign separator, and then the namespace that contains the control and then the class name of the control.</span></span>

<span data-ttu-id="401a3-124">Ein Benutzer Steuerelement in der Praxis würde wahrscheinlich zusätzliche Methoden enthalten, mit denen die in der Anwendung gesammelten Daten persistent gespeichert oder gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="401a3-124">A real-world user control would likely include additional methods used to persist or send the data collected in the application.</span></span>

## <a name="the-autoclaims_webcontrol-project"></a><span data-ttu-id="401a3-125">Das Projekt autoclaims \_ WebControl</span><span class="sxs-lookup"><span data-stu-id="401a3-125">The AutoClaims\_WebControl Project</span></span>

<span data-ttu-id="401a3-126">Das Projekt autoclaims \_ WebControl ist ein Bereitstellungs Projekt, das ein-Setup erstellt, das bei der Installation ein virtuelles Stammverzeichnis, autoclaims \_ WebControl, auf dem Webserver hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="401a3-126">The AutoClaims\_WebControl project is a Deployment Project that creates a setup that adds a virtual root, AutoClaims\_WebControl, on the Web server when installed.</span></span> <span data-ttu-id="401a3-127">Das-Steuerelement und die HTML-Datei werden in diesem virtuellen Stammverzeichnis platziert.</span><span class="sxs-lookup"><span data-stu-id="401a3-127">The control and the HTML file are placed in this virtual root.</span></span>

> [!Note]  
> <span data-ttu-id="401a3-128">Die kompilierten webbeispiele werden von der Standard Installationsoption für das SDK nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="401a3-128">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="401a3-129">Sie müssen eine benutzerdefinierte Installation durchführen und die unter Option "vorkompilierte webbeispiele" auswählen, um Sie zu installieren.</span><span class="sxs-lookup"><span data-stu-id="401a3-129">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="401a3-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="401a3-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="401a3-131">Beispiel für automatisches Anspruchsformular</span><span class="sxs-lookup"><span data-stu-id="401a3-131">Auto Claims Form Sample</span></span>](auto-claims-form-sample.md)
</dt> <dt>

[<span data-ttu-id="401a3-132">Frei Hand Eingaben im Web</span><span class="sxs-lookup"><span data-stu-id="401a3-132">Ink on the Web</span></span>](ink-on-the-web.md)
</dt> </dl>

 

 
