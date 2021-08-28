---
title: Asynchrone Suche
description: Das Device Finder-Objekt ermöglicht sowohl synchrone als auch asynchrone Suchvorgänge. Asynchrone Suchvorgänge geben die Steuerung sofort an die aufrufende Anwendung zurück.
ms.assetid: 809cfb65-9d08-427b-90d9-b8a836176341
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3482e041798db929d1719e1a404823f161f9bf5b0e499f4eca1694df24b38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058138"
---
# <a name="asynchronous-searching"></a>Asynchrone Suche

Das Device Finder-Objekt ermöglicht sowohl synchrone als auch asynchrone Suchvorgänge. Asynchrone Suchvorgänge geben die Steuerung sofort an die aufrufende Anwendung zurück. Anschließend wird die Anwendung über jedes einzelne Gerät benachrichtigt, wie es gefunden wird. Dabei wird eine Rückrufschnittstelle verwendet, die von der Anwendung registriert wurde.

Die asynchrone Suche eignet sich am besten für grafische Benutzeroberflächen und Anwendungen, die eine kontinuierliche Überwachung durchführen.

Die allgemeine Struktur einer asynchronen Suche lautet:

1.  Erstellen eines Suchobjekts
2.  Starten der Suche
3.  Empfangen sie Rückrufbenachrichtigungen, und führen Sie die entsprechenden Verarbeitungsschritte aus.
4.  Wenn die Suche nicht mehr benötigt wird, brechen Sie die Suche ab, und geben Sie die zugeordneten Objekte frei.

> [!Note]  
> Im Rückrufcode kann eine Anwendung weder das Objekt freigeben, über das sie eine Benachrichtigung empfängt, z. B. ein neues Gerät, noch kann die Anwendung die Suche abbrechen.

 

## <a name="c-example"></a>C++-Beispiel

C++-Anwendungen müssen ein Rückrufobjekt implementieren, das an die Suche übergeben werden soll. Beispielcode zur Veranschaulichung dieser Aktion finden Sie [unter Asynchrones Suchen in C++.](searching-asynchronously-in-c-.md)

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



 

 




