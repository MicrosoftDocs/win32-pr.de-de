---
description: Sie können eine Instanz in C++ über die IWbemServices-Schnittstelle erstellen.
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: Erstellen und Deklarieren einer Instanz mit C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046c8c32944c7b726e09eade2701f8d35c9edb0363635eca2a16f7e3d630799a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568799"
---
# <a name="creating-and-declaring-an-instance-using-c"></a>Erstellen und Deklarieren einer Instanz mit C++

Sie können eine Instanz in C++ über die [**IWbemServices-Schnittstelle**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) erstellen.

Die Codebeispiele in diesem Thema erfordern die folgende \# include-Anweisung, um ordnungsgemäß zu kompilieren.


```C++
#include <wbemidl.h>
```



Im folgenden Verfahren wird beschrieben, wie eine Instanz einer vorhandenen Klasse erstellt wird.

**So erstellen Sie eine Instanz einer vorhandenen Klasse**

1.  Rufen Sie die Definition der vorhandenen Klasse ab, indem Sie die [**Methoden IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) aufrufen.

    Im folgenden Codebeispiel wird gezeigt, wie sie die [**Methoden GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) und [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) verwenden, um einen Zeiger auf die [**IWbemClassObject-Schnittstelle**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) abzurufen, die Zugriff auf die Klassendefinition bietet.

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

    

2.  Erstellen Sie die neue Instanz, indem Sie die [**IWbemClassObject::SpawnInstance-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) aufrufen.

    Das folgende Codebeispiel zeigt, wie Sie eine neue -Instanz erstellen und dann die -Klasse freigeben.

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  Legen Sie Werte für eigenschaften fest, die die für die Klasse definierten Werte nicht erben, indem Sie die [**IWbemClassObject::P ut-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) aufrufen.

    Jede Instanz einer Klasse erbt alle Eigenschaften, die für die Klasse definiert sind. Sie können jedoch bei Bedarf unterschiedliche Eigenschaftswerte angeben.

    Wenn die vorhandene Klasse über eine Schlüsseleigenschaft verfügt, sollten Sie die Eigenschaft entweder auf **NULL** oder einen garantierten eindeutigen Wert festlegen. Wenn Sie den Schlüssel auf **NULL** festlegen und der Schlüssel eine Zeichenfolge ist, generiert [**putInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) oder [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) intern eine GUID und weist dem Schlüssel eine GUID zu. Auf diese Weise können Sie durch Angeben von **NULL** für eine Schlüsseleigenschaft eine eindeutige Instanz erstellen, die keine vorherige Instanz überschreibt.

    Das folgende Codebeispiel zeigt, [](swbemrefreshableitem-index.md) wie der Index-Eigenschaftswert der Beispielinstanzklasse festgelegt wird.

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

    

4.  Legen Sie die Werte für alle relevanten Qualifizierer durch einen Aufruf von [**IWbemClassObject::GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset)fest.

    Die [**GetQualifierSet-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) gibt einen Zeiger auf eine [**IWbemQualifierSet-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) zurück, die verwendet, um auf die Qualifizierer für eine Klasse oder Instanz zuzugreifen. Sie können unterschiedliche Werte für einen für die Klasse definierten Qualifizierer angeben, wenn der Typ des Klassenqualifizierers **EnableOverride** ist. Sie können einen Klassenqualifizierer nicht ändern oder löschen, wenn die Variante auf **DisableOverride** festgelegt ist. Weitere Informationen finden Sie unter [Qualifier Flavors](qualifier-flavors.md).

    Optional können Sie auch zusätzliche Qualifizierer für Ihre Instanzklasse definieren. Sie können zusätzliche Qualifizierer für die Instanz- oder Instanzeigenschaft definieren, die nicht in der Klassendeklaration angezeigt werden müssen.

5.  Speichern Sie die Instanz, indem Sie die [**IWbemServices::P utInstance-**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) oder [**IWbemServices::P utInstanceAsync-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) aufrufen.

    WMI speichert die Instanz im aktuellen WMI-Namespace. Daher ist der vollständige Pfad der Instanz vom Namespace abhängig, der in der Regel der \\ Stammstandard ist. In diesem Codebeispiel lautet der vollständige Pfadname \\ \\ . \\ root \\ default:Example.Index="IX100".

    Das folgende Codebeispiel zeigt, wie eine -Instanz gespeichert wird.

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

Durch das Speichern der Instanz in WMI werden mehrere Eigenschaften der Instanz gesperrt.

Insbesondere können Sie keine der folgenden Vorgänge über die WMI-API ausführen, nachdem eine Instanz innerhalb der WMI-Infrastruktur vorhanden ist:

-   Ändern Sie die übergeordnete Klasse der Klasse, zu der die Instanz gehört.
-   Hinzufügen oder Entfernen von Eigenschaften.
-   Ändern Von Eigenschaftstypen.
-   Hinzufügen oder Entfernen von [**Schlüssel-**](standard-qualifiers.md) oder **indizierten** Qualifizierern.
-   Hinzufügen oder Entfernen von [**Singleton-,**](standard-wmi-qualifiers.md) **Dynamic-** oder Abstract-Qualifizierern. [](standard-qualifiers.md)

Im folgenden Codebeispiel werden die im vorherigen Verfahren erläuterten Codebeispiele kombiniert, um zu zeigen, wie eine -Instanz mithilfe der WMI-API erstellt wird.


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



 

 



