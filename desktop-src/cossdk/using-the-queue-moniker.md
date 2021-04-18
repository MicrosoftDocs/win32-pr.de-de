---
description: Der Warteschlangen-Moniker wird verwendet, um eine in der Warteschlange befindliche Komponente Programm gesteuert zu aktivieren.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Verwenden des Warteschlangen Monikers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228964157d08aca868474167ae16590692f16ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340123"
---
# <a name="using-the-queue-moniker"></a><span data-ttu-id="932a2-103">Verwenden des Warteschlangen Monikers</span><span class="sxs-lookup"><span data-stu-id="932a2-103">Using the Queue Moniker</span></span>

<span data-ttu-id="932a2-104">Der Warteschlangen-Moniker wird verwendet, um eine in der Warteschlange befindliche Komponente Programm gesteuert zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="932a2-104">The queue moniker is used to activate a queued component programmatically.</span></span> <span data-ttu-id="932a2-105">Der warteschlangenmoniker erfordert, dass er die Klassen-ID (CLSID) des Objekts empfängt, das vom neuen Moniker direkt auf der rechten Seite aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="932a2-105">The queue moniker requires that it receive the class ID (CLSID) of the object to be invoked from the new moniker directly to the right of it.</span></span> <span data-ttu-id="932a2-106">Wenn das Präfix linksbündig ist, übergibt der neue Moniker die CLSID auf der linken Seite an den Moniker.</span><span class="sxs-lookup"><span data-stu-id="932a2-106">When left-prefixed, the new moniker passes the CLSID to the moniker to the left of it.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="932a2-107">Verwaltungs Tool für Komponenten Dienste</span><span class="sxs-lookup"><span data-stu-id="932a2-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="932a2-108">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="932a2-108">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="932a2-109">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="932a2-109">Visual Basic</span></span>

<span data-ttu-id="932a2-110">Der Anzeige Name-Parameter von GetObject ist "Queue:/New:", gefolgt von der Programm-ID oder der Zeichen folgen-Formular-GUID (mit oder ohne geschweifte Klammern) des Server Objekts, das instanziiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="932a2-110">The GetObject display name parameter is "queue:/new:", followed by the program ID or string-form GUID, with or without braces, of the server object to be instantiated.</span></span> <span data-ttu-id="932a2-111">Die folgenden Beispiele zeigen drei gültige Aktivierungen einer Komponente mit dem warteschlangenmoniker:</span><span class="sxs-lookup"><span data-stu-id="932a2-111">The following examples show three valid activations of a component with the queue moniker:</span></span>

1.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:QCShip.Ship")
    ```

2.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}")
    ```

3.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE")
    ```

## <a name="cc"></a><span data-ttu-id="932a2-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="932a2-112">C/C++</span></span>

<span data-ttu-id="932a2-113">Der Name des [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) -Anzeige namens lautet "Queue:/New:", gefolgt von der Programm-ID oder der Zeichen folgen Formular-GUID mit oder ohne geschweifte Klammern des zu instanzigenden Server Objekts.</span><span class="sxs-lookup"><span data-stu-id="932a2-113">The [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) display name parameter is "queue:/new:", followed by the program ID or string-form GUID, with or without braces, of the server object to be instantiated.</span></span> <span data-ttu-id="932a2-114">Die folgenden Beispiele zeigen drei gültige Aktivierungen einer Komponente mit dem warteschlangenmoniker:</span><span class="sxs-lookup"><span data-stu-id="932a2-114">The following examples show three valid activations of a component with the queue moniker:</span></span>

1.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:QCShip.Ship",
      NULL, IID_IShip, (void**)&pShip);
    ```

2.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}", 
      NULL, IID_IShip, (void**)&pShip);
    ```

3.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE",
      NULL, IID_IShip, (void**)&pShip);
    ```

## <a name="remarks"></a><span data-ttu-id="932a2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="932a2-115">Remarks</span></span>

