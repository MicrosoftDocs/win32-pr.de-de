---
description: Das Erstellen einer abgeleiteten Klasse in WMI ähnelt stark dem Erstellen einer Basisklasse. Wie bei einer Basisklasse müssen Sie zuerst die abgeleitete Klasse definieren und dann die abgeleitete Klasse bei WMI registrieren.
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: Erstellen einer abgeleiteten WMI-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b65079d206cb7a0a490622018f6d2e2df98867d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345878"
---
# <a name="creating-a-wmi-derived-class"></a>Erstellen einer abgeleiteten WMI-Klasse

Das Erstellen einer abgeleiteten Klasse in WMI ähnelt stark dem Erstellen einer Basisklasse. Wie bei einer Basisklasse müssen Sie zuerst die abgeleitete Klasse definieren und dann die abgeleitete Klasse bei WMI registrieren. Der Hauptunterschied besteht darin, dass Sie zuerst die übergeordnete Klasse suchen müssen, von der abgeleitet werden soll. Weitere Informationen finden Sie unter [Schreiben eines Klassen Anbieters](writing-a-class-provider.md) und [Schreiben eines Instanzanbieters](writing-an-instance-provider.md).

Die empfohlene Vorgehensweise zum Erstellen von Klassen für einen-Anbieter ist in Managed Object Format Dateien (MOF). Mehrere abgeleitete Klassen, die miteinander verknüpft sind, sollten zusammen mit allen Basisklassen, von denen Eigenschaften oder Methoden abgeleitet werden, in eine MOF-Datei gruppiert werden. Wenn Sie jede Klasse in einer separaten MOF-Datei platzieren, muss jede Datei kompiliert werden, bevor der Anbieter ordnungsgemäß funktionieren kann.

Nachdem Sie die Klasse erstellt haben, müssen Sie alle Instanzen der Klasse löschen, bevor Sie eine der folgenden Aktivitäten in der abgeleiteten Klasse ausführen können:

-   Ändern Sie die übergeordnete Klasse ihrer abgeleiteten Klasse.
-   Eigenschaften hinzufügen oder entfernen.
-   Ändern Sie die Eigenschafts Typen.
-   [**Schlüssel**](key-qualifier.md) oder **indizierte** Qualifizierer hinzufügen oder entfernen.
-   Fügen Sie [**Singleton**](standard-wmi-qualifiers.md)-, **dynamische** oder [**abstrakte**](standard-qualifiers.md) Qualifizierer hinzu oder entfernen Sie Sie.

> [!Note]  
> Um eine Eigenschaft oder einen Qualifizierer hinzuzufügen, zu entfernen oder zu ändern, nennen Sie [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) oder [**errbemubject. Put \_**](swbemobject-put-.md) , und legen Sie den Flag-Parameter auf "Force Mode" fest. Der [**abstrakte**](standard-qualifiers.md) Qualifizierer kann nur verwendet werden, wenn die übergeordnete Klasse abstrakt ist.

 

Wenn Sie die abgeleitete Klasse deklarieren, beachten Sie die folgenden Regeln und Einschränkungen:

-   Die übergeordnete Klasse der abgeleiteten Klasse muss bereits vorhanden sein.

    Die Deklaration der übergeordneten Klasse kann in derselben MOF-Datei wie die abgeleitete Klasse oder in einer anderen Datei vorkommen. Wenn die übergeordnete Klasse unbekannt ist, generiert der Compiler einen Laufzeitfehler.

-   Eine abgeleitete Klasse kann nur über eine einzige übergeordnete Klasse verfügen.

    WMI unterstützt keine Mehrfachvererbung. Eine übergeordnete Klasse kann jedoch viele abgeleitete Klassen aufweisen.

-   Sie können Indizes für abgeleitete Klassen definieren, aber WMI verwendet diese Indizes nicht.

    Daher wird durch die Angabe eines Indexes für eine abgeleitete Klasse die Leistung von Abfragen für Instanzen der abgeleiteten Klasse nicht verbessert. Sie können die Leistung einer Abfrage für eine abgeleitete Klasse verbessern, indem Sie indizierte Eigenschaften für die übergeordnete Klasse der abgeleiteten Klasse angeben.

