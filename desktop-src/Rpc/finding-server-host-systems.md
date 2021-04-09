---
title: Auffinden von Server Host Systemen
description: Auffinden von Server Hostsystemen mithilfe von Zeichen folgen Bindungen und durch Abfragen einer Name Service-Datenbank für den Speicherort eines Server Programms.
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2357fcafa35d4f64cfb4f6841c0b56e1e94b7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856299"
---
# <a name="finding-server-host-systems"></a><span data-ttu-id="affbe-103">Auffinden von Server Host Systemen</span><span class="sxs-lookup"><span data-stu-id="affbe-103">Finding Server Host Systems</span></span>

<span data-ttu-id="affbe-104">Bei einem Server Host System handelt es sich um den Computer, auf dem das Serverprogramm der verteilten Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="affbe-104">A server host system is the computer that executes the distributed application's server program.</span></span> <span data-ttu-id="affbe-105">Es gibt möglicherweise ein oder mehrere Server Host Systeme in einem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="affbe-105">There may be one or many server host systems on a network.</span></span> <span data-ttu-id="affbe-106">Wie das Client Programm einen Server findet, zu dem eine Verbindung hergestellt werden soll, hängt von den Anforderungen des Programms ab.</span><span class="sxs-lookup"><span data-stu-id="affbe-106">How your client program finds a server to connect to depends on the needs of your program.</span></span>

<span data-ttu-id="affbe-107">Es gibt zwei Methoden zum Auffinden von Server Hostsystemen:</span><span class="sxs-lookup"><span data-stu-id="affbe-107">There are two methods of finding server host systems:</span></span>

-   <span data-ttu-id="affbe-108">Verwendung von Informationen, die in Zeichen folgen im Client Quellcode, in Umgebungsvariablen oder in anwendungsspezifischen Konfigurationsdateien gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="affbe-108">Using information stored in strings in the client source code, environment variables, or application-specific configuration files.</span></span> <span data-ttu-id="affbe-109">Die Client Anwendung kann die Daten in der Zeichenfolge verwenden, um eine Bindung zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="affbe-109">Your client application can use the data in the string to compose a binding between the client and the server.</span></span>
-   <span data-ttu-id="affbe-110">Abfragen einer Name Service-Datenbank für den Speicherort eines Server Programms.</span><span class="sxs-lookup"><span data-stu-id="affbe-110">Querying a name service database for the location of a server program.</span></span>

<span data-ttu-id="affbe-111">Dieser Abschnitt enthält Informationen zu diesen beiden Techniken in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="affbe-111">This section presents information on both of these techniques in the following topics:</span></span>

