---
title: Die Schnittstellen Proxy Datei
description: Bei der Schnittstellen Proxy Datei (U \_ p. c) handelt es sich um eine c-Datei, die Routinen enthält, die den Client-Stub-und Server-Stub-Dateien einer COM-Schnittstelle (com) entsprechen.
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- Mittel l und com-Mittel l, Schnittstellen, Proxy Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be52b3561af03df0375212d729f64f41e3cdd7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947903"
---
# <a name="the-interface-proxy-file"></a><span data-ttu-id="94d3c-104">Die Schnittstellen Proxy Datei</span><span class="sxs-lookup"><span data-stu-id="94d3c-104">The Interface Proxy File</span></span>

<span data-ttu-id="94d3c-105">Bei der Schnittstellen Proxy Datei (U \_ p. c) handelt es sich um eine c-Datei, die Routinen enthält, die den Client-Stub-und Server-Stub-Dateien einer COM-Schnittstelle (com) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="94d3c-105">The interface proxy file (U\_p.c) is a C file that contains routines equivalent to those in the client stub and server stub files of an object (COM) interface.</span></span> <span data-ttu-id="94d3c-106">Diese Datei enthält Implementierungen der Ersatz Zeichenroutinen für Client und Server im Inline Modus des Compilers, oder äquivalente Daten und thunna in den interpretierten Modi sowie andere geeignete com-Daten, wie z. b. die Proxy-und stubvtables.</span><span class="sxs-lookup"><span data-stu-id="94d3c-106">This file contains implementations of the surrogate routines for client and server in the inline mode of the compiler or equivalent data and thunks in the interpreted modes, as well as other appropriate COM glue data, such as the proxy and stub Vtables.</span></span>

<span data-ttu-id="94d3c-107">Die Schnittstellen Proxy Datei enthält die unterstützenden Routinen und Daten nur für Methoden der Schnittstellen, die in der aktuellen IDL-Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="94d3c-107">The interface proxy file includes the supporting routines and data only for methods of the interfaces defined in the current IDL file.</span></span> <span data-ttu-id="94d3c-108">Um dieses Verhalten zu verdeutlichen, wird in diesem Abschnitt ein erweitertes Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="94d3c-108">To clarify this behavior, an extended example is used throughout this section.</span></span> <span data-ttu-id="94d3c-109">Beim Kompilieren einer IDL-Datei mit einer Schnittstelle, wie z. b. ifaceb, die von ifacea erbt, werden mit ifaceb verknüpfte zusätzliche Daten und Routinen in der aktuellen Proxy Datei generiert, während die ifacea-bezogenen Erweiterungs Daten und-Routinen in dem von der IDL-Datei generierten Proxy gefunden werden</span><span class="sxs-lookup"><span data-stu-id="94d3c-109">When compiling an IDL file with an interface such as IFaceB that inherits from IFaceA, IFaceB related auxiliary data and routines are generated to the current proxy file, while the base interface IFaceA related auxiliary data and routines are found in the proxy generated from the IDL file containing the IFaceA definition.</span></span> <span data-ttu-id="94d3c-110">Der Compiler generiert alle Daten, die erforderlich sind, um die Ersatz Zeichen der Basisschnittstelle zu identifizieren, und um Sie bei Bedarf zu delegieren, um die durch die ifaceb-Schnittstelle verwendeten ifacea-Methoden zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="94d3c-110">The compiler generates all data necessary to identify the surrogates of the base interface, and to delegate to them when needed to support the IFaceA methods used through IFaceB interface.</span></span>

<span data-ttu-id="94d3c-111">Für jede Methode in einer Schnittstelle in der aktuellen IDL-Datei enthält die Proxy Datei die folgenden zwei Ersatzmethoden, wenn Sie im gemischten Modus ([/OS](-os.md)) kompiliert werden, und äquivalente interpreterdaten, wenn Sie im Interpretermodus ([/Oi](-oi.md)) kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="94d3c-111">For every method in an interface in the current IDL file, the proxy file contains the following two surrogate methods when compiled in the mixed mode ([/Os](-os.md)), and equivalent interpreter data when compiled in the interpreter mode ([/Oi](-oi.md)).</span></span>

-   <span data-ttu-id="94d3c-112">Das Client seitige Ersatz Zeichen, z. b. der ifaceb- \_ Methoden \_ Proxy in diesem Beispiel.</span><span class="sxs-lookup"><span data-stu-id="94d3c-112">The client-side surrogate, such as IFaceB\_Method\_Proxy in this example.</span></span>

    <span data-ttu-id="94d3c-113">Dieses Client seitige Ersatz Zeichen ist der virtuelle Einstiegspunkt, an den der Client, z. b. ifaceb:: Method, sendet.</span><span class="sxs-lookup"><span data-stu-id="94d3c-113">This client-side surrogate is the virtual entry point to which the client, for example IFaceB::Method, dispatches.</span></span> <span data-ttu-id="94d3c-114">Sie marshallt die Eingabeargumente in ein ausführbares Formular, überträgt die gemarshallten Argumente zusammen mit Informationen, die die-Schnittstelle und den-Vorgang identifizieren, und entmarshallt den Rückgabewert und alle Ausgabe Argumente, wenn der aufgerufene Vorgang zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="94d3c-114">It marshals the input arguments into a transmittable form, transmits the marshaled arguments along with information that identifies the interface and the operation, and then unmarshals the return value and any output arguments when the invoked operation returns.</span></span>

-   <span data-ttu-id="94d3c-115">Das serverseitige Ersatz Zeichen, z. b. ifaceb- \_ \_ Methodenstub.</span><span class="sxs-lookup"><span data-stu-id="94d3c-115">The server-side surrogate, for example, IFaceB\_Method\_Stub .</span></span>

    <span data-ttu-id="94d3c-116">Dieses serverseitige Ersatz Zeichen ist der virtuelle Einstiegspunkt, an den die zugrunde liegende Laufzeit zum Emulieren des Clients auf dem Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="94d3c-116">This server-side surrogate is the virtual entry point that the underlying runtime dispatches to at the server to emulate the client.</span></span> <span data-ttu-id="94d3c-117">Die Eingabeargumente werden zum Replizieren der Client Daten, zum Aufrufen der Implementierung der Schnittstelle des Servers und zum anschließenden marshunzieren und übertragen des Rückgabewerts sowie der Ausgabe Argumente an die Clientseite zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="94d3c-117">It unmarshals the input arguments to replicate the client data, invokes the server's implementation of the interface function, and then marshals and transmits the return value and any output arguments back to the client side.</span></span>

<span data-ttu-id="94d3c-118">Der Standardname für eine aus einer Datei erstellte Proxy Datei. idl ist die Datei \_ p. c. verwenden Sie den [**/Proxy**](-proxy.md) -Compilerschalter, um den Standardnamen der Schnittstellen Proxy Datei zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="94d3c-118">The default name for a proxy file generated from a file.idl is file\_p.c.Use the [**/proxy**](-proxy.md) MIDL compiler switch to override the default name of the interface proxy file.</span></span> <span data-ttu-id="94d3c-119">Die Schalter [**/env**](-env.md) und [**/out**](-out.md) beeinflussen diese Datei.</span><span class="sxs-lookup"><span data-stu-id="94d3c-119">The [**/env**](-env.md) and [**/out**](-out.md) switches affect this file.</span></span>

 

 




