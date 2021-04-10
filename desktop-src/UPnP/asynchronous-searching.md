---
title: Asynchrone Suche
description: Das Device Finder-Objekt ermöglicht synchrone und asynchrone Suchvorgänge. Asynchrone Suchvorgänge geben die Steuerung sofort an die aufrufende Anwendung zurück.
ms.assetid: 809cfb65-9d08-427b-90d9-b8a836176341
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57377eb8ae5a49fc9bafe81f90b9ee7c602ae4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947993"
---
# <a name="asynchronous-searching"></a><span data-ttu-id="c2682-104">Asynchrone Suche</span><span class="sxs-lookup"><span data-stu-id="c2682-104">Asynchronous Searching</span></span>

<span data-ttu-id="c2682-105">Das Device Finder-Objekt ermöglicht synchrone und asynchrone Suchvorgänge.</span><span class="sxs-lookup"><span data-stu-id="c2682-105">The Device Finder object enables both synchronous and asynchronous searches.</span></span> <span data-ttu-id="c2682-106">Asynchrone Suchvorgänge geben die Steuerung sofort an die aufrufende Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="c2682-106">Asynchronous searches return control to the calling application immediately.</span></span> <span data-ttu-id="c2682-107">Anschließend wird die Anwendung über jedes einzelne Gerät benachrichtigt, wenn Sie gefunden wird. dabei wird eine von der Anwendung registrierte Rückruf Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2682-107">Then, the application is notified about each individual device as it is found, using a callback interface that the application has registered.</span></span>

<span data-ttu-id="c2682-108">Die asynchrone Suche eignet sich am besten für grafische Benutzeroberflächen und Anwendungen, die eine kontinuierliche Überwachung durchführen.</span><span class="sxs-lookup"><span data-stu-id="c2682-108">Asynchronous searching is best for graphical user interfaces, and applications that perform continuous monitoring.</span></span>

<span data-ttu-id="c2682-109">Die allgemeine Struktur einer asynchronen Suche lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c2682-109">The general structure of an asynchronous search is:</span></span>

1.  <span data-ttu-id="c2682-110">Erstellen eines Such Objekts</span><span class="sxs-lookup"><span data-stu-id="c2682-110">Create a search object</span></span>
2.  <span data-ttu-id="c2682-111">Starten der Suche</span><span class="sxs-lookup"><span data-stu-id="c2682-111">Start the search</span></span>
3.  <span data-ttu-id="c2682-112">Empfangen Sie Rückruf Benachrichtigungen, und führen Sie die entsprechenden Verarbeitungsschritte aus.</span><span class="sxs-lookup"><span data-stu-id="c2682-112">Receive callback notifications and take the appropriate processing steps.</span></span>
4.  <span data-ttu-id="c2682-113">Wenn die Suche nicht mehr benötigt wird, brechen Sie die Suche ab, und geben Sie die zugeordneten Objekte frei.</span><span class="sxs-lookup"><span data-stu-id="c2682-113">When the search is no longer needed, cancel the search and release the associated objects.</span></span>

> [!Note]  
> <span data-ttu-id="c2682-114">Im Rückruf Code kann eine Anwendung das Objekt, über das Sie benachrichtigt wird, nicht freigeben, z. b. ein neues Gerät, und die Anwendung kann die Suche nicht abbrechen.</span><span class="sxs-lookup"><span data-stu-id="c2682-114">In the callback code, an application cannot release the object it is receiving notification about, such as a new device, nor can the application cancel the search.</span></span>

 

## <a name="c-example"></a><span data-ttu-id="c2682-115">C++-Beispiel</span><span class="sxs-lookup"><span data-stu-id="c2682-115">C++ Example</span></span>

<span data-ttu-id="c2682-116">C++-Anwendungen müssen ein Rückruf Objekt implementieren, das an die Suche übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2682-116">C++ applications must implement a callback object to pass to the search.</span></span> <span data-ttu-id="c2682-117">Beispielcode, der diese Aktion veranschaulicht, finden Sie [unter Asynchrones suchen in C++](searching-asynchronously-in-c-.md) .</span><span class="sxs-lookup"><span data-stu-id="c2682-117">See [Searching Asynchronously in C++](searching-asynchronously-in-c-.md) for sample code that illustrates this action.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="c2682-118">VBScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="c2682-118">VBScript Example</span></span>

<span data-ttu-id="c2682-119">VBScript-Code muss die Adresse der Rückruffunktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="c2682-119">VBScript code must pass the address of the callback function.</span></span>


```VB
Sub DeviceFinderCallback (device, UDN, calltype)

  select case calltype
    Case 0
      output = "Found: " & vbCrLf
      output = output & "DisplayName: " & device.FriendlyName & vbCrLf
      output = output & "Type: " & device.Type & vbCrLf
      output = output & "UDN: " & device.UniqueDeviceName & vbCrLf
      MsgBox output

    Case 1
      MsgBox "device removed: " & UDN

    Case 2
      MsgBox "search complete"

    end select
End Sub

Dim devicefinder
Dim findData

Set devicefinder = CreateObject("UPnP.UPnPDeviceFinder")

Sub StartFind()
  findData = devicefinder.CreateAsyncFind("upnp:rootdevice", 0, _
   GetRef("DeviceFinderCallback"))

  devicefinder.StartAsyncFind(findData)
End Sub

Sub StopFind()
  deviceFinder.CancelAsyncFind(findData)
End Sub
```



 

 




