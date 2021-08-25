---
title: Unterstützung für späte Bindungen
description: Wenn späte Bindungsunterstützung vorhanden ist, muss jeder Funktionsaufruf die ADSI-IDispatch-Schnittstelle durchlaufen, bevor er an die entsprechende Erweiterung umgeleitet wird.
ms.assetid: fbdc6234-9381-4d64-bf02-05e393b3e0bd
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, Unterstützung für späte Bindungen
- ADSI ADSI , Beispielcode Visual Basic, Unterstützung für späte Bindungen
- Binden von AD, Unterstützung für späte Bindungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff8a66764e49e912e7d4db61356c997516b8d2192046912e673640e9567e415
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821320"
---
# <a name="late-binding-support"></a>Unterstützung für späte Bindungen

Wenn späte Bindungsunterstützung vorhanden ist, muss jeder Funktionsaufruf die [**ADSI-IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) durchlaufen, bevor er an die entsprechende Erweiterung umgeleitet wird.

Betrachten Sie das folgende Codebeispiel.


```C++
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
 
x.MyNewMethod( "\\srv\public")
x.MyProperty = "Hello World"
 
x.OtherMethod()
x.OtherProperty = 4362
 
Debug.Print x.LastName
```



Es gibt keine expliziten Aufrufe der **QueryInterface-Methode,** um die Erweiterungen abzurufen. Die Erweiterungen müssen ihre [**IDispatch-Aufrufe**](/windows/win32/api/oaidl/nn-oaidl-idispatch) an die **ADSI-IDispatch-Schnittstelle** umleiten. ADSI trifft die Entscheidung und löst alle konflikte, die auftreten, und leitet dann mithilfe einer Schnittstelle namens [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)erneut an die entsprechende Erweiterung weiter. Daher muss jede Erweiterung, die späte Bindung unterstützt, **IADsExtension** implementieren.

 

 