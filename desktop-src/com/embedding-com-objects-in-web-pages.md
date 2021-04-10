---
title: Einbetten von COM-Objekten in Webseiten
description: Sie können COM-Objekte in Webseiten verwenden. Erstellen Sie zu diesem Zweck zunächst eine Instanz dieses COM-Objekts. Nachdem eine Objektinstanz erstellt wurde, können Sie Sie in nachfolgenden Skripts auf dieser Webseite verwenden.
ms.assetid: 7e2c9da7-aeae-4206-8be9-1303240b2b1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4762dd01d4bc07aab5c0b146c56cdb1aec3cb28f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309728"
---
# <a name="embedding-com-objects-in-web-pages"></a><span data-ttu-id="2c50a-105">Einbetten von COM-Objekten in Webseiten</span><span class="sxs-lookup"><span data-stu-id="2c50a-105">Embedding COM Objects in Web Pages</span></span>

<span data-ttu-id="2c50a-106">Sie können COM-Objekte in Webseiten verwenden.</span><span class="sxs-lookup"><span data-stu-id="2c50a-106">You can use COM objects in webpages.</span></span> <span data-ttu-id="2c50a-107">Erstellen Sie zu diesem Zweck zunächst eine Instanz dieses COM-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2c50a-107">To do this, first create an instance of that COM object.</span></span> <span data-ttu-id="2c50a-108">Nachdem eine Objektinstanz erstellt wurde, können Sie Sie in nachfolgenden Skripts auf dieser Webseite verwenden.</span><span class="sxs-lookup"><span data-stu-id="2c50a-108">After an object instance is created, you can use it in subsequent scripts on that webpage.</span></span>

<span data-ttu-id="2c50a-109">Um eine com-Objektinstanz auf einer Webseite zu erstellen, können Sie ein Objekttag verwenden.</span><span class="sxs-lookup"><span data-stu-id="2c50a-109">To create a COM object instance in a webpage, you can use an OBJECT tag.</span></span> <span data-ttu-id="2c50a-110">Wenn Ihre Skriptsprache eine native Methode zum Erstellen von COM-Objekten bereitstellt, können Sie alternativ eine Objektinstanz mithilfe eines Skripts erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c50a-110">Alternatively, if your scripting language provides a native way to create COM objects, you can create an object instance using script.</span></span>

<span data-ttu-id="2c50a-111">Beachten Sie, dass das Einbetten von COM-Objekten in Webseiten nur mit Browsern funktioniert, die ActiveX und com unterstützen, z.b. Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2c50a-111">Note that embedding COM objects in webpages only works with browsers that support ActiveX and COM, for example Internet Explorer.</span></span>

<span data-ttu-id="2c50a-112">Im folgenden Beispiel wird veranschaulicht, wie das Objekttag zum Einbetten eines COM-Objekts in eine Webseite verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="2c50a-112">The following example illustrates using the OBJECT tag to embed a COM object in a webpage:</span></span>

``` syntax
<OBJECT 
  ID = vid 
  CLASSID = "clsid:31263EC0-2957-11CF-A1E5-00AA9EC79700" 
  BORDER = 0 
  VSPACE = 0 
  HSPACE = 0 
  ALIGN = TOP 
  HEIGHT = 100% 
  WIDTH = 100%
>
</OBJECT>
 
```

<span data-ttu-id="2c50a-113">Sie können auch eine com-Objektinstanz im Skript erstellen, wenn Ihre Skriptsprache eine Möglichkeit zum Erstellen von COM-Objekten bietet.</span><span class="sxs-lookup"><span data-stu-id="2c50a-113">You can also create a COM object instance in script, if your scripting language provides a way to create COM objects.</span></span> <span data-ttu-id="2c50a-114">VBScript stellt z. b. die Methode "-Methode" und "JScript" das ActiveXObject-Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="2c50a-114">For example, VBScript provides the CreateObject method and JScript provides the ActiveXObject object.</span></span> <span data-ttu-id="2c50a-115">Das Erstellen von Objekten in Skripts wird in den folgenden Beispielen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2c50a-115">Creating objects in script is illustrated in the following examples.</span></span>

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

<span data-ttu-id="2c50a-116">Neben der Methode "kreateobject" und dem ActiveXObject-Objekt wird von VBScript und JScript die Methode "GetObject" bereitgestellt, die eine Objektinstanz zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2c50a-116">In addition to the CreateObject method and the ActiveXObject object, both VBScript and JScript provide the method GetObject, which returns an object instance.</span></span>

<span data-ttu-id="2c50a-117">Nachdem ein COM-Objekt erstellt wurde, können Sie es in nachfolgenden Skripts mit dem im ID-Attribut des Objekttags angegebenen Bezeichner referenzieren.</span><span class="sxs-lookup"><span data-stu-id="2c50a-117">After a COM object has been created, you can reference it in subsequent scripts by using the identifier specified in the OBJECT tag's ID attribute.</span></span> <span data-ttu-id="2c50a-118">Im vorherigen Beispiel wurde dieser Bezeichner als "vid" angegeben.</span><span class="sxs-lookup"><span data-stu-id="2c50a-118">In the preceding example, this identifier was specified as "vid."</span></span> <span data-ttu-id="2c50a-119">Beachten Sie, dass das Skript, das das COM-Objekt verwendet, nach dem Objekttag oder dem Skript angezeigt werden muss, das die Objektinstanz erstellt. Andernfalls ist der Objekt Bezeichner nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="2c50a-119">Note that the script that uses the COM object must appear after the OBJECT tag or script that creates the object instance; otherwise, the object identifier is undefined.</span></span> <span data-ttu-id="2c50a-120">Im folgenden Skript wird das objxl-Objekt verwendet, um die Versionsinformationen für Microsoft Excel anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2c50a-120">The following script uses the objXL object to display the version information for Microsoft Excel.</span></span>

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

<span data-ttu-id="2c50a-121">Wenn Sie Skripts schreiben, die auf einer Webseite eingebettet sind, stellt der Browser auch ein Objektmodell bereit, auf das Ihre Skripts zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="2c50a-121">If you are writing scripts embedded in a webpage, the browser also exposes an object model that your scripts can access.</span></span> <span data-ttu-id="2c50a-122">Das Modell, das von Internet Explorer verwendet wird, entspricht dem vom World Wide Web Consortium (W3C) vorgeschlagenen Dokumentobjektmodell (DOM).</span><span class="sxs-lookup"><span data-stu-id="2c50a-122">The model used by Internet Explorer conforms to the Document Object Model (DOM) proposed by the World Wide Web Consortium (W3C).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c50a-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2c50a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c50a-124">Skripterstellung mit COM-Objekten</span><span class="sxs-lookup"><span data-stu-id="2c50a-124">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




