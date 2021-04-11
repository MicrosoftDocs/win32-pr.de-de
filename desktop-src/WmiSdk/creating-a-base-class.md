---
description: Die empfohlene Vorgehensweise zum Erstellen einer neuen WMI-Basisklasse für einen WMI-Anbieter befindet sich in einer MOF-Datei (Managed Object Format).
ms.assetid: d46060aa-77c3-4f51-b4a7-2c3612f2bc5c
ms.tgt_platform: multiple
title: Erstellen einer WMI-Basisklasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebdcbe6995a7782d854a4d0950db841f23a30b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960617"
---
# <a name="creating-a-wmi-base-class"></a>Erstellen einer WMI-Basisklasse

Die empfohlene Vorgehensweise zum Erstellen einer neuen WMI-Basisklasse für einen WMI-Anbieter befindet sich in einer MOF-Datei (Managed Object Format). Sie können auch eine Basisklasse mithilfe der [com-API für WMI](com-api-for-wmi.md)erstellen. Obwohl Sie eine Basisklasse oder eine abgeleitete Klasse im Skript erstellen können, ohne dass ein Anbieter Daten für die Klasse und deren Unterklassen bereitstellt, ist die Klasse nicht nützlich.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Erstellen einer Basisklasse mithilfe von MOF](#creating-a-base-class-using-mof)
-   [Erstellen einer Basisklasse mit C++](#creating-a-base-class-with-c)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-a-base-class-using-mof"></a>Erstellen einer Basisklasse mithilfe von MOF

WMI-Klassen basieren in der Regel auf Vererbung. Überprüfen Sie vor dem Erstellen einer Basisklasse die in der[DMTF](https://www.dmtf.org/)(verteilte Management Task Force) verfügbaren Common Information Model (CIM)-Klassen.

Wenn viele abgeleitete Klassen die gleichen Eigenschaften verwenden, platzieren Sie diese Eigenschaften und Methoden in ihrer Basisklasse. Die maximale Anzahl von Eigenschaften, die Sie in einer WMI-Klasse definieren können, ist 1024.

Beachten Sie beim Erstellen einer Basisklasse die folgende Liste von Richtlinien für Klassennamen:

-   Verwenden Sie groß-und Kleinbuchstaben.
-   Beginnen Sie einen Klassennamen mit einem Buchstaben.
-   Verwenden Sie weder einen führenden noch einen nachfolgenden unterstrich.
-   Definieren Sie alle verbleibenden Zeichen als Buchstaben, Ziffern oder Unterstriche.
-   Verwenden Sie eine konsistente Benennungs Konvention.

    Eine gute Benennungs Konvention für eine Klasse ist zwar nicht erforderlich, ist jedoch zwei Komponenten, die mit einem Unterstrich verknüpft sind. Wenn möglich, sollte ein Herstellername die erste Hälfte des Namens ausmachen, und ein beschreibender Klassenname sollte der zweite Teil sein.

> [!Note]  
> Klassen können während der Ausführung von Anbietern nicht geändert werden. Sie müssen die Aktivität abbrechen, die Klasse ändern und dann den Windows-Verwaltungsdienst neu starten. Es ist derzeit nicht möglich, eine Klassen Änderung zu erkennen.

 

Erstellen Sie in MOF eine Basisklasse, indem Sie Sie mit dem Schlüsselwort **Class** benennen, ohne eine übergeordnete Klasse anzugeben.

**So erstellen Sie eine Basisklasse mithilfe von MOF-Code**

1.  Verwenden Sie das **Class** -Schlüsselwort mit dem Namen der neuen Klasse, gefolgt von einem Paar aus geschweiften Klammern und einem Semikolon. Fügen Sie Eigenschaften und Methoden für die-Klasse zwischen den geschweiften Klammern hinzu. Das folgende Codebeispiel wird bereitgestellt.

    Im folgenden Codebeispiel wird gezeigt, wie eine Basisklasse definiert werden muss.

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

2.  Fügen Sie vor dem Schlüsselwort class alle Klassen [*Qualifizierer*](gloss-q.md) hinzu, um die Verwendung der-Klasse zu ändern. Platzieren Sie die Qualifizierer zwischen eckigen Klammern. Weitere Informationen zu Qualifizierern zum Ändern von Klassen finden Sie unter [WMI-Qualifizierer](wmi-qualifiers.md). Verwenden Sie den **abstrakten** Qualifizierer, um anzugeben, dass keine Instanz dieser Klasse direkt erstellt werden kann. Abstrakte Klassen werden häufig verwendet, um Eigenschaften oder Methoden zu definieren, die von mehreren abgeleiteten Klassen verwendet werden. Weitere Informationen finden Sie unter [Erstellen einer abgeleiteten Klasse](creating-a-derived-class.md).

    Im folgenden Codebeispiel wird die-Klasse als abstrakt definiert und der Anbieter definiert, der die Daten bereitstellt. Der " **desubclass** "-qualifiziererwert gibt an, dass die Informationen im **Anbieter Qualifizierer** von abgeleiteten Klassen geerbt werden [](gloss-f.md)

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  Fügen Sie die Eigenschaften und Methoden für die Klasse in eckigen Klammern vor dem Eigenschafts-oder Methodennamen hinzu. Weitere Informationen finden Sie unter [Hinzufügen einer Eigenschaft](adding-a-property.md) und [Erstellen einer Methode](creating-a-method.md). Sie können diese Eigenschaften und Methoden mithilfe von MOF-Qualifizierern ändern. Weitere Informationen finden Sie unter [Hinzufügen eines Qualifizierers](adding-a-qualifier.md).

    Im folgenden Codebeispiel wird gezeigt, wie Eigenschaften und Methoden mit MOF-Qualifizierern geändert werden.

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  Speichern Sie die MOF-Datei mit der Erweiterung. mof.
5.  Registrieren Sie die Klasse bei WMI, indem Sie [**Mofcomp.exe**](mofcomp.md) für die Datei ausführen.

    **mofcomp.exe** *newmof. MOF*

    Wenn Sie den Schalter **-N** oder den Pragma-Namespace des Präprozessorbefehls nicht verwenden \# [](pragma-namespace.md) , um einen Namespace anzugeben, werden die kompilierten MOF-Klassen im Stamm- \\ Standard Namespace im Repository gespeichert. Weitere Informationen finden Sie unter " [**MUF**](mofcomp.md)".

Im folgenden Codebeispiel werden die MOF-Codebeispiele kombiniert, die in der vorherigen Prozedur erläutert wurden, und es wird gezeigt, wie eine Basisklasse im root \\ CIMV2-Namespace mithilfe von MOF erstellt wird.

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

Weitere Informationen finden Sie unter [Erstellen einer abgeleiteten Klasse](creating-a-derived-class.md) für ein Beispiel für eine dynamische Klasse, die von dieser Basisklasse abgeleitet wird.

## <a name="creating-a-base-class-with-c"></a>Erstellen einer Basisklasse mit C++

Das Erstellen einer Basisklasse mithilfe der WMI-API ist hauptsächlich eine Reihe von Put-Befehlen, mit denen die Klasse definiert und die Klasse bei WMI registriert wird. Der Hauptzweck dieser API besteht darin, Client Anwendungen das Erstellen von Basisklassen zu ermöglichen. Sie können jedoch auch einen Anbieter verwenden, um eine Basisklasse mithilfe dieser API zu erstellen. Wenn Sie z. b. der Meinung sind, dass der MOF-Code für den Anbieter nicht ordnungsgemäß installiert wird, können Sie den Anbieter anweisen, automatisch die richtigen Klassen im WMI-Repository zu erstellen. Weitere Informationen zu Anbietern finden Sie unter [Schreiben eines Klassen Anbieters](writing-a-class-provider.md).

> [!Note]  
> Klassen können während der Ausführung von Anbietern nicht geändert werden. Sie müssen die Aktivität abbrechen, die Klasse ändern und dann den Windows-Verwaltungsdienst neu starten. Es ist derzeit nicht möglich, eine Klassen Änderung zu erkennen.

 

Der Code erfordert, dass der folgende Verweis ordnungsgemäß kompiliert wird.


```C++
#include <wbemidl.h>
```



Sie können eine neue Basisklasse mithilfe der [com-API für WMI](com-api-for-wmi.md)Programm gesteuert erstellen.

**So erstellen Sie eine neue Basisklasse mit der WMI-API**

1.  Rufen Sie eine Definition für die neue Klasse ab, indem Sie die [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Methode aufrufen, wobei der Parameter " *strobjectpath* " auf einen **null** -Wert festgelegt ist.

    Im folgenden Codebeispiel wird gezeigt, wie eine Definition für eine neue Klasse abgerufen wird.

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  Richten Sie einen Namen für die Klasse ein, indem Sie die **\_ \_ Klassen** System Eigenschaft mit einem-Befehl für die [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) -Methode festlegen.

    Im folgenden Codebeispiel wird gezeigt, wie die-Klasse durch Festlegen der **\_ \_ Klassen** System-Eigenschaft benennen kann.

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

    

3.  Erstellen Sie die Schlüsseleigenschaft oder die Eigenschaften, indem Sie [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)aufrufen.

    Im folgenden Codebeispiel wird beschrieben, wie die [**Index**](swbemrefreshableitem-index.md) -Eigenschaft erstellt wird, die in Schritt 4 als Schlüsseleigenschaft bezeichnet wird.

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  Fügen Sie den [**Schlüssel**](standard-qualifiers.md) Standard Qualifizierer an die Schlüsseleigenschaft an, indem Sie zuerst die [**IWbemClassObject:: getpropertyqualifierset**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) -Methode und dann die [**iwbemqualifierset::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) -Methode aufrufen.

    Im folgenden Codebeispiel wird gezeigt, wie der [**Schlüssel**](standard-qualifiers.md) Standard Qualifizierer an die Schlüsseleigenschaft angefügt wird.

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

    

5.  Erstellen Sie mit [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)weitere Eigenschaften der Klasse.

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

    

6.  Registrieren Sie die neue Klasse durch Aufrufen von [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    Da Sie nach dem Registrieren einer neuen Klasse keine Schlüssel und Indizes definieren können, stellen Sie sicher, dass Sie alle Eigenschaften vor dem Aufruf von [**putclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)definiert haben.

    Im folgenden Codebeispiel wird beschrieben, wie eine neue Klasse registriert wird.

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

Im folgenden Codebeispiel werden die Codebeispiele kombiniert, die in der vorherigen Prozedur erläutert wurden, und es wird gezeigt, wie Sie eine Basisklasse mithilfe der WMI-API erstellen.


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

 

 



