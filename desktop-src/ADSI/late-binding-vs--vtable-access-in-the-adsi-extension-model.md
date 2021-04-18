---
title: Späte Bindung im Vergleich zu Vtable-Zugriff im ADSI-Erweiterungs Modell
description: Eine duale Schnittstelle ermöglicht den direkten Vtable-Zugriff auf alle Funktionen, während eine Dispatchschnittstelle dies nicht tut.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- späte Bindung im Vergleich zu Vtable-Zugriff im ADSI-Erweiterungs Modell ADSI
- Erweiterungen ADSI, späte Bindung im Vergleich zu Vtable-Zugriff im ADSI-Erweiterungs Modell
- ADSI ADSI, Beispielcode Visual Basic mit iadsdualinf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f95431fcde9a194f28cd103d93faa3f182c1968
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339097"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a>Späte Bindung im Vergleich zu Vtable-Zugriff im ADSI-Erweiterungs Modell

Eine duale Schnittstelle ermöglicht den direkten Vtable-Zugriff auf alle Funktionen, während eine Dispatchschnittstelle dies nicht tut. Ein C/C++-Client kann einen doppelten Schnittstellen Zeiger Abfragen und den direkten Vtable-Zugriff verwenden, um seine Funktionen aufzurufen. Dies ermöglicht einen schnelleren Zugriff als das Aufrufen der Funktion mithilfe der Funktionen [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) und [**IDispatch:: Aufrufen**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) . Dies gilt insbesondere für das Erweiterungs Modell, da alle Dual Schnittstellen in einem Erweiterungs Objekt ihre **GetIDsOfNames** -und **Aufruf** Funktionen zunächst an den Aggregator (ADSI) zurück delegieren müssen. Der Aggregator muss dann zusätzliche interne Schritte durchführen, um zu ermitteln, welches Erweiterungs Objekt, möglicherweise auch den Aggregator selbst, Unterstützung für die aufgerufene Funktion und den Aufruf an das entsprechende-Objekt bereitstellt.

Visual Basic ruft auch eine Dual-Interface-Funktion mit direktem Zugriff auf eine Vtable auf, wenn Sie über einen Zeiger auf die-Schnittstelle und Zugriff auf Typdaten aus der Typbibliothek verfügt. In Visual Basic geschriebene ADSI-Clients können einen Zeiger auf eine duale Schnittstelle, z. b. [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explizit angeben und somit den vtable-Zugriff auf Funktionen in der Schnittstelle ermöglichen.


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



Da eine [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle keinen Vtable-Zugriff unterstützt, gilt dieses Beispiel nicht. Das heißt, eine dispatchfunktion wird immer durch die [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) -und [**IDispatch:: Aufrufen**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) -Funktionen aufgerufen.

Die aktuellen Releases von VBScript und JScript unterstützen auch keinen Vtable-Zugriff. Daher wird eine duale Schnittstelle in einer VBScript-oder JScript-Umgebung wie eine Dispatch-Schnittstelle ausgeführt.

 

 