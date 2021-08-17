---
description: Das Erstellen einer abgeleiteten Klasse in WMI ähnelt dem Erstellen einer Basisklasse. Wie bei einer Basisklasse müssen Sie zuerst die abgeleitete Klasse definieren und dann die abgeleitete Klasse bei WMI registrieren.
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: Erstellen einer abgeleiteten WMI-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cddc2b381346b2765e836bb3606cc06845280c41a7505b872098f383ac0409c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374870"
---
# <a name="creating-a-wmi-derived-class"></a>Erstellen einer abgeleiteten WMI-Klasse

Das Erstellen einer abgeleiteten Klasse in WMI ähnelt dem Erstellen einer Basisklasse. Wie bei einer Basisklasse müssen Sie zuerst die abgeleitete Klasse definieren und dann die abgeleitete Klasse bei WMI registrieren. Der Hauptunterschied besteht darin, dass Sie zuerst die übergeordnete Klasse suchen müssen, von der Sie ableiten möchten. Weitere Informationen finden Sie unter [Schreiben eines Klassenanbieters](writing-a-class-provider.md) und [Schreiben eines Instanzanbieters.](writing-an-instance-provider.md)

Es wird empfohlen, Klassen für einen Anbieter in MOF-Dateien (Managed Object Format) zu erstellen. Mehrere abgeleitete Klassen, die miteinander in Beziehung stehen, sollten zusammen mit allen Basisklassen, von denen sie Eigenschaften oder Methoden ableiten, in einer MOF-Datei gruppiert werden. Wenn Sie jede Klasse in einer separaten MOF-Datei platzieren, muss jede Datei kompiliert werden, bevor der Anbieter ordnungsgemäß funktioniert.

Nachdem Sie die Klasse erstellt haben, müssen Sie alle Instanzen der Klasse löschen, bevor Sie eine der folgenden Aktivitäten für Die abgeleitete Klasse ausführen können:

-   Ändern Sie die übergeordnete Klasse ihrer abgeleiteten Klasse.
-   Hinzufügen oder Entfernen von Eigenschaften.
-   Ändern Von Eigenschaftstypen.
-   Hinzufügen oder Entfernen von [**Schlüssel-**](key-qualifier.md) oder **indizierten** Qualifizierern.
-   Hinzufügen oder Entfernen von [**Singleton-,**](standard-wmi-qualifiers.md) **Dynamic-** oder Abstract-Qualifizierern. [](standard-qualifiers.md)

> [!Note]  
> Um eine Eigenschaft oder einen Qualifizierer hinzuzufügen, zu entfernen oder zu ändern, rufen [**Sie IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) oder [**SWbemObject.Put \_**](swbemobject-put-.md) auf, und legen Sie den Flagparameter auf "Force Mode" fest. Der [](standard-qualifiers.md) Abstract-Qualifizierer kann nur verwendet werden, wenn die übergeordnete Klasse abstrakt ist.

 

Beachten Sie beim Deklarieren der abgeleiteten Klasse die folgenden Regeln und Einschränkungen:

-   Die übergeordnete Klasse der abgeleiteten Klasse muss bereits vorhanden sein.

    Die Deklaration der übergeordneten Klasse kann in derselben MOF-Datei wie die abgeleitete Klasse oder in einer anderen Datei angezeigt werden. Wenn die übergeordnete Klasse unbekannt ist, generiert der Compiler einen Laufzeitfehler.

-   Eine abgeleitete Klasse kann nur über eine einzelne übergeordnete Klasse verfügen.

    WMI unterstützt keine mehrfache Vererbung. Eine übergeordnete Klasse kann jedoch über viele abgeleitete Klassen verfügen.

-   Sie können Indizes für abgeleitete Klassen definieren, aber WMI verwendet diese Indizes nicht.

    Daher verbessert das Angeben eines Indexes für eine abgeleitete Klasse die Leistung von Abfragen für Instanzen der abgeleiteten Klasse nicht. Sie können die Leistung einer Abfrage für eine abgeleitete Klasse verbessern, indem Sie indizierte Eigenschaften für die übergeordnete Klasse der abgeleiteten Klasse angeben.

-   Abgeleitete Klassendefinitionen können komplexer sein und Features wie Aliase, Qualifizierer und Qualifizierer-Varianten enthalten.

    Weitere Informationen finden Sie unter [Erstellen eines Alias](creating-an-alias.md) und Hinzufügen eines [Qualifizierers.](adding-a-qualifier.md)

