---
title: Die Get-Methode
description: Die IADs Get-Methode wird verwendet, um einzelne benannte Attribute aus einem Verzeichnis Objekt abzurufen.
ms.assetid: e3754663-fe31-46f3-9dc1-a9c96ed53fde
ms.tgt_platform: multiple
keywords:
- ADSI mithilfe von IADs Get
- ADSI ADSI, using, using the IADs get Method
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11590fda2cfd207315453323fa3d0999f298103d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341626"
---
# <a name="the-get-method"></a>Die Get-Methode

Die [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode wird verwendet, um einzelne benannte Attribute aus einem Verzeichnis Objekt abzurufen.

Im folgenden Codebeispiel wird die [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode verwendet, um ein benanntes Attribut aus einem-Objekt abzurufen.


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.Get("distinguishedName")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



In Automatisierungs Sprachen können auf benannte Attribute auch direkt mithilfe der Punkt Notation zugegriffen werden. Beispielsweise **Object. Get ("Unterscheidung nach Name")** ist identisch mit **Object. unterscheiden Name**.

Das folgende Codebeispiel ist mit dem vorherigen Beispiel identisch, mit dem Unterschied, dass auf das Attribut "Unterscheidung nach **Name** " mithilfe der Punkt Notation zugegriffen wird.


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.distinguishedName

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



Wenn für das Objekt kein Wert festgelegt ist, gibt die [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode den Fehler "die Eigenschaft wurde nicht im Cache gefunden" zurück.

 

 




