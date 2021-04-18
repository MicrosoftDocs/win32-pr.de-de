---
description: Eine Möglichkeit zum Erstellen von frei Hand fähigen Webanwendungen besteht darin, innerhalb von Microsoft Internet Explorer Windows Forms Steuerelemente in awebpagezu platzieren.
ms.assetid: a4fcd692-cd4a-4d2a-bfad-198010e27c6f
title: Websteuer Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b28fa2a3293b6b780412ddbc755634c745b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343285"
---
# <a name="web-controls"></a><span data-ttu-id="f529f-103">Websteuer Elemente</span><span class="sxs-lookup"><span data-stu-id="f529f-103">Web Controls</span></span>

<span data-ttu-id="f529f-104">Eine Möglichkeit zum Erstellen von frei Hand fähigen Webanwendungen besteht darin, innerhalb von Microsoft Internet Explorer Windows Forms Steuerelemente in awebpagezu platzieren.</span><span class="sxs-lookup"><span data-stu-id="f529f-104">One way to create ink-enabled Web applications is to put Windows Forms controls inside awebpagewithin Microsoft Internet Explorer.</span></span> <span data-ttu-id="f529f-105">Ein gutes Tutorial zu diesem Verfahren finden Sie unter Verwenden von Windows Forms-Steuer [Elementen in Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx).</span><span class="sxs-lookup"><span data-stu-id="f529f-105">A good tutorial on this technique can be found at [Using Windows Forms Controls in Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx).</span></span> <span data-ttu-id="f529f-106">Die grundlegenden Schritte im Tutorial lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f529f-106">The basic steps in the tutorial are:</span></span>

1.  <span data-ttu-id="f529f-107">Erstellen Sie ein Steuerelement, das von [**System. Windows. Forms. UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)erbt.</span><span class="sxs-lookup"><span data-stu-id="f529f-107">Create a control that inherits from [**System.Windows.Forms.UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).</span></span>
2.  <span data-ttu-id="f529f-108">Erstellen Sie eine HTML-Seite mit einem Objekttag, das auf das UserControl-Steuerelement verweist.</span><span class="sxs-lookup"><span data-stu-id="f529f-108">Create an HTML page with an object tag that refers to that UserControl.</span></span>
3.  <span data-ttu-id="f529f-109">Erstellen Sie ein virtuelles Verzeichnis, und legen Sie Berechtigungen fest.</span><span class="sxs-lookup"><span data-stu-id="f529f-109">Create a virtual directory and set permissions.</span></span>
4.  <span data-ttu-id="f529f-110">Laden Sie die URL der HTML-Seite in den Browser.</span><span class="sxs-lookup"><span data-stu-id="f529f-110">Load the URL of the HTML page into the browser.</span></span>

<span data-ttu-id="f529f-111">Diese Technik kann auf Freihand-aktivierte Steuerelemente wie jedes andere Windows Forms [**Steuer**](/dotnet/api/system.windows.forms.control?view=netcore-3.1)Element angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f529f-111">This technique can be applied to ink-enabled controls, just like any other Windows Forms [**Control**](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span></span> <span data-ttu-id="f529f-112">Tatsächlich kann die Technik mit jeder Klasse im Microsoft .NET Framework verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f529f-112">In fact, the technique can be used with any class in the Microsoft .NET Framework.</span></span> <span data-ttu-id="f529f-113">Die vom Microsoft Windows XP Tablet PC Edition-SDK (Software Development Kit) bereitgestellten Beispiele beinhalten eine websteuerungs Version des Beispiels "Auto Claims" im Abschnitt "Ink Web Samples".</span><span class="sxs-lookup"><span data-stu-id="f529f-113">The samples provided by the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) include a Web control version of the Auto Claims sample in the Ink Web Samples section.</span></span> <span data-ttu-id="f529f-114">In diesem Beispiel wird das ursprüngliche [Formular Beispiel für automatische Ansprüche](auto-claims-form-sample.md) übernommen und in ein Steuerelement umgewandelt, das auf einer Webseite abgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f529f-114">This example takes the original [Auto Claims Form Sample](auto-claims-form-sample.md) and turns it into a control that is put on a Web page.</span></span> <span data-ttu-id="f529f-115">Weitere Informationen zur Webaktivierung dieses Beispiels finden Sie im Beispiel für das [Ink-websteuer](ink-web-control-sample.md)Element.</span><span class="sxs-lookup"><span data-stu-id="f529f-115">For more information about Web-enabling this sample, see the [Ink Web Control Sample](ink-web-control-sample.md).</span></span>

> [!Note]  
> <span data-ttu-id="f529f-116">Wenn Sie eine Anwendung bereitstellen, die mithilfe von .net über das Internet erstellt wurde, kann die Anwendung vom Sicherheitsmodell für .net betroffen sein.</span><span class="sxs-lookup"><span data-stu-id="f529f-116">When you deploy an application created by using .NET over the Web, the application may be affected by security model for .NET.</span></span> <span data-ttu-id="f529f-117">Weitere Informationen zur Funktionsweise der Sicherheit mit frei Hand fähigen Webanwendungen finden Sie unter [Sicherheit und Vertrauens](security-and-trust.md)Stellung.</span><span class="sxs-lookup"><span data-stu-id="f529f-117">For more information about how security works with ink-enabled Web applications, see [Security and Trust](security-and-trust.md).</span></span>

 

 

 
