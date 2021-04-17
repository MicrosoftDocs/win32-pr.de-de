---
description: Gibt ein HRESULT zurück. In diesem HRESULT gibt der Wert S OK an \_ , dass die Methode erfolgreich ausgeführt wurde.
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: Eigenschaften der Zertifikat Registrierungs Steuerung in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76525f26f318178f122cc0feee6221bbd948bba0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525832"
---
# <a name="certificate-enrollment-control-properties-in-c"></a>Eigenschaften der Zertifikat Registrierungs Steuerung in C++

Wenn Sie in C++ eine Eigenschaft für die Zertifikat Registrierungs Steuerung festlegen oder abrufen, gibt der Methodenaufrufe ein **HRESULT** zurück. In diesem **HRESULT** gibt der Wert S OK an \_ , dass die Methode erfolgreich ausgeführt wurde.

In C++ geschriebene Programme können die Zertifikatregistrierungs-Steuerungseigenschaften mithilfe von Methoden aufrufen in der folgenden Form abrufen.


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



Dabei gibt *propertyName* den Namen der Eigenschaft an, auf die zugegriffen wird, und *ppropvalue* ist ein Zeiger auf eine Variable des entsprechenden Datentyps. Nach erfolgreichem Abschluss dieses Methoden Aufrufens zeigt *ppropvalue* auf die Variable, die den Wert der *propertyName* -Eigenschaft enthält.

Um z. b. den Wert für die **rootstoretype** -Eigenschaft abzurufen, verwenden Sie den folgenden Code.


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



In C++ geschriebene Programme können die Eigenschaften für die Zertifikat Registrierungs Steuerung festlegen, indem Sie Methoden in der folgenden Form aufrufen.


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



Dabei gibt *propertyName* den Namen der Eigenschaft an, auf die zugegriffen wird, und *propvalue* ist ein Wert des entsprechenden Datentyps. Nach erfolgreichem Abschluss dieses Methoden Aufrufes ist der neue Wert der *propertyName* -Eigenschaft *propvalue*.

Um z. b. den-Eigenschafts Wert für **rootstoretype** festzulegen, könnte der folgende Code verwendet werden.


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



