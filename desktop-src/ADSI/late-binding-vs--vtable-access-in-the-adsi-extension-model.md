---
title: Späte Bindung im Vergleich zu VTable-Zugriff im ADSI-Erweiterungsmodell
description: Eine duale Schnittstelle ermöglicht direkten vtable-Zugriff auf alle ihre Funktionen, während eine Dispatchschnittstelle dies nicht tut.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- Späte Bindung und vtabler Zugriff im ADSI-Erweiterungsmodell ADSI
- Erweiterungen ADSI , späte Bindung und vtabler Zugriff im ADSI-Erweiterungsmodell
- ADSI ADSI , Beispielcode Visual Basic , mit IADsDualInf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eacc2008d3da33cd8d1897eeff2c30301849f9ec306656fc494072c33608c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023358"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a>Späte Bindung im Vergleich zu VTable-Zugriff im ADSI-Erweiterungsmodell

Eine duale Schnittstelle ermöglicht direkten vtable-Zugriff auf alle ihre Funktionen, während eine Dispatchschnittstelle dies nicht tut. Ein C/C++-Client kann einen Dual Interface-Zeiger abfragen und direkten vtable-Zugriff verwenden, um seine Funktionen aufzurufen. Dies ermöglicht einen schnelleren Zugriff als das Aufrufen der Funktion mithilfe der Funktionen [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) und [**IDispatch::Invoke.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) Dies gilt insbesondere für das Erweiterungsmodell, da alle dualen Schnittstellen in einem **Erweiterungsobjekt ihre Funktionen GetIDsOfNames** und **Invoke** zuerst an den Aggregator (ADSI) delegieren müssen. Der Aggregator muss dann zusätzliche interne Schritte ausführen, um zu ermitteln, welches Erweiterungsobjekt, möglicherweise einschließlich des Aggregators selbst, Unterstützung für die aufgerufene Funktion bereitstellt und den Aufruf an das entsprechende Objekt umleitet.

Visual Basic ruft auch eine Dual-Interface-Funktion mit direktem Zugriff auf eine vtable auf, wenn sie über einen Zeiger auf die Schnittstelle und Zugriff auf Typdaten aus der Typbibliothek verfügt. ADSI-Clients, die in Visual Basic geschrieben wurden, können explizit einen Zeiger auf eine duale Schnittstelle angeben, z. B. [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads)und so den vtable-Zugriff auf Funktionen in der Schnittstelle ermöglichen.


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



Da eine [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) keinen vtable-Zugriff unterstützt, gilt dieses Beispiel nicht. Das heißt, eine Dispatchfunktion wird immer nur über die Funktionen [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) und [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) aufgerufen.

Aktuelle Versionen von VBScript und JScript unterstützen auch keinen vtable-Zugriff. Daher funktioniert eine duale Schnittstelle in einer VBScript- oder JScript-Umgebung wie eine Dispatchschnittstelle.

 

 