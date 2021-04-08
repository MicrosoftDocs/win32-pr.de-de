---
description: Sie können auf jeden beliebigen XML-Webdienst zugreifen und ihn verwenden, auch wenn dieser XML-Webdienst nicht mit com+ oder sogar Microsoft Windows erstellt wurde, solange der XML-Webdienst eine WSDL-Beschreibung seiner Syntax veröffentlicht.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Zugreifen auf XML-Webdienste im WKO-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e726f430c47b3202932796455e1cf997e370a022
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748193"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a><span data-ttu-id="56f64-103">Zugreifen auf XML-Webdienste im WKO-Modus</span><span class="sxs-lookup"><span data-stu-id="56f64-103">Accessing XML Web Services in WKO Mode</span></span>

<span data-ttu-id="56f64-104">Sie können auf jeden beliebigen XML-Webdienst zugreifen und ihn verwenden, auch wenn dieser XML-Webdienst nicht mit com+ oder sogar Microsoft Windows erstellt wurde, solange der XML-Webdienst eine WSDL-Beschreibung seiner Syntax veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="56f64-104">You can access and use any XML web service, even if that XML web service was not created using COM+ or even Microsoft Windows, as long as the XML Web Service publishes a WSDL description of its syntax.</span></span> <span data-ttu-id="56f64-105">Erstellen Sie einfach eine Instanz der Komponente, indem Sie den SOAP: WSDL = URL-Moniker verwenden, wobei URL die URL der WSDL-Beschreibung des XML-Webdiensts ist, auf den Sie zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="56f64-105">Just create an instance of the component by using the soap:wsdl=URL moniker, where URL is the URL of the WSDL description of the XML web service you want to access.</span></span> <span data-ttu-id="56f64-106">Dies ist der WKO-Modus (well-known Object) für den Zugriff auf XML-Webdienste.</span><span class="sxs-lookup"><span data-stu-id="56f64-106">This is the well-known object (WKO) mode of accessing XML web services.</span></span>

<span data-ttu-id="56f64-107">Die Methoden des-Objekts können ohne besondere Überlegungen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="56f64-107">The object's methods can be called without any special considerations.</span></span> <span data-ttu-id="56f64-108">Der Zugriff auf den XML-Webdienst erfolgt über eine SOAP-Abfrage, und die Antwort wird transparent interpretiert.</span><span class="sxs-lookup"><span data-stu-id="56f64-108">The XML web service is accessed via a SOAP query, and the response is interpreted transparently.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="56f64-109">Verwaltungs Tool für Komponenten Dienste</span><span class="sxs-lookup"><span data-stu-id="56f64-109">Component Services Administrative Tool</span></span>

<span data-ttu-id="56f64-110">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="56f64-110">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="56f64-111">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="56f64-111">Visual Basic</span></span>

<span data-ttu-id="56f64-112">Das folgende Microsoft Visual Basic-Code Fragment veranschaulicht die Verwendung eines XML-Webdiensts im WKO-Modus.</span><span class="sxs-lookup"><span data-stu-id="56f64-112">The following Microsoft Visual Basic code fragment illustrates the use of an XML web service in WKO mode.</span></span>


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



<span data-ttu-id="56f64-113">In diesem Code Fragment, das die Verwendung einer Komponente einer COM+-Anwendung veranschaulicht, die als XML-Webdienst verfügbar gemacht wurde, ist Servername der voll qualifizierte Domänen Name des Servers, der den XML-Webdienst anbietet. vroot ist das virtuelle IIS-Stammverzeichnis, von dem der XML-Webdienst verfügbar gemacht wird. und ProgID ist die ProgID der Komponente, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="56f64-113">In this code fragment, which illustrates the use of a component of a COM+ application that has been exposed as an XML web service, servername is the fully qualified domain name of the server offering the XML web service; vroot is the IIS virtual root directory from which the XML web service is exposed; and progID is the ProgID of the component you want to use.</span></span>

## <a name="cc"></a><span data-ttu-id="56f64-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="56f64-114">C/C++</span></span>

<span data-ttu-id="56f64-115">Das folgende Code Fragment veranschaulicht die Verwendung eines XML-Webdiensts im WKO-Modus.</span><span class="sxs-lookup"><span data-stu-id="56f64-115">The following code fragment illustrates the use of an XML web service in WKO mode.</span></span>


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



<span data-ttu-id="56f64-116">In diesem Code Fragment, das die Verwendung einer Komponente einer COM+-Anwendung veranschaulicht, die als XML-Webdienst verfügbar gemacht wurde, ist Servername der voll qualifizierte Domänen Name des Servers, der den XML-Webdienst anbietet. vroot ist das virtuelle IIS-Stammverzeichnis, von dem der XML-Webdienst verfügbar gemacht wird. und ProgID ist die ProgID der Komponente, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="56f64-116">In this code fragment, which illustrates the use of a component of a COM+ application that has been exposed as an XML web service, servername is the fully qualified domain name of the server offering the XML web service; vroot is the IIS virtual root directory from which the XML web service is exposed; and progID is the ProgID of the component you want to use.</span></span>

## <a name="remarks"></a><span data-ttu-id="56f64-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56f64-117">Remarks</span></span>

<span data-ttu-id="56f64-118">Beim ersten Zugriff auf einen XML-Webdienst im WKO-Modus generiert com+ einen Proxy Client und kompiliert ihn im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="56f64-118">When an XML web service is first accessed in WKO mode, COM+ generates a proxy client and compiles it in the background.</span></span> <span data-ttu-id="56f64-119">Diese Lauf Zeit Generierung und der Mangel an permanenten Verbindungen im WKO-Modus führen im Vergleich zum Modus "Cao" zu einer erheblich geringeren Leistung.</span><span class="sxs-lookup"><span data-stu-id="56f64-119">This run-time generation and the lack of persistent connections in WKO mode results in significantly reduced performance in comparison to CAO mode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56f64-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56f64-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56f64-121">Zugreifen auf XML-Webdienste im Modus "Cao"</span><span class="sxs-lookup"><span data-stu-id="56f64-121">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="56f64-122">Übersicht über den COM+ SOAP-Dienst</span><span class="sxs-lookup"><span data-stu-id="56f64-122">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="56f64-123">Erstellen von XML-Webdiensten</span><span class="sxs-lookup"><span data-stu-id="56f64-123">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="56f64-124">Sichern von XML-Webdiensten</span><span class="sxs-lookup"><span data-stu-id="56f64-124">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 



