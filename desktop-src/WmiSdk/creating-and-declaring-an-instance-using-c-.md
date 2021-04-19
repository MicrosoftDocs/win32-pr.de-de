---
description: Sie können eine Instanz in C++ über die IWbemServices-Schnittstelle erstellen.
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: Erstellen und Deklarieren einer Instanz mithilfe von C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd316975c68625383a9d2a2d1fe2fc389d30494a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356970"
---
# <a name="creating-and-declaring-an-instance-using-c"></a>Erstellen und Deklarieren einer Instanz mithilfe von C++

Sie können eine Instanz in C++ über die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle erstellen.

Die Codebeispiele in diesem Thema erfordern, dass die folgende \# include-Anweisung ordnungsgemäß kompiliert wird.


```C++
#include <wbemidl.h>
```



Im folgenden Verfahren wird beschrieben, wie eine Instanz einer vorhandenen Klasse erstellt wird.

**So erstellen Sie eine Instanz einer vorhandenen Klasse**

1.  Rufen Sie die Definition der vorhandenen Klasse ab, indem Sie die [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Methode oder die [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) -Methode aufrufen.

    Im folgenden Codebeispiel wird gezeigt, wie die [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Methode und die [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) -Methode verwendet werden, um einen Zeiger auf die [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Schnittstelle zu erhalten, die Zugriff auf die Klassendefinition bietet.

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                  &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  Erstellen Sie die neue-Instanz, indem Sie die [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) -Methode aufrufen.

    Im folgenden Codebeispiel wird gezeigt, wie Sie eine neue-Instanz erstellen und dann die-Klasse freigeben.

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  Legen Sie Werte für alle Eigenschaften fest, die die Werte, die für die Klasse definiert sind, durch Aufrufen der Methode [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) nicht erben.

    Jede Instanz einer Klasse erbt alle Eigenschaften, die für die Klasse definiert sind. Sie können jedoch andere Eigenschaftswerte angeben, wenn Sie auswählen.

    Wenn die vorhandene Klasse über eine Schlüsseleigenschaft verfügt, sollten Sie die-Eigenschaft entweder auf **null** oder einen garantierten eindeutigen Wert festlegen. Wenn Sie den Schlüssel auf **null** festlegen und der Schlüssel eine Zeichenfolge ist, generiert [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) oder [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) intern eine GUID und weist Sie dem Schlüssel zu. Auf diese Weise können Sie bei Angabe von **null** für eine Schlüsseleigenschaft eine eindeutige-Instanz erstellen, die keine vorherige Instanz überschreibt.

    Im folgenden Codebeispiel wird veranschaulicht, wie der Wert der [**Index**](swbemrefreshableitem-index.md) Eigenschaft der Instanzklasse example festgelegt wird.

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);
    ```

    

4.  Legen Sie die Werte für alle relevanten Qualifizierer durch einen Befehl von [**IWbemClassObject:: getqualifierset**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset)fest.

    Die [**getqualifierset**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) -Methode gibt einen Zeiger auf eine [**iwbemqualifierset**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) -Schnittstelle zurück, die für den Zugriff auf die Qualifizierer für eine Klasse oder eine Instanz verwendet. Sie können unterschiedliche Werte für einen Qualifizierer angeben, der für die Klasse definiert ist, wenn die klassenqualifizierungskonfiguration **EnableOverride** Klassen Qualifizierer können nicht geändert oder gelöscht werden  Weitere Informationen finden Sie unter [qualifizierervarianten](qualifier-flavors.md).

    Optional können Sie auch zusätzliche Qualifizierer für Ihre Instanzklasse definieren. Sie können zusätzliche Qualifizierer für die Instanz oder die Instanzeigenschaft definieren, die nicht in der Klassen Deklaration enthalten sein müssen.

5.  Speichern Sie die Instanz, indem Sie die [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) -Methode oder die [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) -Methode aufrufen.

    WMI speichert die Instanz im aktuellen WMI-Namespace. Daher ist der vollständige Pfad der-Instanz vom-Namespace abhängig, bei dem es sich in der Regel um einen Stamm \\ Standard handelt. Für dieses Codebeispiel lautet der vollständige Pfadname \\ \\ . \\ root \\ Default: example. Index = "IX100".

    Im folgenden Codebeispiel wird gezeigt, wie eine-Instanz gespeichert wird.

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

Das Speichern der Instanz in WMI sperrt mehrere der Eigenschaften der Instanz.

Vor allem können Sie die folgenden Vorgänge nicht über die WMI-API ausführen, nachdem eine Instanz in der WMI-Infrastruktur vorhanden ist:

-   Ändern Sie die übergeordnete Klasse der Klasse, zu der die Instanz gehört.
-   Eigenschaften hinzufügen oder entfernen.
-   Ändern Sie die Eigenschafts Typen.
-   [**Schlüssel**](standard-qualifiers.md) oder **indizierte** Qualifizierer hinzufügen oder entfernen.
-   Fügen Sie [**Singleton**](standard-wmi-qualifiers.md)-, **dynamische** oder [**abstrakte**](standard-qualifiers.md) Qualifizierer hinzu oder entfernen Sie Sie.

Im folgenden Codebeispiel werden die Codebeispiele kombiniert, die im vorherigen Verfahren erläutert wurden, um zu veranschaulichen, wie eine-Instanz mithilfe der WMI-API erstellt wird.


```C++
void CreateInstance (IWbemServices *pSvc)
{
    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    // Get the class definition.
    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                 &pExampleClass, &pResult);
    SysFreeString(PathToClass);

    if (hRes != 0)
       return;

    // Create a new instance.
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more

    VARIANT v;
    VariantInit(&v);

    // Set the Index property (the key).
    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);

    // Set the IntVal property.
    V_VT(&v) = VT_I4;
    V_I4(&v) = 1001;  
    
    BSTR Prop = SysAllocString(L"IntVal");
    pNewInstance->Put(Prop, 0, &v, 0);
    SysFreeString(Prop);
    VariantClear(&v);    
    
    // Other properties acquire the 'default' value specified
    // in the class definition unless otherwise modified here.

    // Write the instance to WMI. 
    hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
    pNewInstance->Release();
}
```



 

 



