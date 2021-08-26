---
description: Die empfohlene Methode zum Erstellen einer neuen WMI-Basisklasse für einen WMI-Anbieter ist eine Managed Object Format(MOF)-Datei.
ms.assetid: d46060aa-77c3-4f51-b4a7-2c3612f2bc5c
ms.tgt_platform: multiple
title: Erstellen einer WMI-Basisklasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4780279f00eea403b330400c490da75adfa097406796cd0b14f15f9861411bfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071510"
---
# <a name="creating-a-wmi-base-class"></a>Erstellen einer WMI-Basisklasse

Die empfohlene Methode zum Erstellen einer neuen WMI-Basisklasse für einen WMI-Anbieter ist eine Managed Object Format(MOF)-Datei. Sie können auch eine Basisklasse mithilfe der [COM-API für WMI erstellen.](com-api-for-wmi.md) Sie können zwar eine Basisklasse oder eine abgeleitete Klasse im Skript erstellen, ohne dass ein Anbieter Daten für die Klasse und deren Unterklassen anfing, aber die -Klasse ist nicht nützlich.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Erstellen einer Basisklasse mit MOF](#creating-a-base-class-using-mof)
-   [Erstellen einer Basisklasse mit C++](#creating-a-base-class-with-c)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-a-base-class-using-mof"></a>Erstellen einer Basisklasse mit MOF

WMI-Klassen basieren in der Regel auf Vererbung. Überprüfen Sie vor dem Erstellen einer Basisklasse die Common Information Model (CIM), die von der Distributed Management Task Force[(DMTF)](https://www.dmtf.org/)verfügbar sind.

Wenn viele abgeleitete Klassen die gleichen Eigenschaften verwenden, legen Sie diese Eigenschaften und Methoden in Ihrer Basisklasse ab. Die maximale Anzahl von Eigenschaften, die Sie in einer WMI-Klasse definieren können, ist 1024.

Beachten Sie beim Erstellen einer Basisklasse die folgende Liste von Richtlinien für Klassennamen:

-   Verwenden Sie Groß- und Kleinbuchstaben.
-   Beginnen Sie einen Klassennamen mit einem Buchstaben.
-   Verwenden Sie weder einen führenden noch einen nachdenkenden Unterstrich.
-   Definieren Sie alle verbleibenden Zeichen als Buchstaben, Ziffern oder Unterstriche.
-   Verwenden Sie eine konsistente Benennungskonvention.

    Obwohl es nicht notwendig ist, ist eine gute Namenskonvention für eine Klasse zwei Komponenten, die durch einen Unterstrich verbunden sind. Nach Möglichkeit sollte ein Herstellername die erste Hälfte des Namens und ein beschreibender Klassenname der zweite Teil sein.

> [!Note]  
> Klassen können während der Ausführung von Anbietern nicht geändert werden. Sie müssen die Aktivität beenden, die -Klasse ändern und dann den Windows-Verwaltungsdienst neu starten. Das Erkennen einer Klassenänderung ist derzeit nicht möglich.

 

Erstellen Sie in MOF eine Basisklasse, indem Sie sie mit dem Class-Schlüsselwort benennen, aber keine übergeordnete Klasse angeben. 

**So erstellen Sie eine Basisklasse mit MOF-Code**

1.  Verwenden Sie **das Schlüsselwort class** mit dem Namen der neuen Klasse, gefolgt von einem Paar geschweifter Klammern und einem Semikolon. Fügen Sie Eigenschaften und Methoden für die -Klasse zwischen den geschweiften Klammern hinzu. Das folgende Codebeispiel wird bereitgestellt.

    Das folgende Codebeispiel zeigt, wie eine Basisklasse definiert werden soll.

    ``` syntax
    class MyClass_BaseDisk
    {
    };
    ```

    Das folgende Codebeispiel zeigt eine falsche Definition einer Basisklasse.

    ``` syntax
    class MyClass_BaseDisk : CIM_LogicalDisk
    {
    };
    ```

2.  Fügen Sie [*klassenqualifizierer vor*](gloss-q.md) dem Class-Schlüsselwort hinzu, um die Verwendung der Klasse zu ändern. Platzieren Sie die Qualifizierer zwischen eckigen Klammern. Weitere Informationen zu Qualifizierern zum Ändern von Klassen finden Sie unter [WMI-Qualifizierer](wmi-qualifiers.md). Verwenden Sie den Abstract-Qualifizierer, um anzugeben, dass Sie keine Instanz dieser Klasse direkt erstellen können.  Abstrakte Klassen werden häufig verwendet, um Eigenschaften oder Methoden zu definieren, die von mehreren abgeleiteten Klassen verwendet werden. Weitere Informationen finden Sie unter [Erstellen einer abgeleiteten Klasse.](creating-a-derived-class.md)

    Im folgenden Codebeispiel wird die -Klasse als abstrakt definiert und der Anbieter definiert, der die Daten liefert. Die ToSubClass-Qualifizierer-Variante gibt an, dass die Informationen im **Anbieterqualifizierer** von abgeleiteten Klassen geerbt werden.  [](gloss-f.md)

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  Fügen Sie die Eigenschaften und Methoden für die Klasse in eckigen Klammern vor dem Eigenschaften- oder Methodennamen hinzu. Weitere Informationen finden Sie unter [Hinzufügen einer Eigenschaft und](adding-a-property.md) Erstellen einer [Methode.](creating-a-method.md) Sie können diese Eigenschaften und Methoden mithilfe von MOF-Qualifizierern ändern. Weitere Informationen finden Sie unter [Hinzufügen eines Qualifizierers.](adding-a-qualifier.md)

    Das folgende Codebeispiel zeigt, wie Eigenschaften und Methoden mit MOF-Qualifizierern geändert werden.

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  Speichern Sie die MOF-Datei mit der Erweiterung MOF.
5.  Registrieren Sie die -Klasse bei WMI, indem [**Mofcomp.exe**](mofcomp.md) für die Datei ausführen.

    **mofcomp.exe** *newmof.mof*

    Wenn Sie nicht den Schalter **-N** oder den Pragmanamespace des Präprozessorbefehls verwenden, um einen Namespace anzugeben, werden die kompilierten MOF-Klassen im Stamm-Standardnamespace im Repository \# [](pragma-namespace.md) \\ gespeichert. Weitere Informationen finden Sie unter [**mofcomp**](mofcomp.md).

Im folgenden Codebeispiel werden die im vorherigen Verfahren erläuterten MOF-Codebeispiele kombiniert, und es wird gezeigt, wie sie eine Basisklasse im Cimv2-Stammnamespace mit \\ MOF erstellen.

``` syntax
#pragma namespace("\\\\.\\Root\\cimv2")

[Abstract, Provider("MyProvider") : ToSubClass]
class MyClass_BaseDisk
{
  [read : ToSubClass, key : ToSubClass ] string DeviceID;
  [read : ToSubClass] uint32 State;
  [read : ToSubClass, write : ToSubClass] uint64 LimitUsers;
};
```

Weitere Informationen finden Sie unter [Erstellen einer abgeleiteten Klasse](creating-a-derived-class.md) für ein Beispiel für eine dynamische Klasse, die von dieser Basisklasse abgeleitet wurde.

## <a name="creating-a-base-class-with-c"></a>Erstellen einer Basisklasse mit C++

Das Erstellen einer Basisklasse mithilfe der WMI-API besteht hauptsächlich aus einer Reihe von Put-Befehlen, die die Klasse definieren und die Klasse bei WMI registrieren. Der Hauptzweck dieser API ist es, Clientanwendungen das Erstellen von Basisklassen zu ermöglichen. Sie können jedoch auch einen Anbieter haben, der diese API verwendet, um eine Basisklasse zu erstellen. Wenn Sie beispielsweise der Meinung sind, dass der MOF-Code für Ihren Anbieter nicht ordnungsgemäß installiert wird, können Sie Ihren Anbieter anweisen, automatisch die richtigen Klassen im WMI-Repository zu erstellen. Weitere Informationen zu Anbietern finden Sie unter [Schreiben eines Klassenanbieters.](writing-a-class-provider.md)

> [!Note]  
> Klassen können während der Ausführung von Anbietern nicht geändert werden. Sie müssen die Aktivität beenden, die -Klasse ändern und dann den Windows-Verwaltungsdienst neu starten. Das Erkennen einer Klassenänderung ist derzeit nicht möglich.

 

Der Code erfordert den folgenden Verweis, um ordnungsgemäß zu kompilieren.


```C++
#include <wbemidl.h>
```



Sie können eine neue Basisklasse programmgesteuert mithilfe der [COM-API für WMI erstellen.](com-api-for-wmi.md)

**So erstellen Sie eine neue Basisklasse mit der WMI-API**

1.  Rufen Sie eine Definition für die neue Klasse ab, indem Sie die [**IWbemServices::GetObject-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) aufrufen, bei der *der parameter strObjectPath* auf einen **NULL-Wert festgelegt** ist.

    Das folgende Codebeispiel zeigt, wie eine Definition für eine neue Klasse abgerufen wird.

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  Legen Sie einen Namen für die Klasse fest, indem Sie die **\_ \_ CLASS-Systemeigenschaft** mit einem Aufruf der [**IWbemClassObject::P ut-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) festlegen.

    Das folgende Codebeispiel zeigt, wie die Klasse durch Festlegen der **\_ \_ CLASS-Systemeigenschaft bezeichnet** wird.

    ```C++
    VARIANT v;
    VariantInit(&v);
    V_VT(&v) = VT_BSTR;

    V_BSTR(&v) = SysAllocString(L"Example");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

3.  Erstellen Sie die Schlüsseleigenschaft oder die Eigenschaften, indem [**Sie IWbemClassObject::P ut aufrufen.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)

    Im folgenden Codebeispiel wird beschrieben, wie die [**Index-Eigenschaft**](swbemrefreshableitem-index.md) erstellt wird, die in Schritt 4 als Schlüsseleigenschaft bezeichnet wird.

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  Fügen [](standard-qualifiers.md) Sie den Key-Standardqualifizierer an die key-Eigenschaft an, indem Sie zuerst die [**IWbemClassObject::GetPropertyQualifierSet-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) und dann die [**IWbemQualifierSet::P ut-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) aufrufen.

    Das folgende Codebeispiel zeigt, [](standard-qualifiers.md) wie sie den Key-Standardqualifizierer an die Key-Eigenschaft anfügen.

    ```C++
      IWbemQualifierSet *pQual = 0;
      pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
      SysFreeString(KeyProp);

      V_VT(&v) = VT_BOOL;
      V_BOOL(&v) = VARIANT_TRUE;
      BSTR Key = SysAllocString(L"Key");

      pQual->Put(Key, &v, 0);   // Flavors not required for Key 
      SysFreeString(Key);

      // No longer need the qualifier set for "Index"
      pQual->Release();   
      VariantClear(&v);
    ```

    

5.  Erstellen Sie andere Eigenschaften der -Klasse mit [**IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Im folgenden Codebeispiel wird beschrieben, wie zusätzliche Eigenschaften erstellt werden.

    ```C++
      V_VT(&v) = VT_BSTR;
      V_BSTR(&v) = SysAllocString(L"<default>");
      BSTR OtherProp = SysAllocString(L"OtherInfo");
      pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
      SysFreeString(OtherProp);
      VariantClear(&v);

      OtherProp = SysAllocString(L"IntVal");
      pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
      SysFreeString(OtherProp);
    ```

    

6.  Registrieren Sie die neue Klasse, indem [**Sie IWbemServices::P utClass aufrufen.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)

    Da Sie keine Schlüssel und Indizes definieren können, nachdem Sie eine neue Klasse registriert haben, stellen Sie sicher, dass Sie alle Eigenschaften definiert haben, bevor [**Sie PutClass aufrufen.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)

    Im folgenden Codebeispiel wird beschrieben, wie eine neue Klasse registriert wird.

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

Im folgenden Codebeispiel werden die im vorherigen Verfahren erläuterten Codebeispiele kombiniert, und es wird gezeigt, wie sie mithilfe der WMI-API eine Basisklasse erstellen.


```C++
void CreateClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  // Get a class definition. 
  // ============================
  HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create the key property. 
  // ============================
  BSTR KeyProp = SysAllocString(L"Index");
  pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);

  // Attach Key qualifier to mark the "Index" property as the key.
  // ============================
  IWbemQualifierSet *pQual = 0;
  pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
  SysFreeString(KeyProp);

  V_VT(&v) = VT_BOOL;
  V_BOOL(&v) = VARIANT_TRUE;
  BSTR Key = SysAllocString(L"Key");

  pQual->Put(Key, &v, 0);   // Flavors not required for Key 
  SysFreeString(Key);

  // No longer need the qualifier set for "Index"
  pQual->Release();     
  VariantClear(&v);

  // Create other properties.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"<default>");
  BSTR OtherProp = SysAllocString(L"OtherInfo");
  pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
  SysFreeString(OtherProp);
  VariantClear(&v);

  OtherProp = SysAllocString(L"IntVal");
  pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
  SysFreeString(OtherProp);
  
  // Register the class with WMI
  // ============================
  hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
  pNewClass->Release();
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Klasse](creating-a-class.md)
</dt> </dl>

 

 



