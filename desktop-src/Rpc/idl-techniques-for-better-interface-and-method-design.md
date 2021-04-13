---
title: IDL-Techniken für einen besseren Schnittstellen-und Methoden Entwurf
description: Verwenden Sie die folgenden IDL-spezifischen Techniken, um die Sicherheit und Leistung bei der Entwicklung von RPC-Schnittstellen und-Methoden zu verbessern, die sowohl konforme als auch Variant-Daten verarbeiten.
ms.assetid: 651bdb5c-ad56-4526-9b7d-7165141e7ceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b897d8d1f2f5e1c11a5328fb095341871e3689e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388228"
---
# <a name="idl-techniques-for-better-interface-and-method-design"></a><span data-ttu-id="a84c8-103">IDL-Techniken für einen besseren Schnittstellen-und Methoden Entwurf</span><span class="sxs-lookup"><span data-stu-id="a84c8-103">IDL Techniques for Better Interface and Method Design</span></span>

<span data-ttu-id="a84c8-104">Verwenden Sie die folgenden IDL-spezifischen Techniken, um die Sicherheit und Leistung bei der Entwicklung von RPC-Schnittstellen und-Methoden zu verbessern, die sowohl konforme als auch Variant-Daten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a84c8-104">Consider using the following IDL-specific techniques to improve security and performance when you are developing RPC interfaces and methods that handle both conformant and variant data.</span></span> <span data-ttu-id="a84c8-105">Die Attribute, auf die in diesem Thema verwiesen wird, sind die IDL-Attribute, die für Methoden Parameter festgelegt werden, die entweder konforme Daten verarbeiten (z. b. die \[ **\_ Größe** \] und die \[ **Maximale \_** \] Anzahl von Attributen) oder Variant-Daten (z. b. die \[ **Länge \_** \] und \[ **Zeichen** folgen \] Attribute).</span><span class="sxs-lookup"><span data-stu-id="a84c8-105">The attributes referred to in this topic are the IDL attributes set on method parameters that handle either conformant data (for example, the \[**size\_is**\] and \[**max\_is**\] attributes) or variant data (for example, the \[**length\_is**\] and \[**string**\] attributes).</span></span>

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a><span data-ttu-id="a84c8-106">Verwenden des \[ Range- \] Attributs mit kompatiblen Daten Parametern</span><span class="sxs-lookup"><span data-stu-id="a84c8-106">Using the \[range\] Attribute with Conformant Data Parameters</span></span>

<span data-ttu-id="a84c8-107">Das \[ **Range** \] -Attribut weist die RPC-Laufzeit an, während des Daten unmarshallingprozesses eine zusätzliche Größenüberprüfung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a84c8-107">The \[**range**\] attribute instructs the RPC run-time to perform additional size validation during the data unmarshaling process.</span></span> <span data-ttu-id="a84c8-108">Insbesondere wird überprüft, ob die angegebene Größe der Daten, die als zugeordneter Parameter übergeben werden, innerhalb des angegebenen Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="a84c8-108">Specifically, it verifies that the supplied size of the data passed as the associated parameter is within the specified range.</span></span>

<span data-ttu-id="a84c8-109">Das \[ **Range** - \] Attribut wirkt sich nicht auf das Wire-Format aus.</span><span class="sxs-lookup"><span data-stu-id="a84c8-109">The \[**range**\] attribute does not affect wire format.</span></span>

<span data-ttu-id="a84c8-110">Wenn der Wert für Wire außerhalb des zulässigen Bereichs liegt, löst RPC eine \_ ungültige RPC x \_ - \_ gebundene oder RPC x-Daten Ausnahme für einen ungültigen \_ \_ \_ Stub aus \_ .</span><span class="sxs-lookup"><span data-stu-id="a84c8-110">If the value on wire is outside of the allowed range, RPC will throw an RPC\_X\_INVALID\_BOUND or RPC\_X\_BAD\_STUB\_DATA exception.</span></span> <span data-ttu-id="a84c8-111">Dadurch wird eine zusätzliche Ebene der Datenüberprüfung ermöglicht, und häufige Sicherheitsfehler wie Pufferüberläufe können vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="a84c8-111">This provides an additional level of data validation, and can help prevent common security errors like buffer overruns.</span></span> <span data-ttu-id="a84c8-112">Ebenso \[  \] kann durch die Verwendung von Range die Anwendungsleistung verbessert werden, da konforme Daten, die mit diesem gekennzeichnet sind, klar definierte Einschränkungen für den RPC-Dienst zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="a84c8-112">Likewise, using \[**range**\] can improve application performance, since conformant data marked with it has clearly-defined constraints available for consideration by the RPC service.</span></span>

## <a name="rpc-server-stub-memory-management-rules"></a><span data-ttu-id="a84c8-113">Regeln für die Speicherverwaltung von RPC-Server-Stubs</span><span class="sxs-lookup"><span data-stu-id="a84c8-113">RPC Server Stub Memory Management Rules</span></span>

