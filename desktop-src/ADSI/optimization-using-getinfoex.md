---
title: Optimierung mit GetInfoEx
description: Wird verwendet, um bestimmte Attributwerte aus dem zugrunde liegenden Verzeichnisdienst in den lokalen Cache zu laden.
ms.assetid: e6111957-22cb-4473-9814-5bcbc79583b2
ms.tgt_platform: multiple
keywords:
- Optimierung mit GetInfoEx ADSI
- GetInfoEx ADSI , Optimierung mit IADs GetInfoEx
- ADSI ADSI , Using, Optimization Using the IADs GetInfoEx Method
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4daf75fa3961a57996d6ae51d237d27835213a25a20c52452b5896c6224964a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838994"
---
# <a name="optimization-using-getinfoex"></a>Optimierung mit GetInfoEx

Die [**IADs.GetInfoEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) wird verwendet, um bestimmte Attributwerte aus dem zugrunde liegenden Verzeichnisdienst in den lokalen Cache zu laden. Diese Methode lädt nur die angegebenen Attributwerte in den lokalen Cache. Die [**IADs.GetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) wird verwendet, um alle Attributwerte in den lokalen Cache zu laden.

Die [**IADs.GetInfoEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) ruft bestimmte aktuelle Werte für die Eigenschaften eines Active Directory-Objekts aus dem zugrunde liegenden Verzeichnisspeicher ab und aktualisiert die zwischengespeicherten Werte.

Wenn jedoch bereits ein Wert im Eigenschaftencache vorhanden ist, ruft der Aufruf der [**IADs.Get-**](/windows/desktop/api/Iads/nf-iads-iads-get) oder [**IADs.GetEx-Methode,**](/windows/desktop/api/Iads/nf-iads-iads-getex) ohne zuerst [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) für dieses Attribut aufzurufen, den zwischengespeicherten Wert anstelle des aktuellen Werts aus dem zugrunde liegenden Verzeichnis ab. Dies kann dazu führen, dass aktualisierte Attributwerte überschrieben werden, wenn der lokale Cache geändert wurde, aber für die Werte kein Commit an den zugrunde liegenden Verzeichnisdienst mit einem Aufruf der [**IADs.SetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) ausgeführt wurde. Die empfohlene Methode zum Vermeiden von Zwischenspeicherungsproblemen besteht darin, Attributwertänderungen immer durch Aufrufen von **IADs.SetInfo** vor dem Aufrufen von [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo)zu committen.


```VB
Dim usr As IADs
Dim PropArray As Variant

On Error GoTo Cleanup

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' The code example assumes that the property description has a single value in the directory.
' Be aware that this will implicitly call GetInfo because, at this point, GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Change two of the attribute values in the local cache.
usr.Put "cn", "Jeff Smith"
usr.Put "title", "Vice President"
usr.Put "department", "Head Office"
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Initialize the array of properties to pass to GetInfoEx.
PropArray = Array("department", "title")
 
' Get the specified attribute values.
usr.GetInfoEx PropArray, 0

' The specific attributes values were overwritten, but the attribute
' value not retrieved has not changed.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="retrieving-active-directory-constructed-attributes"></a>Abrufen von von Active Directory konstruierten Attributen

In Active Directory werden die meisten konstruierten Attribute abgerufen und zwischengespeichert, wenn die [**IADs.GetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) aufgerufen wird ([**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) führt einen impliziten **IADs.GetInfo-Aufruf** aus, wenn der Cache leer ist). Einige konstruierte Attribute werden jedoch nicht automatisch abgerufen und zwischengespeichert und erfordern daher, dass die [**IADs.GetInfoEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) explizit aufgerufen wird, um sie abzurufen. Beispielsweise wird in Active Directory das [**canonicalName-Attribut**](/windows/desktop/ADSchema/a-canonicalname) nicht abgerufen, wenn die **IADs.GetInfo-Methode** aufgerufen wird und **IADs.Get** **E ADS PROPERTY NOT \_ \_ \_ \_ FOUND** zurückgibt. Die **IADs.GetInfoEx-Methode** muss aufgerufen werden, um das **canonicalName-Attribut** abzurufen. Die gleichen konstruierten Attribute werden auch nicht mithilfe der [**IADsPropertyList-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) abgerufen, um die Attribute aufzulisten.

Weitere Informationen und ein Codebeispiel, das zeigt, wie alle Attributwerte abgerufen werden, finden Sie unter [Beispielcode zum Lesen eines konstruierten Attributs.](example-code-for-reading-a-constructed-attribute.md)

 

 