-   Abgeleitete Klassendefinitionen können komplexer sein und Funktionen wie Aliase, Qualifizierer und qualifizierervarianten enthalten.

    Weitere Informationen finden Sie unter [Erstellen eines Alias](creating-an-alias.md) und [Hinzufügen eines Qualifizierers](adding-a-qualifier.md).

-   Wenn Sie einen Qualifizierer ändern, den Standardwert einer Basisklassen Eigenschaft ändern oder eine Verweis-oder eingebettete Objekt Eigenschaft einer Basisklasse stark eingeben möchten, müssen Sie die gesamte Basisklasse erneut deklarieren.
-   Die maximale Anzahl von Eigenschaften, die Sie in einer WMI-Klasse definieren können, ist 1024.

> [!Note]  
> Klassen können während der Ausführung von Anbietern nicht geändert werden. Sie müssen die Aktivität abbrechen, die Klasse ändern und dann den Windows-Verwaltungsdienst neu starten. Es ist derzeit nicht möglich, eine Klassen Änderung zu erkennen.

 

Wie bei der Basisklasse wird diese Technik am häufigsten von Client Anwendungen verwendet. Ein Anbieter kann jedoch auch eine abgeleitete Klasse erstellen. Weitere Informationen finden Sie unter [Erstellen einer Basisklasse](creating-a-base-class.md) und [Schreiben eines Klassen Anbieters](writing-a-class-provider.md).

Das Codebeispiel in diesem Thema erfordert, dass die folgende \# include-Anweisung ordnungsgemäß kompiliert wird.


```C++
#include <wbemidl.h>
```



Im folgenden Verfahren wird beschrieben, wie eine abgeleitete Klasse mit C++ erstellt wird.

**So erstellen Sie eine abgeleitete Klasse mithilfe von C++**

1.  Suchen Sie die Basisklasse mit einem Befehl von [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

    Im folgenden Codebeispiel wird gezeigt, wie Sie die Beispiel Basisklasse finden.

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

    

2.  Erstellen Sie ein abgeleitetes Objekt aus der Basisklasse mit einem-Befehl, der [**IWbemClassObject:: spawnderivedclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass)aufruft.

    Im folgenden Codebeispiel wird gezeigt, wie ein abgeleitetes Klassenobjekt erstellt wird.

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  Richten Sie einen Namen für die Klasse ein, indem Sie die **\_ \_ Klassen** System Eigenschaft mit einem-Befehl für die [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) -Methode festlegen.

    Im folgenden Codebeispiel wird gezeigt, wie der abgeleiteten Klasse ein Name zugewiesen wird.

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

    

4.  Erstellen Sie zusätzliche Eigenschaften mit [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Im folgenden Codebeispiel wird gezeigt, wie zusätzliche Eigenschaften erstellt werden.

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  Speichern Sie die neue Klasse durch Aufrufen von [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    Im folgenden Codebeispiel wird gezeigt, wie die neue abgeleitete Klasse gespeichert wird.

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

Im folgenden Codebeispiel werden die Codebeispiele kombiniert, die im vorherigen Verfahren erläutert wurden, um das Erstellen einer abgeleiteten Klasse mithilfe der WMI-API zu beschreiben.


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



Im folgenden Verfahren wird beschrieben, wie eine abgeleitete Klasse mithilfe von MOF-Code definiert wird.

**So definieren Sie eine abgeleitete Klasse mithilfe von MOF-Code**

1.  Definieren Sie Ihre abgeleitete Klasse mit dem Schlüsselwort **Class** , gefolgt vom Namen der abgeleiteten Klasse und dem Namen der übergeordneten Klasse, getrennt durch einen Doppelpunkt.

    Im folgenden Codebeispiel wird die Implementierung einer abgeleiteten Klasse beschrieben.

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

2.  Kompilieren Sie den MOF-Code nach Abschluss des Vorgangs mit dem MOF-Compiler.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Klasse](creating-a-class.md)
</dt> </dl>

 

 