<span data-ttu-id="a84c8-114">Beim Erstellen der IDL-Dateien für eine RPC-fähige Anwendung ist es wichtig, dass Sie die Regeln für die Verwaltung von RPC-Server-Stubs verstehen.</span><span class="sxs-lookup"><span data-stu-id="a84c8-114">It is important to understand RPC server stub memory management rules when creating the IDL files for an RPC-enabled application.</span></span> <span data-ttu-id="a84c8-115">Anwendungen können die Auslastung der Server Ressourcen verbessern, indem Sie einen \[ **Bereich** \] in Verbindung mit konformen Daten wie oben angegeben verwenden, und die Anwendung von Daten-IDL-Attributen variabler Länge wie etwa \[ **length \_** \] in Übereinstimmung mit Daten vermeiden.</span><span class="sxs-lookup"><span data-stu-id="a84c8-115">Applications can improve server resource utilization by using \[**range**\] in conjunction with conformant data as indicated above, as well as deliberately avoiding the application of variable-length data IDL attributes like like \[**length\_is**\] to conformant data.</span></span>

<span data-ttu-id="a84c8-116">Die Anwendung der \[ **Länge \_ erfolgt** \] auf Datenstruktur Felder, die in einer IDL-Datei definiert sind, wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="a84c8-116">The application of \[**length\_is**\] to data structure fields defined in an IDL file is not recommended.</span></span>

## <a name="best-practices-for-variable-length-data-parameters"></a><span data-ttu-id="a84c8-117">Bewährte Methoden für Daten Parameter mit variabler Länge</span><span class="sxs-lookup"><span data-stu-id="a84c8-117">Best Practices for Variable-length Data Parameters</span></span>

<span data-ttu-id="a84c8-118">Nachfolgend sind einige bewährte Methoden zu beachten, die beim Definieren der IDL-Attribute für Datenstrukturen variabler Größen, Methoden Parameter und Felder zu beachten sind.</span><span class="sxs-lookup"><span data-stu-id="a84c8-118">The following are several best practices to consider when defining the IDL attributes for variable-sized data structures, method parameters and fields.</span></span>

-   <span data-ttu-id="a84c8-119">Frühe Korrelation verwenden.</span><span class="sxs-lookup"><span data-stu-id="a84c8-119">Use early correlation.</span></span> <span data-ttu-id="a84c8-120">Es ist in der Regel besser, den Variablen Größen Parameter oder das Feld so zu definieren, dass er unmittelbar nach dem steuernden ganzzahligen Typ auftritt.</span><span class="sxs-lookup"><span data-stu-id="a84c8-120">It is generally better to define the variable size parameter or field such that it occurs immediately after the controlling integral type.</span></span>

    <span data-ttu-id="a84c8-121">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a84c8-121">For example,</span></span>

    ``` syntax
    earlyCorr
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long size, 
    [in,size_is(size)] char *pv
    );
    ```

    <span data-ttu-id="a84c8-122">besser als</span><span class="sxs-lookup"><span data-stu-id="a84c8-122">is better than</span></span>

    ``` syntax
    lateCorr
    (
    [in,size_is(size)] char *pv, 
    [in, range(MIN_COUNT, MAX_COUNT)] long size)
    );
    ```

    <span data-ttu-id="a84c8-123">Dabei deklariert **earlycorr** den size-Parameter direkt vor dem Daten Parameter mit variabler Länge, und **latecorr** deklariert den size-Parameter danach.</span><span class="sxs-lookup"><span data-stu-id="a84c8-123">wherein **earlyCorr** declares the size parameter immediately before the variable-length data parameter, and **lateCorr** declares the size parameter after it.</span></span> <span data-ttu-id="a84c8-124">Mithilfe der frühen Korrespondenz wird die Leistung insgesamt verbessert, insbesondere in Fällen, in denen die-Methode häufig aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a84c8-124">Using early correspondence improves performance overall, especially in cases where the method is called frequently.</span></span>

-   <span data-ttu-id="a84c8-125">Bei Parametern, die mit "out" gekennzeichnet sind \[ **, \_ ist "size** " ein \] Attribut-Tupel, und wenn die Daten Länge auf der Clientseite bekannt ist oder der Client über eine vernünftige obere Grenze verfügt, sollte die Methoden Definition der folgenden in Bezug auf die Parameter Zuordnung und-Reihenfolge ähneln:</span><span class="sxs-lookup"><span data-stu-id="a84c8-125">For parameters marked with the \[**out, size\_is**\] attribute tuple, and where the data length is known on the client side or where the client has a reasonable upper bound, the method definition should be similar to the following in terms of parameter attribution and sequence:</span></span>

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    <span data-ttu-id="a84c8-126">In diesem Fall stellt der Client einen Puffer mit fester Größe für die *Bir* bereit, sodass der serverseitige RPC-Dienst einen Puffer mit hoher Sicherheit zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="a84c8-126">In this case, the client provides a fixed size buffer for *pArr*, allowing the server-side RPC service to allocate a reasonably-sized buffer with a good degree of assurance.</span></span> <span data-ttu-id="a84c8-127">Beachten Sie, dass im Beispiel die Daten vom Server ( \[ **out** \] ) empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="a84c8-127">Note that in the example the data is received from the server (\[**out**\]).</span></span> <span data-ttu-id="a84c8-128">Die Definition ist für Daten, die an den Server übermittelt werden, ähnlich ( \[ **in** \] ).</span><span class="sxs-lookup"><span data-stu-id="a84c8-128">The definition is similar for data passed to the server (\[**in**\]).</span></span>

