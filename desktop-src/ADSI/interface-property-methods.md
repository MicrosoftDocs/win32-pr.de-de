---
title: Schnittstelleneigenschaften Methoden
description: Viele ADSI-Schnittstellen dienen zur Unterstützung der Automatisierung und sind daher duale Schnittstellen darin, dass Sie den Client Zugriff über IUnknown-und IDispatch-Schnittstellen unterstützen.
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- Schnittstelleneigenschaften Methoden
- ADSI ADSI, Referenz, Eigenschaften Methoden erläutert
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018999d4834859cdb465bba2e6cdb9a05bd38a98
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106342376"
---
# <a name="interface-property-methods"></a>Schnittstelleneigenschaften Methoden

Viele ADSI-Schnittstellen dienen zur Unterstützung der Automatisierung und sind daher duale Schnittstellen darin, dass Sie den Client Zugriff über [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -und [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstellen unterstützen. Nicht Automatisierungs Clients, wie z. b. in C/C++ geschriebene Clients, lösen den Methodenaufruf direkt mithilfe der [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode aus, und die Methode wird direkt aufgerufen. Automatisierungs Clients, auch als namens gebundene Clients bezeichnet (z. b. in Visual Basic oder Visual Basic Scripting Edition (VBScript)), müssen den Methodenaufruf indirekt mit der [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) -Methode auflösen.

Eine ADSI-Schnittstelle zur Unterstützung der Automatisierung definiert Eigenschaften Methoden zum Abrufen und Ändern von Eigenschaften eines Objekts, das die-Schnittstelle implementiert. Die Eigenschaften Methoden haben Namen, denen " **Get** " \_ und " **Put** " \_ die entsprechenden Eigenschaften Namen vorangestellt sind, z. b. " **get \_ User** " und " **Put \_ Name**".

Jede **get \_** -Methode nimmt einen einzelnen Parameter als Ausgabe an. Dieser Parameter ist eine von der Methode zugewiesene Adresse einer Variablen des Eigenschafts Datentyps. Bei der Rückgabe nimmt diese Variable den aktuellen Wert der angeforderten Eigenschaft an. Der Aufrufer muss den zugewiesenen Speicher der Variablen freigeben, wenn die Eigenschaft nicht mehr benötigt wird.

Jede **Put \_** -Methode nimmt einen einzelnen Parameter als Eingabe für den Datentyp der entsprechenden Eigenschaft an. Der-Parameter enthält einen neuen Wert der-Eigenschaft.

Im folgenden Codebeispiel wird der Aufruf der-Eigenschaften Methoden veranschaulicht, die der üblichen Prozedur folgen, um die Member-Funktion eines Objekts aufzurufen.


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



Im folgenden Codebeispiel wird der Aufruf der-Eigenschaften Methoden in Automatisierungs Clients veranschaulicht, die sich etwas unterscheiden können. Beispielsweise Visual Basic die Punkt Notation verwendet.


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



Alle Parameter und Rückgabe Typen müssen die Werte aufweisen, die der Variant-Datentyp definiert. Alle Methoden für eine duale Schnittstelle geben einen HRESULT-Wert zurück, um einen Erfolg oder Fehler anzugeben.

Weitere Informationen zum erhalten und Festlegen von Eigenschaften für ADSI-Objekte finden Sie unter [Property Cache](property-cache-interfaces.md).

 

 