-   Wenn Sie einen Qualifizierer ändern, den Standardwert einer Basisklasseneigenschaft ändern oder einen Verweis oder eine eingebettete Objekteigenschaft einer Basisklasse stärker eingeben möchten, müssen Sie die gesamte Basisklasse erneut deklarieren.
-   Die maximale Anzahl von Eigenschaften, die Sie in einer WMI-Klasse definieren können, ist 1024.

> [!Note]  
> Klassen können während der Ausführung von Anbietern nicht geändert werden. Sie müssen die Aktivität beenden, die -Klasse ändern und dann den Windows-Verwaltungsdienst neu starten. Das Erkennen einer Klassenänderung ist derzeit nicht möglich.

 

Wie bei der Basisklasse wird dieses Verfahren am häufigsten von Clientanwendungen verwendet. Ein Anbieter kann jedoch auch eine abgeleitete Klasse erstellen. Weitere Informationen finden Sie unter [Erstellen einer Basisklasse](creating-a-base-class.md) und [Schreiben eines Klassenanbieters.](writing-a-class-provider.md)

Das Codebeispiel in diesem Thema erfordert die folgende \# include-Anweisung, um ordnungsgemäß zu kompilieren.


```C++
#include <wbemidl.h>
```



Im folgenden Verfahren wird beschrieben, wie Sie eine abgeleitete Klasse mit C++ erstellen.

**So erstellen Sie eine abgeleitete Klasse mit C++**

1.  Suchen Sie die Basisklasse mit einem Aufruf von [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

    Das folgende Codebeispiel zeigt, wie Sie die Beispielbasisklasse suchen.

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewDerivedClass = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  Erstellen Sie ein abgeleitetes Objekt aus der Basisklasse mit einem Aufruf von [**IWbemClassObject::SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).

    Das folgende Codebeispiel zeigt, wie ein abgeleitetes Klassenobjekt erstellt wird.

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  Richten Sie einen Namen für die Klasse ein, indem Sie die **\_ \_ CLASS-Systemeigenschaft** mit einem Aufruf der [**IWbemClassObject::P ut-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) festlegen.

    Das folgende Codebeispiel zeigt, wie der abgeleiteten Klasse ein Name zugewiesen wird.

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"Example2");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewDerivedClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

4.  Erstellen Sie zusätzliche Eigenschaften mit [**IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Das folgende Codebeispiel zeigt, wie zusätzliche Eigenschaften erstellt werden.

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  Speichern Sie die neue Klasse, indem [**Sie IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)aufrufen.

    Das folgende Codebeispiel zeigt, wie die neue abgeleitete Klasse gespeichert wird.

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

Im folgenden Codebeispiel werden die in der vorherigen Prozedur beschriebenen Codebeispiele kombiniert, um zu beschreiben, wie eine abgeleitete Klasse mithilfe der WMI-API erstellt wird.


```C++
void CreateDerivedClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewDerivedClass = 0;
  IWbemClassObject *pExampleClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  BSTR PathToClass = SysAllocString(L"Example");
  HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
    &pExampleClass, &pResult);
  SysFreeString(PathToClass);

  if (hRes != 0)
    return;

  pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
  pExampleClass->Release();  // The parent class is no longer needed

  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // =====================

  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example2");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewDerivedClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create another property.
  // =======================
  BSTR OtherProp = SysAllocString(L"OtherInfo2");
  // No default value
  pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
  SysFreeString(OtherProp);
  
  // Register the class with WMI. 
  // ============================
  hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
  pNewDerivedClass->Release();
}
```



Das folgende Verfahren beschreibt, wie eine abgeleitete Klasse mithilfe von MOF-Code definiert wird.

**So definieren Sie eine abgeleitete Klasse mit MOF-Code**

1.  Definieren Sie Ihre abgeleitete Klasse mit dem **Schlüsselwort Class,** gefolgt vom Namen der abgeleiteten Klasse und dem Namen der übergeordneten Klasse, die durch einen Doppelpunkt getrennt ist.

    Im folgenden Codebeispiel wird eine Implementierung einer abgeleiteten Klasse beschrieben.

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32   dwProp1;
        uint32       dwProp2;
    };

    class MyDerivedClass : MyClass
    {
        string   strDerivedProp;
        sint32   dwDerivedProp;
    };
    ```

2.  Kompilieren Sie nach Abschluss des Vorgangs Ihren MOF-Code mit dem MOF-Compiler.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien.](compiling-mof-files.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Klasse](creating-a-class.md)
</dt> </dl>

 

 