-   <span data-ttu-id="a84c8-129">In Situationen, in denen die serverseitige Komponente einer RPC-Anwendung die Daten Länge bestimmt, sollte die Methoden Definition wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="a84c8-129">For situations where the server-side component of an RPC application decides the data length, the method definition should be similar to the following:</span></span>

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    <span data-ttu-id="a84c8-130">**Bereichs \_ Long** ist ein Typ, der sowohl für den Client-als auch für den serverstubwert und für eine angegebene Größe definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a84c8-130">**RANGED\_LONG** is a type defined for both the client and server stubs, and of a specified size the client can correctly anticipate.</span></span> <span data-ttu-id="a84c8-131">Im Beispiel übergibt der Client *pparr* als **null**, und die RPC-Server Anwendungs Komponente ordnet die richtige Arbeitsspeicher Menge zu.</span><span class="sxs-lookup"><span data-stu-id="a84c8-131">In the example, the client passes *ppArr* as **NULL**, and the RPC server application component allocates the correct amount of memory.</span></span> <span data-ttu-id="a84c8-132">Bei der Rückgabe ordnet der RPC-Dienst auf der Clientseite den Arbeitsspeicher für die zurückgegebenen Daten zu.</span><span class="sxs-lookup"><span data-stu-id="a84c8-132">Upon return, the RPC service on the client side allocates the memory for the returned data.</span></span>

-   <span data-ttu-id="a84c8-133">Wenn der Client eine Teilmenge eines großen konformen Arrays an den Server senden möchte, kann die Anwendung die Größe der Teilmenge angeben, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="a84c8-133">If the client wants to send a subset of a large conformant array to the server, the application can specify the size of the subset as demonstrated in the following example:</span></span>

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    <span data-ttu-id="a84c8-134">Auf diese Weise überträgt RPC nur *llength* -Elemente des Arrays über das Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a84c8-134">This way RPC will only transmit *lLength* elements of the array across the wire.</span></span> <span data-ttu-id="a84c8-135">Diese Definition zwingt jedoch den RPC-Dienst, Arbeitsspeicher der Größe *LSIZE* auf der Serverseite zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a84c8-135">However, this definition forces the RPC service to allocate memory of size *lSize* on the server side.</span></span>

-   <span data-ttu-id="a84c8-136">Wenn die Client Anwendungs Komponente die maximale Größe eines Arrays bestimmt, das vom Server zurückgegeben werden kann, aber der Server die Übertragung einer Teilmenge dieses Arrays ermöglicht, kann die Anwendung ein solches Verhalten angeben, indem die IDL ähnlich dem folgenden Beispiel definiert wird:</span><span class="sxs-lookup"><span data-stu-id="a84c8-136">If the client application component determines the maximum size of an array the server can return, but allows the server to transmit a subset of that array, the application can specify such a behavior by defining the IDL similar to the following example:</span></span>

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    <span data-ttu-id="a84c8-137">Die Client Anwendungs Komponente gibt die maximale Größe des Arrays an, und der Server gibt an, wie viele Elemente zurück an den Client übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="a84c8-137">The client application component specifies the maximum size of the array, and the server specifies how many elements it transmits back to the client.</span></span>

-   <span data-ttu-id="a84c8-138">Wenn die Server Anwendungs Komponente eine Zeichenfolge an die Client Anwendungs Komponente zurückgeben muss und der Client die maximale Größe kennt, die vom Server zurückgegeben werden soll, kann die Anwendung wie im folgenden Beispiel gezeigt einen konformen Zeichen Folgentyp verwenden:</span><span class="sxs-lookup"><span data-stu-id="a84c8-138">If the server application component needs to return a string to the client application component, and if the client knows the maximum size to be returned from the server, the application can use a conformant string type as demonstrated in the following example:</span></span>

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   <span data-ttu-id="a84c8-139">Wenn die Client Anwendungs Komponente die Größe der Zeichenfolge nicht steuern soll, kann der RPC-Dienst den Arbeitsspeicher explizit zuordnen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="a84c8-139">If the client application component should not control the size of the string, the RPC service can specifically allocate the memory as demonstrated in the following example:</span></span>

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    <span data-ttu-id="a84c8-140">Beim Aufrufen der RPC-Methode muss bei der Client Anwendungs Komponente *ppstr* auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a84c8-140">The client application component must set *ppStr* to **NULL** on when calling the RPC method.</span></span>

 

 




