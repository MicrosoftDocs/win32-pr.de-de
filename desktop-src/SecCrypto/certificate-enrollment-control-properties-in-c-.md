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
# <a name="certificate-enrollment-control-properties-in-c"></a><span data-ttu-id="9c264-104">Eigenschaften der Zertifikat Registrierungs Steuerung in C++</span><span class="sxs-lookup"><span data-stu-id="9c264-104">Certificate Enrollment Control Properties in C++</span></span>

<span data-ttu-id="9c264-105">Wenn Sie in C++ eine Eigenschaft für die Zertifikat Registrierungs Steuerung festlegen oder abrufen, gibt der Methodenaufrufe ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="9c264-105">When you set or retrieve a Certificate Enrollment Control property in C++, the method call returns an **HRESULT**.</span></span> <span data-ttu-id="9c264-106">In diesem **HRESULT** gibt der Wert S OK an \_ , dass die Methode erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="9c264-106">In this an **HRESULT**, a value of S\_OK indicates that the method was successfully executed.</span></span>

<span data-ttu-id="9c264-107">In C++ geschriebene Programme können die Zertifikatregistrierungs-Steuerungseigenschaften mithilfe von Methoden aufrufen in der folgenden Form abrufen.</span><span class="sxs-lookup"><span data-stu-id="9c264-107">Programs written in C++ can retrieve the Certificate Enrollment Control properties by method calls in the following form.</span></span>


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



<span data-ttu-id="9c264-108">Dabei gibt *propertyName* den Namen der Eigenschaft an, auf die zugegriffen wird, und *ppropvalue* ist ein Zeiger auf eine Variable des entsprechenden Datentyps.</span><span class="sxs-lookup"><span data-stu-id="9c264-108">Where *propertyName* specifies the name of the property being accessed, and *pPropValue* is a pointer to a variable of the appropriate data type.</span></span> <span data-ttu-id="9c264-109">Nach erfolgreichem Abschluss dieses Methoden Aufrufens zeigt *ppropvalue* auf die Variable, die den Wert der *propertyName* -Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="9c264-109">After successful completion of this method call, *pPropValue* will point to the variable that contains the value of the *propertyName* property.</span></span>

<span data-ttu-id="9c264-110">Um z. b. den Wert für die **rootstoretype** -Eigenschaft abzurufen, verwenden Sie den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="9c264-110">For example, to retrieve the value for the **RootStoreType** property, you use the following code.</span></span>


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



<span data-ttu-id="9c264-111">In C++ geschriebene Programme können die Eigenschaften für die Zertifikat Registrierungs Steuerung festlegen, indem Sie Methoden in der folgenden Form aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9c264-111">Programs written in C++ can set the Certificate Enrollment Control properties by calling methods in the following form.</span></span>


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



<span data-ttu-id="9c264-112">Dabei gibt *propertyName* den Namen der Eigenschaft an, auf die zugegriffen wird, und *propvalue* ist ein Wert des entsprechenden Datentyps.</span><span class="sxs-lookup"><span data-stu-id="9c264-112">Where *propertyName* specifies the name of the property being accessed, and *PropValue* is a value of the appropriate data type.</span></span> <span data-ttu-id="9c264-113">Nach erfolgreichem Abschluss dieses Methoden Aufrufes ist der neue Wert der *propertyName* -Eigenschaft *propvalue*.</span><span class="sxs-lookup"><span data-stu-id="9c264-113">After successful completion of this method call, the new value of the *propertyName* property will be *PropValue*.</span></span>

<span data-ttu-id="9c264-114">Um z. b. den-Eigenschafts Wert für **rootstoretype** festzulegen, könnte der folgende Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c264-114">For example, to set the property value for the **RootStoreType**, the following code could be used.</span></span>


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



