---
title: Verwenden von COM-Objekten in Active Server Seiten
description: Sie können Skripts für COM-Objekte in Active Server Pages (ASP)-Anwendungen erstellen.
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d73244ce5bd6c56deeda9bf4e3e4986b3d4039
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309359"
---
# <a name="using-com-objects-in-active-server-pages"></a><span data-ttu-id="db04d-103">Verwenden von COM-Objekten in Active Server Seiten</span><span class="sxs-lookup"><span data-stu-id="db04d-103">Using COM Objects in Active Server Pages</span></span>

<span data-ttu-id="db04d-104">Sie können Skripts für COM-Objekte in Active Server Pages (ASP)-Anwendungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="db04d-104">You can script COM objects in Active Server Pages (ASP) applications.</span></span> <span data-ttu-id="db04d-105">Zu diesem Zweck müssen Sie zuerst eine Instanz des Objekts erstellen, indem Sie entweder das Objekttag verwenden oder die CreateObject-Methode des ASP-Server Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="db04d-105">To do so, you must first create an instance of the object either by using the OBJECT tag or by calling the CreateObject method of the ASP Server object.</span></span> <span data-ttu-id="db04d-106">Nachdem ein COM-Objekt erstellt wurde, können Sie es in nachfolgenden Skripts auf der ASP-Seite verwenden.</span><span class="sxs-lookup"><span data-stu-id="db04d-106">Once a COM object has been created, you can use it in subsequent scripts on the ASP page.</span></span>

<span data-ttu-id="db04d-107">Mithilfe von ASP können Sie mit vielen verschiedenen Typen von Skript Modulen arbeiten, die jeweils eine andere Skriptsprache unterstützen.</span><span class="sxs-lookup"><span data-stu-id="db04d-107">Using ASP, you can work with many different types of scripting engines, each of which supports a different scripting language.</span></span> <span data-ttu-id="db04d-108">ASP enthält VBScript-und JScript-Skript-Engines.</span><span class="sxs-lookup"><span data-stu-id="db04d-108">ASP comes with VBScript and JScript scripting engines.</span></span> <span data-ttu-id="db04d-109">Sie können auch Skript-Engines einbinden, die von anderen Unternehmen entwickelt wurden, um Sprachen wie z. b. Perl Script, Pscript, Python und andere zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="db04d-109">You can also plug in scripting engines developed by other companies to support languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="db04d-110">Wenn Sie die Skriptsprache für eine ASP-Seite nicht festlegen, ist VBScript die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="db04d-110">If you do not set the scripting language for an ASP page, VBScript is the default.</span></span> <span data-ttu-id="db04d-111">Wenn Sie eine andere Skriptsprache als VBScript angeben möchten, fügen Sie oben auf jeder ASP-Seite eine Zeile wie die folgende ein:</span><span class="sxs-lookup"><span data-stu-id="db04d-111">To specify a scripting language other than VBScript, include a line such as the following at the top of each ASP page:</span></span>

``` syntax
<%@ LANGUAGE=JScript %>
 
```

<span data-ttu-id="db04d-112">Wenn Sie ein COM-Objekt in einer ASP-Seite verwenden möchten, müssen Sie zuerst eine Instanz dieses Objekts erstellen.</span><span class="sxs-lookup"><span data-stu-id="db04d-112">To use a COM object in an ASP page, you must first create an instance of that object.</span></span> <span data-ttu-id="db04d-113">Verwenden Sie hierzu das Objekttag, und geben Sie den Wert "Server" für das runat-Attribut an, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="db04d-113">You do this by using the OBJECT tag and specifying the value "SERVER" for the RUNAT attribute, as shown in the following example.</span></span> <span data-ttu-id="db04d-114">Standardmäßig erstellt das Objekttag eine Instanz des-Objekts auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="db04d-114">By default, the OBJECT tag creates an instance of the object on the client.</span></span> <span data-ttu-id="db04d-115">Wenn das runat-Attribut auf Server festgelegt wird, wird das-Objekt auf dem Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="db04d-115">Setting the RUNAT attribute to SERVER causes the object to be created on the server.</span></span> <span data-ttu-id="db04d-116">Das Objekt muss auf dem Server ausgeführt werden, damit es von ASP verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="db04d-116">The object must run on the server in order to be used by ASP.</span></span>

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

<span data-ttu-id="db04d-117">Sie können auch eine Instanz eines COM-Objekts auf einer ASP-Seite erstellen, indem Sie die CreateObject-Methode des ASP-Server Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="db04d-117">You can also create an instance of a COM object on an ASP page by calling the CreateObject method of the ASP Server object.</span></span> <span data-ttu-id="db04d-118">Die Verwendung von Server. kreateobject ist langsamer als das Erstellen des Objekts mithilfe eines Objekttags, aber es ist etwas besser lesbar, da es den programmatischen Bezeichner anstelle des Klassen Bezeichners des COM-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="db04d-118">Using Server.CreateObject is slower than creating the object using an OBJECT tag, but it is slightly more readable because it specifies the programmatic identifier instead of the class identifier of the COM object.</span></span> <span data-ttu-id="db04d-119">Das Server Objekt wird von ASP verfügbar gemacht und muss nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="db04d-119">The Server object is exposed by ASP and does not need to be created.</span></span> <span data-ttu-id="db04d-120">Die Vorgehensweise zum Aufrufen von Server. kreateobject wird in den folgenden Beispielen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="db04d-120">How to call Server.CreateObject is illustrated in the following examples.</span></span> <span data-ttu-id="db04d-121">Das erste Beispiel ist VBScript:</span><span class="sxs-lookup"><span data-stu-id="db04d-121">The first example is VBScript:</span></span>

``` syntax
<% 
  Set MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

<span data-ttu-id="db04d-122">Das nächste Beispiel ist JScript:</span><span class="sxs-lookup"><span data-stu-id="db04d-122">The next example is JScript:</span></span>

``` syntax
<% 
  var MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

<span data-ttu-id="db04d-123">Das Aufrufen von CreateObject ist langsamer als die Verwendung des Objekttags zum Erstellen eines COM-Objekts.</span><span class="sxs-lookup"><span data-stu-id="db04d-123">Calling CreateObject is slower than using the OBJECT tag to create a COM object.</span></span> <span data-ttu-id="db04d-124">In Anwendungen, bei denen die Leistung kritisch ist, sollten Sie das Object-Tag verwenden.</span><span class="sxs-lookup"><span data-stu-id="db04d-124">In applications where performance is critical, you should use the OBJECT tag.</span></span>

<span data-ttu-id="db04d-125">Nachdem Sie eine Instanz des COM-Objekts erstellt haben, können Sie Sie in Skripts verwenden.</span><span class="sxs-lookup"><span data-stu-id="db04d-125">After you have created an instance of the COM object, you can use it in scripts.</span></span> <span data-ttu-id="db04d-126">Dies wird im folgenden VBScript-Beispiel veranschaulicht, mit dem der Wert der Border-Eigenschaft des COM-Objekts festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="db04d-126">Doing this is illustrated in the VBScript example following, which sets the value of the COM object's Border property.</span></span>

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a><span data-ttu-id="db04d-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db04d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db04d-128">Skripterstellung mit COM-Objekten</span><span class="sxs-lookup"><span data-stu-id="db04d-128">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




