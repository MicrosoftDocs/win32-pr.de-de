---
title: Verwalten von Sitzungsinformationen
description: Verwalten von Sitzungsinformationen
ms.assetid: 2ab862dc-62e1-44d6-ac81-7d3c574a779f
keywords:
- Windows Media Player Online Stores, Download-Manager
- Online Stores, Download-Manager
- Typ 2 Online Stores, Download-Manager
- Windows Media Player Online Stores, Verwalten von Sitzungsinformationen
- Online Stores, Verwalten von Sitzungsinformationen
- Typ 2 Online Stores, Verwaltung von Sitzungsinformationen
- Windows Media Player Online Stores, Sitzungsinformationen
- Online Stores, Sitzungsinformationen
- Typ 2 Online Stores, Sitzungsinformationen
- Windows Media Player, Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Verwalten von Sitzungsinformationen
- Sitzungsinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786892afebb26f64a97b300bd1a4bd7c46d44883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311538"
---
# <a name="maintaining-session-information"></a><span data-ttu-id="710eb-117">Verwalten von Sitzungsinformationen</span><span class="sxs-lookup"><span data-stu-id="710eb-117">Maintaining Session Information</span></span>

## <a name="how-the-sample-stores-information"></a><span data-ttu-id="710eb-118">Speichern von Informationen im Beispiel</span><span class="sxs-lookup"><span data-stu-id="710eb-118">How the Sample Stores Information</span></span>

<span data-ttu-id="710eb-119">Die Beispiel Webseite verwaltet Daten mithilfe von Cookies.</span><span class="sxs-lookup"><span data-stu-id="710eb-119">The sample webpage maintains data by using cookies.</span></span> <span data-ttu-id="710eb-120">Cookies sind einfach persistente Name/Wert-Paare, die der Webbrowser für Sie speichern kann.</span><span class="sxs-lookup"><span data-stu-id="710eb-120">Cookies are simply persistent name/value pairs that the Web browser can store for you.</span></span>

<span data-ttu-id="710eb-121">Wenn die Webseite geschlossen wird, wird die Funktion zum **herunter** fahren ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="710eb-121">When the webpage closes, the **Shutdown** function runs.</span></span> <span data-ttu-id="710eb-122">Beim **herunter** fahren wird die Funktion **setpdingcookies** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="710eb-122">**Shutdown** calls the function **SetPendingCookies**.</span></span> <span data-ttu-id="710eb-123">Diese Funktion durchläuft die Liste der Download Sammlungen, die im Dropdown-Listenfeld mit dem Namen seldlc gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="710eb-123">This function loops through the download collection list, stored in the drop-down list box named selDLC.</span></span> <span data-ttu-id="710eb-124">Wenn eine Download Auflistung unvollständige Elemente enthält, ruft die Funktion die Methode **setcookie** auf und übergibt dabei einen Namen und einen Wert.</span><span class="sxs-lookup"><span data-stu-id="710eb-124">If a download collection contains incomplete items, the function calls the method **SetCookie**, passing a name and a value.</span></span> <span data-ttu-id="710eb-125">Die namens Zeichenfolge wird festgelegt, indem ein ganzzahliger Wert an einen konstanten Wert ( **wmpdlc**) angehängt wird, der in der Variablen mit dem Namen g-Tabellenwert gespeichert wird \_ .</span><span class="sxs-lookup"><span data-stu-id="710eb-125">The name string is determined by appending an integer value to a constant value, **WMPDLC**, which is stored in the variable named g\_sPreCookie.</span></span> <span data-ttu-id="710eb-126">Der Cookiename für die dritte ausstehende Download Auflistung lautet beispielsweise "WMPDLC2", da der Zählmechanismus Null basiert ist.</span><span class="sxs-lookup"><span data-stu-id="710eb-126">For instance, for the third pending download collection, the cookie name would be "WMPDLC2", because the counting mechanism is zero-based.</span></span> <span data-ttu-id="710eb-127">Beim Erstellen jedes Cookies erhöht die Funktion die globale Variable g \_ Pending, um die Anzahl ausstehender Downloads beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="710eb-127">As each cookie is created, the function increments the global variable g\_Pending to keep a count of pending downloads.</span></span> <span data-ttu-id="710eb-128">Der Code wird hier zur einfacheren wiedergegeben:</span><span class="sxs-lookup"><span data-stu-id="710eb-128">The code is reproduced here for your convenience:</span></span>


```C++
// Write cookies for pending downloads.
function SetPendingCookies()
{
    g_Pending = 0; // Init the pending count.
    
    for(var i = 0; i < selDLC.length; i++)
    {
        var sCookieName = g_sPreCookie + i.toString(10);
        var sCookieVal = selDLC.options[i].text;
    
        // Write a cookie for each pending download.    
        if(IsDLCComplete(sCookieVal.valueOf()) == false)
        {      
            SetCookie(sCookieName, sCookieVal);
            g_Pending++;
        }        
    }
}

```



<span data-ttu-id="710eb-129">**Isdlccomplete** ist eine Hilfsfunktion, die einfach die einzelnen Download Elemente in der Download Auflistung durchläuft, um zu bestimmen, ob ein Element aussteht.</span><span class="sxs-lookup"><span data-stu-id="710eb-129">**IsDLCComplete** is a helper function that simply loops through each download item in the download collection to determine whether any item is pending.</span></span> <span data-ttu-id="710eb-130">Wenn es ein ausstehendes Element gibt, gibt die Funktion false zurück.</span><span class="sxs-lookup"><span data-stu-id="710eb-130">If there is a pending item, the function returns false.</span></span>

