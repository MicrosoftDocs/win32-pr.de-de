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
# <a name="asynchronous-searching"></a>Asynchrone Suche

Das Device Finder-Objekt ermöglicht synchrone und asynchrone Suchvorgänge. Asynchrone Suchvorgänge geben die Steuerung sofort an die aufrufende Anwendung zurück. Anschließend wird die Anwendung über jedes einzelne Gerät benachrichtigt, wenn Sie gefunden wird. dabei wird eine von der Anwendung registrierte Rückruf Schnittstelle verwendet.

Die asynchrone Suche eignet sich am besten für grafische Benutzeroberflächen und Anwendungen, die eine kontinuierliche Überwachung durchführen.

Die allgemeine Struktur einer asynchronen Suche lautet wie folgt:

1.  Erstellen eines Such Objekts
2.  Starten der Suche
3.  Empfangen Sie Rückruf Benachrichtigungen, und führen Sie die entsprechenden Verarbeitungsschritte aus.
4.  Wenn die Suche nicht mehr benötigt wird, brechen Sie die Suche ab, und geben Sie die zugeordneten Objekte frei.

> [!Note]  
> Im Rückruf Code kann eine Anwendung das Objekt, über das Sie benachrichtigt wird, nicht freigeben, z. b. ein neues Gerät, und die Anwendung kann die Suche nicht abbrechen.

 

## <a name="c-example"></a>C++-Beispiel

C++-Anwendungen müssen ein Rückruf Objekt implementieren, das an die Suche übergeben werden soll. Beispielcode, der diese Aktion veranschaulicht, finden Sie [unter Asynchrones suchen in C++](searching-asynchronously-in-c-.md) .

## <a name="vbscript-example"></a>VBScript-Beispiel

VBScript-Code muss die Adresse der Rückruffunktion übergeben.


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



 

 




