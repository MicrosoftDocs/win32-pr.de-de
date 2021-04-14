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
# <a name="maintaining-session-information"></a>Verwalten von Sitzungsinformationen

## <a name="how-the-sample-stores-information"></a>Speichern von Informationen im Beispiel

Die Beispiel Webseite verwaltet Daten mithilfe von Cookies. Cookies sind einfach persistente Name/Wert-Paare, die der Webbrowser für Sie speichern kann.

Wenn die Webseite geschlossen wird, wird die Funktion zum **herunter** fahren ausgeführt. Beim **herunter** fahren wird die Funktion **setpdingcookies** aufgerufen. Diese Funktion durchläuft die Liste der Download Sammlungen, die im Dropdown-Listenfeld mit dem Namen seldlc gespeichert ist. Wenn eine Download Auflistung unvollständige Elemente enthält, ruft die Funktion die Methode **setcookie** auf und übergibt dabei einen Namen und einen Wert. Die namens Zeichenfolge wird festgelegt, indem ein ganzzahliger Wert an einen konstanten Wert ( **wmpdlc**) angehängt wird, der in der Variablen mit dem Namen g-Tabellenwert gespeichert wird \_ . Der Cookiename für die dritte ausstehende Download Auflistung lautet beispielsweise "WMPDLC2", da der Zählmechanismus Null basiert ist. Beim Erstellen jedes Cookies erhöht die Funktion die globale Variable g \_ Pending, um die Anzahl ausstehender Downloads beizubehalten. Der Code wird hier zur einfacheren wiedergegeben:


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



**Isdlccomplete** ist eine Hilfsfunktion, die einfach die einzelnen Download Elemente in der Download Auflistung durchläuft, um zu bestimmen, ob ein Element aussteht. Wenn es ein ausstehendes Element gibt, gibt die Funktion false zurück.

**Setcookie** ist die Funktion, die das Cookie erstellt.

Wenn **settzdingcookies** zurückgibt, erstellt **Shutdown** das count-Cookie, in dem der Wert aus der Variablen g Pending gespeichert wird \_ . Dieser Wert ist wichtig, da die Webseite eine Möglichkeit benötigt, zu bestimmen, wie viele Cookies beim erneuten Laden abgerufen werden sollen. Der Name des Anzahl Cookies wird in der Variablen mit dem Namen g \_ szählcookie gespeichert.

## <a name="how-the-sample-retrieves-information"></a>Abrufen von Informationen durch das Beispiel

Wenn die Webseite geladen wird, wird die **Init** -Funktion ausgeführt. Zuerst Ruft die Funktion **gettzdingdlcount** auf, um das Anzahl Cookie abzurufen. Anschließend wird dieser Wert in der Variablen mit dem Namen g \_ Pending gespeichert. Anschließend wird die Funktion " **populatedllist** " aufgerufen, um jedes Download Sitzungs Cookie abzurufen und seinen Bezeichner dem Dropdown-Listenfeld hinzuzufügen. Dies ist der Code für diese Funktion:


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



Die **ClearList** -Funktion entfernt alle Elemente aus dem Listenfeld.

Die Funktion gibt dann eine Schleife ein. Jeder Cookie-Name wird als Zeichenfolge erstellt, und das Cookie wird durch Aufrufen der Hilfsfunktion **GetCookie** abgerufen. Nachdem das Cookie abgerufen wurde, wird es durch Aufrufen von " **Delta Cookie**" gelöscht. Wenn das Cookie über einen Wert verfügt, wird der Wert dem Listenfeld hinzugefügt. Durch diese Aktion wird das **OnChange** -Ereignis für die seldlc-Liste initiiert, das wiederum die Handlerfunktion mit dem Namen " **onselectdlc**" aufruft. Dabei handelt es sich um dieselbe Funktion, die ausgeführt wird, wenn der Benutzer eine Download Auflistung auswählt. Dabei handelt es sich um den Code, der das Listenfeld Download Element ausfüllt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Download-Managers**](using-the-download-manager.md)
</dt> </dl>

 

 




