---
title: Optimierung mithilfe von "GetInfoEx"
description: Wird verwendet, um bestimmte Attributwerte aus dem zugrunde liegenden Verzeichnisdienst in den lokalen Cache zu laden.
ms.assetid: e6111957-22cb-4473-9814-5bcbc79583b2
ms.tgt_platform: multiple
keywords:
- Optimierung mit GetInfoEx ADSI
- GetInfoEx ADSI, Optimierung mithilfe von IADs GetInfoEx
- ADSI ADSI, using, Optimierung mithilfe der IADs GetInfoEx-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b522093fff00700cf35b864edde2a6ae7f8f9922
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316454"
---
# <a name="optimization-using-getinfoex"></a>Optimierung mithilfe von "GetInfoEx"

Die [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) -Methode wird verwendet, um bestimmte Attributwerte aus dem zugrunde liegenden Verzeichnisdienst in den lokalen Cache zu laden. Diese Methode lädt nur die angegebenen Attributwerte in den lokalen Cache. Die [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Methode wird verwendet, um alle Attributwerte in den lokalen Cache zu laden.

Die [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) -Methode ruft bestimmte aktuelle Werte für die Eigenschaften eines Active Directory Objekts aus dem zugrunde liegenden Verzeichnis Speicher ab und aktualisiert die zwischengespeicherten Werte.

Wenn bereits ein Wert im Eigenschafts Cache vorhanden ist, wird der zwischengespeicherte Wert anstelle des aktuellen Werts aus dem zugrunde liegenden Verzeichnis abgerufen, wenn die [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -oder [**IADs. Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode aufgerufen wird, ohne dass zuerst " [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) " für dieses Attribut aufgerufen wird. Dies kann bewirken, dass aktualisierte Attributwerte überschrieben werden, wenn der lokale Cache geändert wurde, die Werte jedoch nicht mit einem Aufrufen der [**IADs. * tinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode in den zugrunde liegenden Verzeichnisdienst übertragen wurden. Die empfohlene Methode zur Vermeidung von zwischen Speicherungs Problemen besteht darin, die Attribut Wertänderungen immer zu übertragen, indem **IADs. SetInfo** aufgerufen wird, bevor [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo)aufgerufen wird


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



## <a name="retrieving-active-directory-constructed-attributes"></a>Abrufen Active Directory konstruierter Attribute

In Active Directory werden die meisten konstruierten Attribute abgerufen und zwischengespeichert, wenn die [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Methode aufgerufen wird ([**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) führt einen impliziten **IADs. GetInfo** -Aufruf aus, wenn der Cache leer ist). Einige konstruierte Attribute werden jedoch nicht automatisch abgerufen und zwischengespeichert. Daher ist es erforderlich, dass die [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) -Methode explizit aufgerufen wird, um Sie abzurufen. In Active Directory wird das Attribut [**CanonicalName**](/windows/desktop/ADSchema/a-canonicalname) beispielsweise nicht abgerufen, wenn die **IADs. GetInfo** -Methode aufgerufen wird und **IADs. Get** die **E \_ ADS- \_ Eigenschaft \_ nicht \_ gefunden** zurückgibt. Die **IADs. GetInfoEx** -Methode muss aufgerufen werden, um das **CanonicalName** -Attribut abzurufen. Diese konstruierten Attribute werden auch nicht mithilfe der [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) -Schnittstelle zum Auflisten der Attribute abgerufen.

Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie alle Attributwerte abrufen, finden Sie unter [Beispielcode zum Lesen eines konstruierten Attributs](example-code-for-reading-a-constructed-attribute.md).

 

 