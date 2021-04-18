---
title: Die Getex-Methode
description: Einige Attribute können einen oder mehrere Werte speichern.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- Getex ADSI, using IADs Getex
- ADSI ADSI, using, using the IADs Getex Method
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a909b33664ad805b0bf483ee9f0c2b40316ec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338560"
---
# <a name="the-getex-method"></a>Die Getex-Methode

Einige Attribute können einen oder mehrere Werte speichern. Beispielsweise ist das **OtherTelephone** -Attribut eines Benutzer Objekts in Active Directory eine Eigenschaft, die NULL, einen oder mehrere Werte aufweisen kann. Attribute mit mehreren Werten werden als "mehrwertige Attribute" bezeichnet. Wenn die [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode zum Abrufen eines mehrwertigen Attributs verwendet wird, müssen die Ergebnisse anders verarbeitet werden, als wenn das Attribut über einen einzelnen Wert verfügt. Die Ergebnisse, die von der [**IADs:: Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode bereitgestellt werden, werden jedoch auf die gleiche Weise verarbeitet, unabhängig davon, ob das Attribut einen einzelnen oder mehrere Werte aufweist. In beiden Fällen gibt die **IADs:: Getex** -Methode die Werte in einem Array zurück.

Die [**IADs:: Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode ruft Eigenschaften aus dem Eigenschafts Cache ab. Wenn die angegebene Eigenschaft nicht im Cache gefunden wird, führt **IADs:: Getex** einen impliziten [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Aufrufs aus.

Die [**IADs:: Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode gibt ein Variant-Array von Varianten zurück, unabhängig von der Anzahl von Werten, die vom Server zurückgegeben werden. Dies gilt auch, wenn das Attribut nur einen Wert enthält.


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



Die [**IADs:: Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode kann auch für einwertige Attribute verwendet werden. Die Ergebnisse eines einwertigen Attributs werden genauso wie die Ergebnisse für ein mehr wertiges Attribut verarbeitet.


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



Wenn für das Attribut kein Wert festgelegt ist, gibt [**IADs:: Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) den Fehler "die Eigenschaft wurde im Cache nicht gefunden" zurück.

 

 




