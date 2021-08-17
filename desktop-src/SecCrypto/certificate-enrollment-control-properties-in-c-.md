---
description: Gibt ein HRESULT zurück. In diesem HRESULT gibt der Wert S \_ OK an, dass die Methode erfolgreich ausgeführt wurde.
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: Eigenschaften der Zertifikatregistrierungssteuerung in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941967b7b4be0bfa6d7db2f9b31e2971f8ca1d0deb9d9f92540a1ae5300791a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771919"
---
# <a name="certificate-enrollment-control-properties-in-c"></a>Eigenschaften der Zertifikatregistrierungssteuerung in C++

Wenn Sie eine Certificate Enrollment Control-Eigenschaft in C++ festlegen oder abrufen, gibt der Methodenaufruf ein **HRESULT** zurück. In diesem **HRESULT** gibt der Wert S \_ OK an, dass die Methode erfolgreich ausgeführt wurde.

In C++ geschriebene Programme können die Eigenschaften der Zertifikatregistrierungssteuerung durch Methodenaufrufe im folgenden Format abrufen.


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



Dabei gibt *propertyName* den Namen der Eigenschaft an, auf die zugegriffen wird, und *pPropValue* ist ein Zeiger auf eine Variable des entsprechenden Datentyps. Nach erfolgreichem Abschluss dieses Methodenaufrufs zeigt *pPropValue* auf die Variable, die den Wert der *propertyName-Eigenschaft* enthält.

Um beispielsweise den Wert für die **RootStoreType-Eigenschaft** abzurufen, verwenden Sie den folgenden Code.


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



In C++ geschriebene Programme können die Eigenschaften der Zertifikatregistrierungssteuerung festlegen, indem Methoden im folgenden Format aufgerufen werden.


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



Dabei gibt *propertyName* den Namen der Eigenschaft an, auf die zugegriffen wird, und *PropValue* ist ein Wert des entsprechenden Datentyps. Nach erfolgreichem Abschluss dieses Methodenaufrufs ist der neue Wert der *propertyName-Eigenschaft* *PropValue.*

Um beispielsweise den Eigenschaftswert für **RootStoreType** festzulegen, kann der folgende Code verwendet werden.


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