<span data-ttu-id="932a2-116">Der warteschlangenmoniker akzeptiert optionale Parameter, die die Eigenschaften der an Message Queuing gesendeten Nachricht ändern.</span><span class="sxs-lookup"><span data-stu-id="932a2-116">The queue moniker accepts optional parameters that alter the properties of the message sent to Message Queuing.</span></span> <span data-ttu-id="932a2-117">Um z. b. die Message Queuing Nachricht mit der Priorität 6 zu senden, wird die in der Warteschlange befindliche Komponente wie folgt aktiviert:</span><span class="sxs-lookup"><span data-stu-id="932a2-117">For example, to cause the Message Queuing message to be sent with a priority 6, the queued component would be activated as follows:</span></span>

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

<span data-ttu-id="932a2-118">In der folgenden Tabelle sind die Warteschlangen-monikerparameter aufgeführt, die die Ziel Warteschlange betreffen.</span><span class="sxs-lookup"><span data-stu-id="932a2-118">The following table lists the queue moniker parameters that affect the destination queue.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="932a2-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="932a2-119">Parameter</span></span></th>
<th><span data-ttu-id="932a2-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="932a2-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="932a2-121"><em>Computername</em></span><span class="sxs-lookup"><span data-stu-id="932a2-121"><em>ComputerName</em></span></span><br/></td>
<td><span data-ttu-id="932a2-122">Gibt den Computernamen Teil eines Message Queuing Warteschlangen Pfadnamens an.</span><span class="sxs-lookup"><span data-stu-id="932a2-122">Specifies the computer name portion of a Message Queuing queue path name.</span></span> <span data-ttu-id="932a2-123">Der Name des Message Queuing Warteschlangen Pfads ist als <em>Computername</em> \ <em>QueueName</em>formatiert.</span><span class="sxs-lookup"><span data-stu-id="932a2-123">The Message Queuing queue path name is formatted as <em>ComputerName</em>\<em>QueueName</em>.</span></span> <span data-ttu-id="932a2-124">Wenn nichts angegeben ist, wird der Computername verwendet, der der konfigurierten Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="932a2-124">If not specified, the computer name associated with the configured application is used.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="932a2-125"><em>QueueName</em></span><span class="sxs-lookup"><span data-stu-id="932a2-125"><em>QueueName</em></span></span><br/></td>
<td><span data-ttu-id="932a2-126">Gibt den Namen der Message Queuing Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="932a2-126">Specifies the Message Queuing queue name.</span></span> <span data-ttu-id="932a2-127">Der Name des Message Queuing Warteschlangen Pfads ist als <em>Computername</em> \ <em>QueueName</em>formatiert.</span><span class="sxs-lookup"><span data-stu-id="932a2-127">The Message Queuing queue path name is formatted as <em>ComputerName</em>\<em>QueueName</em>.</span></span> <span data-ttu-id="932a2-128">Wenn nicht angegeben, wird der der konfigurierten Anwendung zugeordnete Warteschlangen Name verwendet.</span><span class="sxs-lookup"><span data-stu-id="932a2-128">If not specified, the queue name associated with the configured application is used.</span></span><br/> <span data-ttu-id="932a2-129">Um eine nicht transaktionale Warteschlange zu erhalten, können Sie zuerst den Warteschlangen Namen angeben und dann eine COM+-Anwendung mit demselben Namen erstellen.</span><span class="sxs-lookup"><span data-stu-id="932a2-129">To get a non-transactional queue, you can specify the queue name first and then create a COM+ application of the same name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="932a2-130"><em>PathName</em></span><span class="sxs-lookup"><span data-stu-id="932a2-130"><em>PathName</em></span></span><br/></td>
<td><span data-ttu-id="932a2-131">Gibt den Namen des gesamten Message Queuing Warteschlangen Pfads an.</span><span class="sxs-lookup"><span data-stu-id="932a2-131">Specifies the complete Message Queuing queue path name.</span></span> <span data-ttu-id="932a2-132">Wenn nichts angegeben ist, wird der Message Queuing der konfigurierten Anwendung zugeordnete Warteschlangen Pfadname verwendet.</span><span class="sxs-lookup"><span data-stu-id="932a2-132">If not specified, the Message Queuing queue path name associated with the configured application is used.</span></span> <span data-ttu-id="932a2-133">Um den Zielnamen zu überschreiben, kann der Pfad für eine Message Queuing Arbeitsgruppe-Installation im folgenden Format angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="932a2-133">To override the destination name, the path can be specified in the following form for a Message Queuing workgroup installation:</span></span><br/> <span data-ttu-id="932a2-134">Queue:<em>Pfadname</em> = <em>Computername</em>\Private $ \ appname/New: MyProject. CMyClass</span><span class="sxs-lookup"><span data-stu-id="932a2-134">Queue:<em>PathName</em>=<em>ComputerName</em>\PRIVATE$\AppName/new:Myproject.CMyClass</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="932a2-135">Sowohl die Programmiersprachen C als auch Microsoft Visual C++ erfordern zwei umgekehrte Schrägstriche zur Darstellung eines umgekehrten Schrägstrichs in Zeichenfolgenliteralen, z. b. in Chicago- \\ Gehalts</span><span class="sxs-lookup"><span data-stu-id="932a2-135">Both the C and Microsoft Visual C++ programming languages require two backslashes to represent one backslash within string literals for example, chicago\\payroll.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="932a2-136"><em>Format Name</em></span><span class="sxs-lookup"><span data-stu-id="932a2-136"><em>FormatName</em></span></span><br/></td>
<td><span data-ttu-id="932a2-137">Wenn Sie eine COM+-Anwendung als in die Warteschlange eingereiht markieren, erstellt com+ eine Message Queuing Warteschlange, deren Name mit der Anwendung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="932a2-137">When you mark a COM+ application as queued, COM+ creates a Message Queuing queue whose name is the same as the application.</span></span> <span data-ttu-id="932a2-138">Der Message Queuing Formatname dieser Warteschlange befindet sich im com+-Katalog, der der com+-Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="932a2-138">The Message Queuing format name of that queue is in the COM+ catalog, associated with the COM+ application.</span></span> <span data-ttu-id="932a2-139">Um den Zielnamen zu überschreiben, kann der Format Name in der folgenden Form für eine Message Queuing Arbeitsgruppe-Installation angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="932a2-139">To override the destination name, the format name can be specified in the following form for a Message Queuing workgroup installation:</span></span><br/> <span data-ttu-id="932a2-140">Queue:<em>Format Name</em>= Direct = OS:<em>Computername</em>\Private $ \ appname/New: ProgID</span><span class="sxs-lookup"><span data-stu-id="932a2-140">Queue:<em>FormatName</em>=DIRECT=OS:<em>ComputerName</em>\PRIVATE$\AppName/new:ProgId</span></span><br/> <span data-ttu-id="932a2-141">In einer Active Directory Konfiguration &quot; wird private $ &quot; nicht als Teil des Warteschlangen namens angegeben.</span><span class="sxs-lookup"><span data-stu-id="932a2-141">In an Active Directory configuration, &quot;PRIVATE$&quot; is not specified as part of the queue name.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="932a2-142">Optionale Warteschlangen-monikerparameter werden von links nach rechts verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="932a2-142">Optional queue moniker parameters are processed left-to-right.</span></span> <span data-ttu-id="932a2-143">Geben Sie jedes Schlüsselwort nur einmal an.</span><span class="sxs-lookup"><span data-stu-id="932a2-143">Specify each keyword only one time.</span></span> <span data-ttu-id="932a2-144">Wenn Sie den *pathname* -Parameter angeben, werden die Parameter *Computername* und *QueueName* ersetzt.</span><span class="sxs-lookup"><span data-stu-id="932a2-144">Specifying the *PathName* parameter replaces both the *ComputerName* and *QueueName* parameters.</span></span> <span data-ttu-id="932a2-145">Ein bestimmter *Formatname* -Parameter löscht vorherige Kenntnisse zu den Parametern " *Computername*", " *QueueName*" und " *pathname* ".</span><span class="sxs-lookup"><span data-stu-id="932a2-145">A specific *FormatName* parameter deletes prior knowledge of a *ComputerName*, *QueueName*, and *PathName* parameter.</span></span>

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a><span data-ttu-id="932a2-146">Zuordnen der in der Warteschlange befindlichen Komponenten Listener zu einer bestimmten privaten Warteschlange</span><span class="sxs-lookup"><span data-stu-id="932a2-146">Associating the Queued Components Listener with a Specific Private Queue</span></span>

