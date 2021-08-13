---
title: Die GetEx-Methode
description: Einige Attribute können einen oder mehrere Werte speichern.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- GetEx ADSI mit IADs GetEx
- ADSI ADSI mithilfe der GetEx-Methode von IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e656bd6a48830feb725e927f08be1d573e7b0232cf02c16ee87bd7d6a5b2f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690149"
---
# <a name="the-getex-method"></a>Die GetEx-Methode

Einige Attribute können einen oder mehrere Werte speichern. Beispielsweise ist das **otherTelephone-Attribut** eines Benutzerobjekts in Active Directory eine Eigenschaft, die null, einen oder viele Werte aufweisen kann. Attribute mit mehreren Werten werden als "mehrwertige Attribute" bezeichnet. Wenn die [**IADs::Get-Methode**](/windows/desktop/api/Iads/nf-iads-iads-get) zum Abrufen eines mehrwertigen Attributs verwendet wird, müssen die Ergebnisse anders verarbeitet werden, als wenn das Attribut über einen einzelnen Wert verfügt. Die von der [**IADs::GetEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getex) bereitgestellten Ergebnisse werden jedoch auf die gleiche Weise verarbeitet, unabhängig davon, ob das Attribut über einen einzelnen oder mehrere Werte verfügt. In beiden Fällen gibt die **IADs::GetEx-Methode** die Werte in einem Array zurück.

Die [**IADs::GetEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getex) ruft Eigenschaften aus dem Eigenschaftencache ab. Wenn die angegebene Eigenschaft nicht im Cache gefunden wird, führt **IADs::GetEx** einen impliziten [**IADs::GetInfo-Aufruf**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) aus.

Die [**IADs::GetEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getex) gibt unabhängig von der Anzahl der vom Server zurückgegebenen Werte ein Variantarray von Varianten zurück. Dies gilt auch, wenn das Attribut nur einen Wert enthält.


```VB
Dim usr As IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
homePhones = usr.GetEx("otherHomePhone")
For each phone in homePhones
    Debug.Print phone
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



Die [**IADs::GetEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getex) kann auch für einwertige Attribute verwendet werden. Die Ergebnisse eines einwertigen Attributs werden genauso verarbeitet wie die Ergebnisse für ein mehrwertiges Attribut.


```VB
Dim usr as IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
sds = usr.GetEx("ntSecurityDescriptor")
For each sd in sds
    Set acl = sd.DiscretionaryACL
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



Wenn kein Wert für das Attribut festgelegt ist, gibt [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) den Fehler "Property not found in cache" (Eigenschaft wurde nicht im Cache gefunden) zurück.

 

 