<span data-ttu-id="710eb-131">**Setcookie** ist die Funktion, die das Cookie erstellt.</span><span class="sxs-lookup"><span data-stu-id="710eb-131">**SetCookie** is the function that creates the cookie.</span></span>

<span data-ttu-id="710eb-132">Wenn **settzdingcookies** zurückgibt, erstellt **Shutdown** das count-Cookie, in dem der Wert aus der Variablen g Pending gespeichert wird \_ .</span><span class="sxs-lookup"><span data-stu-id="710eb-132">When **SetPendingCookies** returns, **Shutdown** creates the count cookie, which stores the value from the variable g\_Pending.</span></span> <span data-ttu-id="710eb-133">Dieser Wert ist wichtig, da die Webseite eine Möglichkeit benötigt, zu bestimmen, wie viele Cookies beim erneuten Laden abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="710eb-133">This value is important because the webpage needs a way to determine how many cookies to retrieve when it reloads.</span></span> <span data-ttu-id="710eb-134">Der Name des Anzahl Cookies wird in der Variablen mit dem Namen g \_ szählcookie gespeichert.</span><span class="sxs-lookup"><span data-stu-id="710eb-134">The count cookie name is stored in the variable named g\_sCountCookie.</span></span>

## <a name="how-the-sample-retrieves-information"></a><span data-ttu-id="710eb-135">Abrufen von Informationen durch das Beispiel</span><span class="sxs-lookup"><span data-stu-id="710eb-135">How the Sample Retrieves Information</span></span>

<span data-ttu-id="710eb-136">Wenn die Webseite geladen wird, wird die **Init** -Funktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="710eb-136">When the webpage loads, the **Init** function runs.</span></span> <span data-ttu-id="710eb-137">Zuerst Ruft die Funktion **gettzdingdlcount** auf, um das Anzahl Cookie abzurufen.</span><span class="sxs-lookup"><span data-stu-id="710eb-137">First, the function calls **GetPendingDlCount** to retrieve the count cookie.</span></span> <span data-ttu-id="710eb-138">Anschließend wird dieser Wert in der Variablen mit dem Namen g \_ Pending gespeichert.</span><span class="sxs-lookup"><span data-stu-id="710eb-138">Next, it stores this value in the variable named g\_Pending.</span></span> <span data-ttu-id="710eb-139">Anschließend wird die Funktion " **populatedllist** " aufgerufen, um jedes Download Sitzungs Cookie abzurufen und seinen Bezeichner dem Dropdown-Listenfeld hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="710eb-139">Then it calls the **PopulateDLList** function to retrieve each download session cookie and add its identifier to the drop-down list box.</span></span> <span data-ttu-id="710eb-140">Dies ist der Code für diese Funktion:</span><span class="sxs-lookup"><span data-stu-id="710eb-140">Here is the code for that function:</span></span>


```C++
// Fill the drop-down list with pending download collection IDs.
function PopulateDlList(iCount)
{
    ClearList(selDLC);
     
    // For each cookie, add the value to the SELECT element.
    // The value represents a download collection ID.  
    for (var j = 0; j < iCount; j++)
    {
        var sCookieName = g_sPreCookie + j.toString(10);        
        var sCookieVal = GetCookie(sCookieName);
        DelCookie(sCookieName); // Don't leave the cookies lying around. 
  
        if(sCookieVal != null)
        {      
            var oOption = document.createElement("OPTION");
            oOption.text = sCookieVal;
            oOption.value = j;
            selDLC.add(oOption); 
        }          
    }
}

```



<span data-ttu-id="710eb-141">Die **ClearList** -Funktion entfernt alle Elemente aus dem Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="710eb-141">The function **ClearList** removes all items from the list box.</span></span>

<span data-ttu-id="710eb-142">Die Funktion gibt dann eine Schleife ein.</span><span class="sxs-lookup"><span data-stu-id="710eb-142">The function then enters a loop.</span></span> <span data-ttu-id="710eb-143">Jeder Cookie-Name wird als Zeichenfolge erstellt, und das Cookie wird durch Aufrufen der Hilfsfunktion **GetCookie** abgerufen.</span><span class="sxs-lookup"><span data-stu-id="710eb-143">Each cookie name is built as a string, and then the cookie is retrieved by calling the helper function **GetCookie**.</span></span> <span data-ttu-id="710eb-144">Nachdem das Cookie abgerufen wurde, wird es durch Aufrufen von " **Delta Cookie**" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="710eb-144">Once retrieved, the cookie is deleted by calling **DelCookie**.</span></span> <span data-ttu-id="710eb-145">Wenn das Cookie über einen Wert verfügt, wird der Wert dem Listenfeld hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="710eb-145">If the cookie has a value, the value is added to the list box.</span></span> <span data-ttu-id="710eb-146">Durch diese Aktion wird das **OnChange** -Ereignis für die seldlc-Liste initiiert, das wiederum die Handlerfunktion mit dem Namen " **onselectdlc**" aufruft.</span><span class="sxs-lookup"><span data-stu-id="710eb-146">This action initiates the **onChange** event for the selDLC list, which in turn calls the handler function named **OnSelectDLC**.</span></span> <span data-ttu-id="710eb-147">Dabei handelt es sich um dieselbe Funktion, die ausgeführt wird, wenn der Benutzer eine Download Auflistung auswählt. Dabei handelt es sich um den Code, der das Listenfeld Download Element ausfüllt.</span><span class="sxs-lookup"><span data-stu-id="710eb-147">This is the same function that executes when the user selects a download collection; it is the code that fills the download item list box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="710eb-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="710eb-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="710eb-149">**Verwenden des Download-Managers**</span><span class="sxs-lookup"><span data-stu-id="710eb-149">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