<span data-ttu-id="932a2-147">Der von com+ in der Warteschlange befindliche Komponenten Listener empfängt nur aus Warteschlangen, die der com+-Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="932a2-147">The COM+ Queued Components listener receives only from queues associated with the COM+ application marked queued.</span></span> <span data-ttu-id="932a2-148">Wenn Sie eine COM+-Anwendung als in die Warteschlange eingereiht markieren, erstellt com+ eine Message Queuing Warteschlange, deren Name mit der Anwendung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="932a2-148">When you mark a COM+ application as queued, COM+ creates a Message Queuing queue whose name is the same as the application.</span></span> <span data-ttu-id="932a2-149">Der Message Queuing Formatname dieser Warteschlange befindet sich im com+-Katalog, der der com+-Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="932a2-149">The Message Queuing format name of that queue is in the COM+ catalog, associated with the COM+ application.</span></span> <span data-ttu-id="932a2-150">Wenn die COM+-Anwendung gestartet und als lauschen gekennzeichnet ist, wird ein Listener im com+-Anwendungsprozess gestartet und die Warteschlange geöffnet.</span><span class="sxs-lookup"><span data-stu-id="932a2-150">When the COM+ application is started and marked as listen, a listener in the COM+ application process is started and the queue is opened.</span></span> <span data-ttu-id="932a2-151">In der folgenden Tabelle sind die Warteschlangen-monikerparameter aufgeführt, die sich auf die Message Queuing Meldung auswirken.</span><span class="sxs-lookup"><span data-stu-id="932a2-151">The following table lists the queue moniker parameters that affect the Message Queuing message.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="932a2-152">Parameter</span><span class="sxs-lookup"><span data-stu-id="932a2-152">Parameter</span></span></th>
<th><span data-ttu-id="932a2-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="932a2-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="932a2-154"><em>AppSpecific</em></span><span class="sxs-lookup"><span data-stu-id="932a2-154"><em>AppSpecific</em></span></span><br/></td>
<td><span data-ttu-id="932a2-155">Gibt eine ganze Zahl ohne Vorzeichen an, z. b. AppSpecific = 12345.</span><span class="sxs-lookup"><span data-stu-id="932a2-155">Specifies an unsigned integer for example, AppSpecific=12345.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="932a2-156"><em>AuthLevel</em></span><span class="sxs-lookup"><span data-stu-id="932a2-156"><em>AuthLevel</em></span></span><br/></td>
<td><span data-ttu-id="932a2-157">Gibt die Authentifizierungs Ebene der Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="932a2-157">Specifies the message authentication level.</span></span> <span data-ttu-id="932a2-158">Eine authentifizierte Nachricht ist digital signiert und erfordert ein Zertifikat für den Benutzer, der die Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="932a2-158">An authenticated message is digitally signed and requires a certificate for the user sending the message.</span></span> <span data-ttu-id="932a2-159">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="932a2-159">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="932a2-160">MQMSG_AUTH_LEVEL_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="932a2-160">MQMSG_AUTH_LEVEL_NONE,0</span></span></li>
<li><span data-ttu-id="932a2-161">MQMSG_AUTH_LEVEL_ALWAYS, 1</span><span class="sxs-lookup"><span data-stu-id="932a2-161">MQMSG_AUTH_LEVEL_ALWAYS,1</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="932a2-162"><em>Bereitstellung</em></span><span class="sxs-lookup"><span data-stu-id="932a2-162"><em>Delivery</em></span></span><br/></td>
<td><span data-ttu-id="932a2-163">Gibt die Option für die Nachrichtenübermittlung an.</span><span class="sxs-lookup"><span data-stu-id="932a2-163">Specifies the message delivery option.</span></span> <span data-ttu-id="932a2-164">Dieser Wert wird bei transaktionalen Warteschlangen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="932a2-164">This value is ignored for transactional queues.</span></span> <span data-ttu-id="932a2-165">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="932a2-165">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="932a2-166">MQMSG_DELIVERY_EXPRESS, 0</span><span class="sxs-lookup"><span data-stu-id="932a2-166">MQMSG_DELIVERY_EXPRESS,0</span></span></li>
<li><span data-ttu-id="932a2-167">MQMSG_DELIVERY_RECOVERABLE, 1</span><span class="sxs-lookup"><span data-stu-id="932a2-167">MQMSG_DELIVERY_RECOVERABLE,1</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="932a2-168"><em>Verschlüsselungs THM</em></span><span class="sxs-lookup"><span data-stu-id="932a2-168"><em>EncryptAlgorithm</em></span></span><br/></td>
<td><span data-ttu-id="932a2-169">Gibt den Verschlüsselungsalgorithmus an, der von Message Queuing zum Verschlüsseln und Entschlüsseln der Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="932a2-169">Specifies the encryption algorithm to be used by Message Queuing to encrypt and decrypt the message.</span></span> <span data-ttu-id="932a2-170">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="932a2-170">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="932a2-171">CALG_RC2 CALG_RC4</span><span class="sxs-lookup"><span data-stu-id="932a2-171">CALG_RC2, CALG_RC4</span></span></li>
<li><span data-ttu-id="932a2-172">Ein beliebiger ganzzahliger Wert, der für die Message Queuing eines <em>Verschlüsselungsalgorithmus</em>zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="932a2-172">Any integer value that is acceptable to Message Queuing for an <em>EncryptAlgorithm</em>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="932a2-173"><em>HashAlgorithm</em></span><span class="sxs-lookup"><span data-stu-id="932a2-173"><em>HashAlgorithm</em></span></span><br/></td>
<td><span data-ttu-id="932a2-174">Gibt eine kryptografiehash-Funktion an.</span><span class="sxs-lookup"><span data-stu-id="932a2-174">Specifies a cryptographic hash function.</span></span> <span data-ttu-id="932a2-175">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="932a2-175">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="932a2-176">CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC</span><span class="sxs-lookup"><span data-stu-id="932a2-176">CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</span></span></li>
<li><span data-ttu-id="932a2-177">Jeder ganzzahlige Wert, der für die Message Queuing eines <em>HashAlgorithm</em>zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="932a2-177">Any integer value that is acceptable to Message Queuing for a <em>HashAlgorithm</em>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="932a2-178">Journal</span><span class="sxs-lookup"><span data-stu-id="932a2-178">Journal</span></span><br/></td>
<td><span data-ttu-id="932a2-179">Gibt die Message Queuing Nachrichtenjournal Option an.</span><span class="sxs-lookup"><span data-stu-id="932a2-179">Specifies the Message Queuing message journal option.</span></span> <span data-ttu-id="932a2-180">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="932a2-180">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="932a2-181">MQMSG_JOURNAL_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="932a2-181">MQMSG_JOURNAL_NONE,0</span></span></li>
<li><span data-ttu-id="932a2-182">MQMSG_DEADLETTER, 1</span><span class="sxs-lookup"><span data-stu-id="932a2-182">MQMSG_DEADLETTER,1</span></span></li>
<li><span data-ttu-id="932a2-183">MQMSG_JOURNAL, 2</span><span class="sxs-lookup"><span data-stu-id="932a2-183">MQMSG_JOURNAL,2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="932a2-184"><em>Label</em></span><span class="sxs-lookup"><span data-stu-id="932a2-184"><em>Label</em></span></span><br/></td>
<td><span data-ttu-id="932a2-185">Gibt eine Zeichenfolge für die Nachrichten Bezeichnung bis zu MQ_MAX_MSG_LABEL_LEN Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="932a2-185">Specifies a message label string up to MQ_MAX_MSG_LABEL_LEN characters.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="932a2-186"><em>Maxtimetoreachqueue</em></span><span class="sxs-lookup"><span data-stu-id="932a2-186"><em>MaxTimeToReachQueue</em></span></span><br/></td>
<td><span data-ttu-id="932a2-187">Gibt eine maximale Zeit in Sekunden an, die die Nachricht an die Warteschlange gelangt.</span><span class="sxs-lookup"><span data-stu-id="932a2-187">Specifies a maximum time, in seconds, for the message to reach the queue.</span></span> <br/> <span data-ttu-id="932a2-188">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="932a2-188">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="932a2-189">INFINITE</span><span class="sxs-lookup"><span data-stu-id="932a2-189">INFINITE</span></span></li>
<li><span data-ttu-id="932a2-190">LONG_LIVED</span><span class="sxs-lookup"><span data-stu-id="932a2-190">LONG_LIVED</span></span></li>
<li><span data-ttu-id="932a2-191">Anzahl von Sekunden</span><span class="sxs-lookup"><span data-stu-id="932a2-191">Number of seconds</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="932a2-192"><em>Maxtimetor eceive</em></span><span class="sxs-lookup"><span data-stu-id="932a2-192"><em>MaxTimeToReceive</em></span></span><br/></td>
<td><span data-ttu-id="932a2-193">Gibt eine maximale Zeit in Sekunden an, die die Nachricht von der Zielanwendung empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="932a2-193">Specifies a maximum time, in seconds, for the message to be received by the target application.</span></span> <span data-ttu-id="932a2-194">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="932a2-194">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="932a2-195">INFINITE</span><span class="sxs-lookup"><span data-stu-id="932a2-195">INFINITE</span></span></li>
<li><span data-ttu-id="932a2-196">LONG_LIVED</span><span class="sxs-lookup"><span data-stu-id="932a2-196">LONG_LIVED</span></span></li>
<li><span data-ttu-id="932a2-197">Anzahl von Sekunden</span><span class="sxs-lookup"><span data-stu-id="932a2-197">Number of seconds</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="932a2-198"><em>Priority</em></span><span class="sxs-lookup"><span data-stu-id="932a2-198"><em>Priority</em></span></span><br/></td>
<td><span data-ttu-id="932a2-199">Gibt die Prioritäts Ebene der Nachricht innerhalb der zulässigen Message Queuing Werte an.</span><span class="sxs-lookup"><span data-stu-id="932a2-199">Specifies a message priority level, within the Message Queuing values permitted.</span></span><br/> <span data-ttu-id="932a2-200">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="932a2-200">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="932a2-201">MQ_MIN_PRIORITY, 0</span><span class="sxs-lookup"><span data-stu-id="932a2-201">MQ_MIN_PRIORITY,0</span></span></li>
<li><span data-ttu-id="932a2-202">MQ_MAX_PRIORITY, 7</span><span class="sxs-lookup"><span data-stu-id="932a2-202">MQ_MAX_PRIORITY,7</span></span></li>
<li><span data-ttu-id="932a2-203">MQ_DEFAULT_PRIORITY, 3</span><span class="sxs-lookup"><span data-stu-id="932a2-203">MQ_DEFAULT_PRIORITY,3</span></span></li>
<li><span data-ttu-id="932a2-204">Zahl zwischen 0 und 7</span><span class="sxs-lookup"><span data-stu-id="932a2-204">Number between 0 and 7</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="932a2-205"><em>PrivLevel</em></span><span class="sxs-lookup"><span data-stu-id="932a2-205"><em>PrivLevel</em></span></span><br/></td>
<td><span data-ttu-id="932a2-206">Gibt eine Sicherheitsebene an, die zum Verschlüsseln von Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="932a2-206">Specifies a privacy level, used to encrypt messages.</span></span><br/> <span data-ttu-id="932a2-207">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="932a2-207">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="932a2-208">MQMSG_PRIV_LEVEL_NONE, keine, 0</span><span class="sxs-lookup"><span data-stu-id="932a2-208">MQMSG_PRIV_LEVEL_NONE, NONE, 0</span></span></li>
<li><span data-ttu-id="932a2-209">MQMSG_PRIV_LEVEL_BODY, Text,</span><span class="sxs-lookup"><span data-stu-id="932a2-209">MQMSG_PRIV_LEVEL_BODY, BODY,</span></span></li>
<li><span data-ttu-id="932a2-210">MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</span><span class="sxs-lookup"><span data-stu-id="932a2-210">MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</span></span></li>
<li><span data-ttu-id="932a2-211">MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</span><span class="sxs-lookup"><span data-stu-id="932a2-211">MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="932a2-212"><em>Ablaufverfolgung</em></span><span class="sxs-lookup"><span data-stu-id="932a2-212"><em>Trace</em></span></span><br/></td>
<td><span data-ttu-id="932a2-213">Gibt Ablauf Verfolgungs Optionen an, die beim Ablauf Verfolgungs Message Queuing Routing verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="932a2-213">Specifies trace options, used in tracing Message Queuing routing.</span></span><br/> <span data-ttu-id="932a2-214">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="932a2-214">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="932a2-215">MQMSG_TRACE_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="932a2-215">MQMSG_TRACE_NONE,0</span></span></li>
<li><span data-ttu-id="932a2-216">MQMSG_SEND_ROUTE_TO_REPORT_QUEUE, 1</span><span class="sxs-lookup"><span data-stu-id="932a2-216">MQMSG_SEND_ROUTE_TO_REPORT_QUEUE,1</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="932a2-217">Der gesamte Satz von com+-Verwaltungs-SDK-Funktionen ist mit COM-Objekten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="932a2-217">The complete set of COM+ Administrative SDK functions is available by using COM objects.</span></span> <span data-ttu-id="932a2-218">Dies ermöglicht es jedem Programm, com+-Anwendungen nach Bedarf zu starten und zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="932a2-218">This allows any program to start and stop COM+ applications as required.</span></span>

