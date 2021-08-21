---
title: Schnittstelleneigenschaftsmethoden
description: Viele ADSI-Schnittstellen sind für die Unterstützung von Automation konzipiert und daher duale Schnittstellen, da sie den Clientzugriff sowohl über IUnknown- als auch über IDispatch-Schnittstellen unterstützen.
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- Schnittstelleneigenschaftsmethoden
- ADSI ADSI , Referenz, Eigenschaftenmethoden erläutert
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fa872ea1711b23d850fe7063364712bba19d28d3e1157a81f5289f247944db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017087"
---
# <a name="interface-property-methods"></a>Schnittstelleneigenschaftsmethoden

Viele ADSI-Schnittstellen sind für die Unterstützung von Automation konzipiert und daher duale Schnittstellen, da sie den Clientzugriff sowohl über [**IUnknown-**](/windows/win32/api/unknwn/nn-unknwn-iunknown) als auch [**über IDispatch-Schnittstellen**](/windows/win32/api/oaidl/nn-oaidl-idispatch) unterstützen. Nicht-Automatisierungsclients, z. B. in C/C++ geschriebene Clients, lösen den Methodenaufruf direkt mithilfe der [**IUnknown::QueryInterface-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, und rufen Sie die Methode direkt auf. Automatisierungsclients, auch als namensgebundene Clients bezeichnet, z. B. in Visual Basic oder Visual Basic Scripting Edition (VBScript) geschriebene Clients, müssen den Methodenaufruf indirekt mithilfe der [**dispinterface-Methode**](/previous-versions/windows/desktop/automat/dispinterface) auflösen.

Eine ADSI-Schnittstelle, die Automation unterstützt, definiert Eigenschaftenmethoden zum Abrufen und Ändern von Eigenschaften eines Objekts, das die Schnittstelle implementiert. Die Eigenschaftenmethoden verfügen über Namen, denen **get** und den entsprechenden Eigenschaftsnamen vorankommt, z. B. get \_  \_ **\_ User** und **put \_ Name**.

Jede **\_ get-Methode** akzeptiert einen einzelnen Parameter als Ausgabe. Dieser Parameter ist eine von der Methode zugeordnete Adresse einer Variablen des Eigenschaftsdatentyps. Bei der Rückgabe geht diese Variable vom aktuellen Wert der angeforderten Eigenschaft aus. Der Aufrufer muss den zugeordneten Arbeitsspeicher der Variablen frei geben, wenn die -Eigenschaft nicht mehr benötigt wird.

Jede **\_ put-Methode** akzeptiert einen einzelnen Parameter als Eingabe für den Datentyp der entsprechenden Eigenschaft. Der -Parameter enthält einen neuen Wert der -Eigenschaft.

Das folgende Codebeispiel zeigt den Aufruf der Eigenschaftenmethoden, die der üblichen Prozedur zum Aufrufen der Memberfunktion eines Objekts folgen.


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



Das folgende Codebeispiel zeigt den Aufruf der Eigenschaftenmethoden in Automatisierungsclients, die sich etwas unterscheiden können. Beispielsweise verwendet Visual Basic punktierte Notation.


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



Alle Parameter und Rückgabetypen müssen diejenigen sein, die der VARIANT-Datentyp definiert. Alle Methoden auf einer dualen Schnittstelle geben einen HRESULT-Wert zurück, um einen Erfolg oder Fehler anzugeben.

Weitere Informationen zum Abrufen und Festlegen von Eigenschaften für ADSI-Objekte finden Sie unter [Eigenschaftencache](property-cache-interfaces.md).

 

 