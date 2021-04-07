---
title: Unterstützung späterer Bindungen
description: Wenn eine späte Bindungs Unterstützung vorhanden ist, muss jeder Funktions Aufrufer die ADSI IDispatch-Schnittstelle durchlaufen, bevor er an die entsprechende Erweiterung umgeleitet wird.
ms.assetid: fbdc6234-9381-4d64-bf02-05e393b3e0bd
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, späte Bindungs Unterstützung
- ADSI ADSI, Beispielcode Visual Basic, späte Bindungs Unterstützung
- Binden von AD, späterer Bindungs Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e4dd1de0000d9edbe3e73cbc47b81d094d48c2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730312"
---
# <a name="late-binding-support"></a>Unterstützung späterer Bindungen

Wenn eine späte Bindungs Unterstützung vorhanden ist, muss jeder Funktions Aufrufer die ADSI [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle durchlaufen, bevor er an die entsprechende Erweiterung umgeleitet wird.

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



Es gibt keine expliziten Aufrufe der **QueryInterface** -Methode, um die Erweiterungen zu erhalten. Die Erweiterungen müssen Ihre [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Aufrufe an die ADSI **IDispatch** -Schnittstelle umleiten. ADSI trifft die Entscheidung und löst alle auftretenden Konflikte auf und leitet dann mithilfe einer Schnittstelle namens [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension)wieder an die entsprechende Erweiterung weiter. Daher muss jede Erweiterung, die spätes Binden unterstützt, **iadsextension** implementieren.

 

 