> [!Note]  
> <span data-ttu-id="932a2-219">Wenn eine COM+-Anwendung gestartet wird, ist dies die Anwendung, die ausgeführt wird, nicht die einzelnen Komponenten innerhalb der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="932a2-219">When a COM+ application is started, it is the application that is running, not the individual components within the application.</span></span> <span data-ttu-id="932a2-220">Wenn eine Anwendung eine Komponente, die keine Warteschlange enthält, aufruft, wird die COM+-Anwendung, die die Komponente enthält, gestartet.</span><span class="sxs-lookup"><span data-stu-id="932a2-220">If an application calls a non-queued component, the COM+ application that contains the component is started.</span></span> <span data-ttu-id="932a2-221">Wenn das Kontrollkästchen Listener aktiviert ist, beginnt der Listener auch mit der Verarbeitung von Nachrichten für in der Warteschlange befindliche Komponenten.</span><span class="sxs-lookup"><span data-stu-id="932a2-221">If the listener check box is enabled, the listener also starts and begins processing for messages for queued components.</span></span> <span data-ttu-id="932a2-222">Obwohl der Dienst für die Warteschlangen Dienste auf diese Weise gestartet werden kann, wenn Sie in einer COM+-Anwendung in der Warteschlange befindliche und nicht in die Warteschlange eingereihte Komponenten packen, sollten Sie sicherstellen, dass in der Warteschlange befindliche Komponenten gestartet werden, wenn eine nicht in der Warteschlange befindliche Komponente ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="932a2-222">While the queued components service can be started in this way, if you package queued and non-queued components into a single COM+ application, be sure that you really want queued components to start if a non-queued component is executed.</span></span> <span data-ttu-id="932a2-223">Wenn dies nicht der Fall ist, Verpacken Sie die in die Warteschlange eingereihten Komponenten in eine COM+-Anwendung, die von den anderen Komponenten getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="932a2-223">If this is not the case, package the queued components into a COM+ application that is separate from the other components.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="932a2-224">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="932a2-224">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="932a2-225">Komponenten Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="932a2-225">Activating Component Queues</span></span>](activating-component-queues.md)
</dt> </dl>

 

 