-   [<span data-ttu-id="affbe-112">Verwenden von Zeichen folgen Bindungen</span><span class="sxs-lookup"><span data-stu-id="affbe-112">Using String Bindings</span></span>](#using-string-bindings)
-   [<span data-ttu-id="affbe-113">Importieren aus Name Service-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="affbe-113">Importing from Name Service Databases</span></span>](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a><span data-ttu-id="affbe-114">Verwenden von Zeichen folgen Bindungen</span><span class="sxs-lookup"><span data-stu-id="affbe-114">Using String Bindings</span></span>

<span data-ttu-id="affbe-115">Anwendungen können Bindungen aus Informationen erstellen, die in Zeichen folgen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="affbe-115">Applications can create bindings from information stored in strings.</span></span> <span data-ttu-id="affbe-116">Ihre Client Anwendung verfasst diese Informationen als Zeichenfolge und ruft dann die [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="affbe-116">Your client application composes this information as a string, then calls the [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) function.</span></span> <span data-ttu-id="affbe-117">Der Client muss die folgenden Informationen bereitstellen, um den Server zu identifizieren:</span><span class="sxs-lookup"><span data-stu-id="affbe-117">The client must supply the following information to identify the server:</span></span>

-   <span data-ttu-id="affbe-118">Der Schnittstellen Name, der Globally Unique Identifier (GUID) des Objekts oder die UUID des Objekts.</span><span class="sxs-lookup"><span data-stu-id="affbe-118">The interface name, the globally unique identifier (GUID) of the object, or UUID of the object.</span></span> <span data-ttu-id="affbe-119">Weitere Informationen finden Sie unter [generierende Schnittstelle UUIDs](generating-interface-uuids.md) und [Zeichenfolge UUID](string-uuid.md).</span><span class="sxs-lookup"><span data-stu-id="affbe-119">For more information, see [Generating Interface UUIDs](generating-interface-uuids.md) and [String UUID](string-uuid.md).</span></span>
-   <span data-ttu-id="affbe-120">Der Transporttyp, über den kommuniziert werden soll, z. b. Named Pipes oder TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="affbe-120">The transport type to communicate over, such as named pipes or TCP/IP.</span></span> <span data-ttu-id="affbe-121">Weitere Informationen finden Sie unter [wichtige RPC-Bindungs Begriffe](essential-rpc-binding-terminology.md) und [Auswählen einer Protokoll Sequenz](selecting-a-protocol-sequence.md).</span><span class="sxs-lookup"><span data-stu-id="affbe-121">For details, see [Essential RPC Binding Terminology](essential-rpc-binding-terminology.md) and [Selecting a Protocol Sequence](selecting-a-protocol-sequence.md).</span></span>
-   <span data-ttu-id="affbe-122">Die Netzwerkadresse oder der Name des Server Host Computers.</span><span class="sxs-lookup"><span data-stu-id="affbe-122">The network address or the name of the server host computer.</span></span>
-   <span data-ttu-id="affbe-123">Der Endpunkt des Server Programms auf dem Server Host Computer.</span><span class="sxs-lookup"><span data-stu-id="affbe-123">The endpoint of the server program on the server host computer.</span></span> <span data-ttu-id="affbe-124">Weitere Informationen finden Sie untersuchen von [Endpunkten](finding-endpoints.md)und [Angeben von Endpunkten](specifying-endpoints.md).</span><span class="sxs-lookup"><span data-stu-id="affbe-124">For more information, see [Finding Endpoints](finding-endpoints.md), and [Specifying Endpoints](specifying-endpoints.md).</span></span>

<span data-ttu-id="affbe-125">(Die Objekt-UUID und die Endpunkt Informationen sind optional.)</span><span class="sxs-lookup"><span data-stu-id="affbe-125">(The object UUID and the endpoint information are optional.)</span></span>

<span data-ttu-id="affbe-126">In den folgenden Beispielen enthalten der *psznetworkaddress* -Parameter und andere Parameter eingebettete umgekehrte Schrägstriche.</span><span class="sxs-lookup"><span data-stu-id="affbe-126">In the following examples, the *pszNetworkAddress* parameter and other parameters include embedded backslashes.</span></span> <span data-ttu-id="affbe-127">Der umgekehrte Schrägstrich ist ein Escapezeichen in der Programmiersprache C.</span><span class="sxs-lookup"><span data-stu-id="affbe-127">The backslash is an escape character in the C programming language.</span></span> <span data-ttu-id="affbe-128">Zwei umgekehrte Schrägstriche sind erforderlich, um jeden einzelnen literalen umgekehrten Schrägstrich darzustellen.</span><span class="sxs-lookup"><span data-stu-id="affbe-128">Two backslashes are needed to represent each single literal backslash character.</span></span> <span data-ttu-id="affbe-129">Die Zeichen folgen Bindungsstruktur muss vier umgekehrte Schrägstriche enthalten, um die beiden literalen umgekehrten Schrägstriche zu repräsentieren, die dem Servernamen vorangestellt sind.</span><span class="sxs-lookup"><span data-stu-id="affbe-129">The string-binding structure must contain four backslash characters to represent the two literal backslash characters that precede the server name.</span></span>

<span data-ttu-id="affbe-130">Das folgende Beispiel zeigt, dass dem Servernamen acht umgekehrte Schrägstriche vorangestellt werden müssen, damit vier literale umgekehrte Schrägstriche in der Datenstruktur für die Zeichen folgen Bindung angezeigt werden, nachdem die **sprintf \_ s** -Funktion die Zeichenfolge verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="affbe-130">The following example shows that the server name must be preceded by eight backslashes so that four literal backslash characters will appear in the string-binding data structure after the **sprintf\_s** function processes the string.</span></span>


```C++
/* client application */

char * pszUuid = "6B29FC40-CA47-1067-B31D-00DD010662DA";
char * pszProtocol = "ncacn_np";
char * pszNetworkAddress = "\\\\\\\\servername";
char * pszEndpoint = "\\\\pipe\\\\pipename";
char * pszString;
 
int len = 0;
 
len  = sprintf_s(pszString, strlen(pszUuid), "%s", pszUuid);
len += sprintf_s(pszString + len, strlen(pszProtocolSequence) + 2, "@%s:",
    pszProtocolSequence);
if (pszNetworkAddress != NULL)
    len += sprintf_s(pszString + len, strlen(pszNetworkAddress), "%s",
    pszNetworkAddress);
len += sprintf_s(pszString + len, strlen(pszEndpoint) + 2, "[%s]", pszEndpoint);
```



<span data-ttu-id="affbe-131">Im folgenden Beispiel wird die Zeichen folgen Bindung folgendermaßen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="affbe-131">In the following example, the string binding appears as:</span></span>

<span data-ttu-id="affbe-132">6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_NP: \\ \\ \\ \\ *Servername* \[ \\ \\ Pipe \\ \\ *Pipename*\]</span><span class="sxs-lookup"><span data-stu-id="affbe-132">6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_np:\\\\\\\\*servername*\[\\\\pipe\\\\*pipename*\]</span></span>

<span data-ttu-id="affbe-133">Der Client ruft dann [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) auf, um das Bindungs Handle abzurufen:</span><span class="sxs-lookup"><span data-stu-id="affbe-133">The client then calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to obtain the binding handle:</span></span>


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



<span data-ttu-id="affbe-134">Eine Hilfsfunktion, [**rpcstringbindingcompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) , assembliert das Objekt UUID, die Protokoll Sequenz, die Netzwerkadresse und den Endpunkt in der korrekten Syntax für den Aufrufen von [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).</span><span class="sxs-lookup"><span data-stu-id="affbe-134">A convenience function, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) assembles the object UUID, protocol sequence, network address, and endpoint in the correct syntax for the call to [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).</span></span> <span data-ttu-id="affbe-135">Sie müssen sich keine Gedanken darüber machen, wie Sie das kaufmännische und-Doppelpunkte sowie die verschiedenen Komponenten für jede Protokoll Sequenz an der richtigen Stelle platzieren. die Zeichen folgen werden lediglich als Parameter für die Funktion bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="affbe-135">You do not have to worry about putting the ampersand, colon, and the various components for each protocol sequence in the right place; you just supply the strings as parameters to the function.</span></span> <span data-ttu-id="affbe-136">Die Lauf Zeit Bibliothek weist sogar den für die Zeichen folgen Bindung benötigten Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="affbe-136">The run-time library even allocates the memory needed for the string binding.</span></span>


```C++
char * pszNetworkAddress = "\\\\server";
char * pszEndpoint = "\\pipe\\pipename";
status = RpcStringBindingCompose(
            pszUuid,
            pszProtocolSequence,
            pszNetworkAddress,
            pszEndpoint,
            pszOptions,
            &pszString);
//...
status = RpcBindingFromStringBinding(
            pszString,
            &hBinding);
//...
```



<span data-ttu-id="affbe-137">Eine andere Hilfsfunktion, [**rpcbindingtostringbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), übernimmt ein Bindungs Handle als Eingabe und erzeugt die entsprechende Zeichen folgen Bindung.</span><span class="sxs-lookup"><span data-stu-id="affbe-137">Another convenience function, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), takes a binding handle as input and produces the corresponding string binding.</span></span>

## <a name="importing-from-name-service-databases"></a><span data-ttu-id="affbe-138">Importieren aus Name Service-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="affbe-138">Importing from Name Service Databases</span></span>

<span data-ttu-id="affbe-139">Name Dienst Datenbanken speichern unter anderem Bindungs Handles und UUIDs.</span><span class="sxs-lookup"><span data-stu-id="affbe-139">Name service databases store, among other things, binding handles and UUIDs.</span></span> <span data-ttu-id="affbe-140">Die Client Anwendung kann nach einer oder beiden von Ihnen suchen, wenn Sie an den Server gebunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="affbe-140">Your client application can search for either or both of these when it needs to bind to the server.</span></span> <span data-ttu-id="affbe-141">Eine Erläuterung der Informationen, die von einem Namensdienst gespeichert werden, und des Speicher Formats finden Sie [unter RPC Name Service Database](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="affbe-141">For a discussion of the information that a name service stores, and the storage format, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

<span data-ttu-id="affbe-142">Die RPC-Bibliothek stellt zwei Funktions Sätze bereit, mit denen das Client Programm die Name Service-Datenbank durchsuchen kann.</span><span class="sxs-lookup"><span data-stu-id="affbe-142">The RPC library provides two sets of functions that your client program can use to search the name service database.</span></span> <span data-ttu-id="affbe-143">Die Namen eines Satzes beginnen mit rpcnsbindingimport.</span><span class="sxs-lookup"><span data-stu-id="affbe-143">The names of one set begin with RpcNsBindingImport.</span></span> <span data-ttu-id="affbe-144">Die Namen der anderen Gruppe beginnen mit rpcnsbindinglookup.</span><span class="sxs-lookup"><span data-stu-id="affbe-144">The names of the other set begin with RpcNsBindingLookup.</span></span> <span data-ttu-id="affbe-145">Der Unterschied zwischen den beiden Gruppen von Funktionen besteht darin, dass die rpcnsbindingimport-Funktionen ein einzelnes Bindungs handle pro Rückruf zurückgeben und die rpcnsbindinglookup-Funktionen Gruppen von Handles pro Rückruf zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="affbe-145">The difference between the two groups of functions is that the RpcNsBindingImport functions return a single binding handle per call and the RpcNsBindingLookup functions return groups of handles per call.</span></span>

<span data-ttu-id="affbe-146">Um eine Suche mit den rpcnsbindingimport-Funktionen zu starten, müssen Sie zuerst [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)aufrufen, wie im folgenden Code Fragment gezeigt.</span><span class="sxs-lookup"><span data-stu-id="affbe-146">To begin a search with the RpcNsBindingImport functions, first call [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), as shown in the following code fragment.</span></span>


```C++
RPC_STATUS status;
RPC_NS_HANDLE hNameServiceHandle;
 
status = RpcNsBindingImportBegin(
    RPC_C_NS_SYNTAX_DEFAULT,
    NULL,
    MyInterface_v1_0_c_ifspec,
    NULL,
    &hNameServiceHandle);
```



<span data-ttu-id="affbe-147">Wenn die RPC-Funktionen die Name Service-Datenbank durchsuchen, benötigen Sie einen Platz, um die Suche zu starten.</span><span class="sxs-lookup"><span data-stu-id="affbe-147">When the RPC functions search the name service database, they need a place to begin the search.</span></span> <span data-ttu-id="affbe-148">In der RPC-Terminologie wird dies als Eintrags Name bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="affbe-148">In RPC terminology, this is called the entry name.</span></span> <span data-ttu-id="affbe-149">Das Client Programm übergibt den Namen des Eintrags als zweiten Parameter an [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="affbe-149">Your client program passes the entry name as the second parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="affbe-150">Dieser Parameter kann **null** sein, wenn Sie die gesamte Name Service-Datenbank durchsuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="affbe-150">This parameter can be **NULL** if you want to search the entire name service database.</span></span> <span data-ttu-id="affbe-151">Alternativ können Sie den Server Eintrag durchsuchen, indem Sie einen Server Eintrags Namen übergeben oder den Gruppen Eintrag durchsuchen, indem Sie einen Gruppen Eintrags Namen übergeben.</span><span class="sxs-lookup"><span data-stu-id="affbe-151">Alternatively, you can search the server entry by passing a server-entry name or search the group entry by passing a group-entry name.</span></span> <span data-ttu-id="affbe-152">Durch die Übergabe eines Eintrags namens wird die Suche auf den Inhalt dieses Eintrags beschränkt.</span><span class="sxs-lookup"><span data-stu-id="affbe-152">Passing an entry name restricts the search to the contents of that entry.</span></span>

<span data-ttu-id="affbe-153">Im vorherigen Beispiel wird der Wert RPC \_ C \_ NS- \_ Syntax \_ Default als erster Parameter an [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)übergeben.</span><span class="sxs-lookup"><span data-stu-id="affbe-153">In the preceding example, the value RPC\_C\_NS\_SYNTAX\_DEFAULT is passed as the first parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="affbe-154">Dadurch wird die standardmäßige Eingabe Namen Syntax ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="affbe-154">This selects the default entry name syntax.</span></span> <span data-ttu-id="affbe-155">Derzeit ist dies die einzige unterstützte Eingabe namens Syntax.</span><span class="sxs-lookup"><span data-stu-id="affbe-155">Currently, this is the only supported entry-name syntax.</span></span>

<span data-ttu-id="affbe-156">Die Client Anwendung kann die Name Service-Datenbank nach einem Schnittstellennamen, einer UUID oder beidem durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="affbe-156">Your client application can search the name service database for an interface name, a UUID, or both.</span></span> <span data-ttu-id="affbe-157">Wenn Sie eine Schnittstelle nach Namen suchen möchten, übergeben Sie die globale Schnittstellen Variable, die der mittlerer l-Compiler generiert, aus ihrer IDL-Datei als dritten Parameter an [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="affbe-157">If you want to have it search for an interface by name, pass the global interface variable that the MIDL compiler generates from your IDL file as the third parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="affbe-158">Sie finden die Deklaration in der Header Datei, die vom-compilercompiler beim Generieren des clientstubs generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="affbe-158">You'll find its declaration in the header file that the MIDL compiler generated when it generated the client stub.</span></span> <span data-ttu-id="affbe-159">Wenn das Client Programm nur nach UUID suchen soll, legen Sie den dritten Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="affbe-159">If you want your client program to search by UUID only, set the third parameter to **NULL**.</span></span>

<span data-ttu-id="affbe-160">Legen Sie beim Durchsuchen der Name Service-Datenbank nach einer UUID den vierten Parameter von [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) auf die UUID fest, nach der Sie suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="affbe-160">When searching the name service database for a UUID, set the fourth parameter of [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) to the UUID that you want to search for.</span></span> <span data-ttu-id="affbe-161">Wenn Sie nicht nach einer UUID suchen, legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="affbe-161">If you are not searching for a UUID, set this parameter to **NULL**.</span></span>

<span data-ttu-id="affbe-162">Die [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) -Funktion übergibt die Adresse eines Namensdienst – Such Kontext Handles über den fünften Parameter.</span><span class="sxs-lookup"><span data-stu-id="affbe-162">The [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) function passes the address of a name service–search context handle through its fifth parameter.</span></span> <span data-ttu-id="affbe-163">Sie übergeben diesen Parameter an andere rpcnsbindingimport-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="affbe-163">You pass this parameter to other RpcNsBindingImport functions.</span></span>

<span data-ttu-id="affbe-164">Die nächste Funktion, die von der Client Anwendung aufgerufen wird, ist " [**rpcnsbindingimportnext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)".</span><span class="sxs-lookup"><span data-stu-id="affbe-164">In particular, the next function your client application would call is [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span></span> <span data-ttu-id="affbe-165">Client Programme verwenden diese Funktion zum Abrufen kompatibler Bindungs Handles aus der Name Service-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="affbe-165">Client programs use this function to retrieve compatible binding handles from the name service database.</span></span> <span data-ttu-id="affbe-166">Das folgende Code Fragment veranschaulicht, wie diese Funktion aufgerufen werden kann:</span><span class="sxs-lookup"><span data-stu-id="affbe-166">The following code fragment demonstrates how this function might be called:</span></span>


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



<span data-ttu-id="affbe-167">Nachdem die Funktion [**rpcnsbindingimportnext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) zum Abrufen eines Bindungs Handles aufgerufen hat, kann Ihre Client Anwendung ermitteln, ob das empfangene handle akzeptabel ist.</span><span class="sxs-lookup"><span data-stu-id="affbe-167">Once it has called the [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) function to obtain a binding handle, your client application can determine if the handle it received is acceptable.</span></span> <span data-ttu-id="affbe-168">Andernfalls kann das Client Programm eine Schleife ausführen und **rpcnsbindingimportnext** erneut ausführen, um festzustellen, ob der Namensdienst ein geeignetere Handle enthält.</span><span class="sxs-lookup"><span data-stu-id="affbe-168">If not, your client program can execute a loop and call **RpcNsBindingImportNext** again to see if the name service contains a more appropriate handle.</span></span> <span data-ttu-id="affbe-169">Für jeden Aufrufen von **rpcnsbindingimportnext** muss ein entsprechender Aufrufen von rpcnsbindingfree vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="affbe-169">For each call to **RpcNsBindingImportNext**, there must be a corresponding call to RpcNsBindingFree.</span></span> <span data-ttu-id="affbe-170">Wenn die Suche abgeschlossen ist, können Sie die Funktion [**rpcnsbindingimportdone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) zum Freigeben des Such Kontexts abrufen.</span><span class="sxs-lookup"><span data-stu-id="affbe-170">When your search is complete, call the [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) function to free the lookup context.</span></span>

<span data-ttu-id="affbe-171">Nachdem die Client Anwendung über ein akzeptables Bindungs Handle verfügt, sollte Sie sicherstellen, dass die Serveranwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="affbe-171">After your client application has an acceptable binding handle, it should check to ensure that the server application is running.</span></span> <span data-ttu-id="affbe-172">Es gibt zwei Methoden, mit denen Ihr Client diese Überprüfung durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="affbe-172">There are two methods your client can use to perform this verification.</span></span> <span data-ttu-id="affbe-173">Der erste besteht darin, eine Funktion in der Client Schnittstelle aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="affbe-173">The first is to call a function in the client interface.</span></span> <span data-ttu-id="affbe-174">Wenn das Serverprogramm ausgeführt wird, wird der-Vorgang beendet.</span><span class="sxs-lookup"><span data-stu-id="affbe-174">If the server program is running, the call will complete.</span></span> <span data-ttu-id="affbe-175">Wenn dies nicht der Fall ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="affbe-175">If not, the call will fail.</span></span> <span data-ttu-id="affbe-176">Eine bessere Möglichkeit, um zu überprüfen, ob der Server ausgeführt wird, ist das Aufrufen von [**rpcepresolvebinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), gefolgt von einem Aufruf von [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening).</span><span class="sxs-lookup"><span data-stu-id="affbe-176">A better way to verify that the server is running is to invoke [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), followed by a call to [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening).</span></span> <span data-ttu-id="affbe-177">Weitere Informationen zur Name Service-Datenbank finden Sie [unter RPC Name Service Database](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="affbe-177">For more information on the name service database, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

 

 




