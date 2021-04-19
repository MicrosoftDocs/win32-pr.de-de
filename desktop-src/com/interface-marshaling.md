---
title: Schnittstellenmarshalling
description: Schnittstellenmarshalling
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5112b67e643fb95e1025fd4ed297043f81f576e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337874"
---
# <a name="interface-marshaling"></a><span data-ttu-id="435f7-103">Schnittstellenmarshalling</span><span class="sxs-lookup"><span data-stu-id="435f7-103">Interface Marshaling</span></span>

<span data-ttu-id="435f7-104">Wenn Sie nicht sicher sind, dass Ihre Schnittstelle nie über Apartment-, Thread-oder Prozess Grenzen hinweg verwendet wird, müssen Sie entscheiden, wie Sie Marshallingunterstützung für ihre Schnittstellen bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="435f7-104">Unless you know beyond all doubt that your interface will never be used across apartment, thread, or process boundaries, you need to decide how to provide marshaling support for your interfaces.</span></span> <span data-ttu-id="435f7-105">Es gibt drei Möglichkeiten, marshalingunterstützung bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="435f7-105">There are three ways to provide marshaling support:</span></span>

-   <span data-ttu-id="435f7-106">Schreiben Sie Ihren eigenen Proxy-/Stubcode, der den com-Kanal aufruft, der wiederum die RPC-Laufzeitbibliotheken aufruft.</span><span class="sxs-lookup"><span data-stu-id="435f7-106">Write your own proxy/stub code that calls the COM channel, which in turn calls the RPC run-time libraries.</span></span> <span data-ttu-id="435f7-107">Theoretisch ist es möglich, dies zu tun, aber in der Praxis ist es fast unmöglich, ohne großen Aufwand zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="435f7-107">Theoretically, it is possible to do this, but in practice it is almost impossible to do without a significant amount of effort.</span></span>
-   <span data-ttu-id="435f7-108">Beschreiben Sie die Schnittstellen in einer IDL-Datei (Interface Definition Language), und verwenden Sie den-compilercompiler, um eine Proxy-/Stub-DLL zu generieren.</span><span class="sxs-lookup"><span data-stu-id="435f7-108">Describe your interfaces in an interface definition language (IDL) file and use the MIDL compiler to generate a proxy/stub DLL.</span></span> <span data-ttu-id="435f7-109">Diese Methode bietet die beste Leistung und die größte Flexibilität in Bezug auf akzeptable Datentypen.</span><span class="sxs-lookup"><span data-stu-id="435f7-109">This method provides the best performance and the most flexibility in terms of acceptable data types.</span></span> <span data-ttu-id="435f7-110">Mithilfe von mit mittlerer l generierten proxystubzugriff können Sie nicht nur die Speicherverwaltung steuern, sondern auch das Marshalling und das nicht Marshalling komplexer Datentypen auf verschiedenen Plattformen.</span><span class="sxs-lookup"><span data-stu-id="435f7-110">Using MIDL-generated proxy stubs, you can control not only memory management but even the marshaling and unmarshaling of complex data types across different platforms.</span></span>
-   <span data-ttu-id="435f7-111">Verwenden Sie die-Mittell, um eine Typbibliothek zu generieren, mit der das System zur Laufzeit Marshallingunterstützung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="435f7-111">Use MIDL to generate a type library that the system uses to provide marshaling support at run time.</span></span> <span data-ttu-id="435f7-112">Dies ist die einfachste Möglichkeit zum Implementieren von Marshalling-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="435f7-112">This is the easiest way to implement marshaling support.</span></span> <span data-ttu-id="435f7-113">Sie müssen lediglich eine Typbibliothek generieren und registrieren.</span><span class="sxs-lookup"><span data-stu-id="435f7-113">All you have to do is generate a type library and register it.</span></span> <span data-ttu-id="435f7-114">Ihre Schnittstellen müssen Automatisierungs kompatibel sein (entweder [**oleautomation**](/windows/desktop/Midl/oleautomation) oder [**Dual**](/windows/desktop/Midl/dual)), sodass einige Einschränkungen hinsichtlich der Arten von Datentypen bestehen, die Sie als Methoden Parameter verwenden können.</span><span class="sxs-lookup"><span data-stu-id="435f7-114">Your interfaces must be Automation-compatible (either [**oleautomation**](/windows/desktop/Midl/oleautomation) or [**dual**](/windows/desktop/Midl/dual)), which places some restrictions on the kinds of data types you can use as method parameters.</span></span> <span data-ttu-id="435f7-115">In den meisten Fällen hat der Vorteil, dass die Schnittstellen für Programme, die in anderen Sprachen geschrieben wurden, wie z. b. Microsoft Visual Basic und Java, die Einschränkungen der Datentypen.</span><span class="sxs-lookup"><span data-stu-id="435f7-115">However, in most cases, the advantage of having your interfaces accessible to programs written in other languages, such as Microsoft Visual Basic and Java, outweighs the limitations on data types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="435f7-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="435f7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="435f7-117">Kommunikation zwischen Objekten</span><span class="sxs-lookup"><span data-stu-id="435f7-117">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> </dl>

 

 