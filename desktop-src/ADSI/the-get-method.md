---
title: Die Get-Methode
description: Die Get-Methode der IADs wird verwendet, um einzelne benannte Attribute aus einem Verzeichnisobjekt abzurufen.
ms.assetid: e3754663-fe31-46f3-9dc1-a9c96ed53fde
ms.tgt_platform: multiple
keywords:
- AdsI mithilfe von IADs Get
- ADSI ADSI mithilfe der Get-Methode der IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386c3fe6e50a9f7357ec161b1e6bd8731cf8d0a74eed4b4a765adc3315c1045d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838630"
---
# <a name="the-get-method"></a>Die Get-Methode

Die [**IADs::Get-Methode**](/windows/desktop/api/Iads/nf-iads-iads-get) wird verwendet, um einzelne benannte Attribute aus einem Verzeichnisobjekt abzurufen.

Im folgenden Codebeispiel wird die [**IADs::Get-Methode**](/windows/desktop/api/Iads/nf-iads-iads-get) verwendet, um ein benanntes Attribut aus einem -Objekt abzurufen.


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



In Automation-Sprachen kann auch direkt mithilfe der Punkt notation auf benannte Attribute zugegriffen werden. Beispiel: **Objekt. Get("distinguishedName") ist** identisch mit **object.distinguishedName**.

Das folgende Codebeispiel ist mit dem vorherigen Beispiel identisch, mit der Ausnahme, dass auf das **DistinguishedName-Attribut** mithilfe der Punkt notation zugegriffen wird.


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



Wenn für das Objekt kein Wert festgelegt ist, gibt die [**IADs::Get-Methode**](/windows/desktop/api/Iads/nf-iads-iads-get) den Fehler "Eigenschaft nicht im Cache gefunden" zurück.

 

 




