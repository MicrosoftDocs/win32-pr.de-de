---
description: Ein Instanzobjektpfad beschreibt den Speicherort einer Instanz einer bestimmten Klasse innerhalb eines bestimmten Namespace.
ms.assetid: 78a194f0-cd21-4622-9242-be7e430b96c0
ms.tgt_platform: multiple
title: Beschreiben eines Instanzobjektpfads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a152d68390c899709cfe6041bfa2880482a0d4498dc371aafd4426aef8f14489
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412060"
---
# <a name="describing-an-instance-object-path"></a>Beschreiben eines Instanzobjektpfads

Ein Instanzobjektpfad beschreibt den Speicherort einer Instanz einer bestimmten Klasse innerhalb eines bestimmten Namespace.

Sie können über verschiedene Arten von Instanzobjektpfaden verfügen:

-   Vollständig

    Ein vollständiger Instanzobjektpfad fügt den Namen und wert der Schlüsseleigenschaft für die Klasse an einen vollständigen Klassenobjektpfad an.

    Das folgende Beispiel zeigt die Definition des vollständigen Instanzobjektpfads.

    ``` syntax
    \\Server\Namespace:Class.KeyName="KeyValue"
    ```

-   Relativ

    Ein relativer Objektpfad bezieht sich auf eine Instanz, die sich im aktuellen Namespace auf dem aktuellen Server befindet. Der relative Pfad besteht aus dem Klassennamen, gefolgt von den Namen und Werten der Schlüsseleigenschaften dieser Instanz.

    Das folgende Beispiel zeigt die Definition des relativen Instanzobjektpfads.

    ``` syntax
    MyClass.MyProp="e:"
    ```

-   Relativ mit einem einzelnen Schlüssel

    Für Klassen mit nur einer Eigenschaft, die als Schlüssel festgelegt ist, können Sie den Namen der Schlüsseleigenschaft weglassen.

    Das folgende Beispiel zeigt die Definition des relativen Instanzobjektpfads mit einem einzelnen Schlüssel.

    ``` syntax
    MyClass="e:"
    ```

-   Relativ mit mehreren Schlüsseln

    Verwenden Sie ein Komma, um zwischen den Schlüsseln einer Instanz mit mehreren Schlüsseln zu unterscheiden.

    Das folgende Beispiel zeigt die Definitionen des relativen Instanzobjektpfads mit mehreren Schlüsseln.

    ``` syntax
    MyOtherClass.FirstKey=1,SecondKey=2
    ```

-   Relativ für eine Singletonklasse

    Der relative Objektpfad für eine Singletonklasse besteht aus dem Klassennamen, gefolgt von der Notation "=@".

    Das folgende Beispiel zeigt die Definition des relativen Instanzobjektpfads für eine Singletonklasse.

    ``` syntax
    MySingletonClass=@
    ```

Im folgenden Verfahren wird beschrieben, wie eine Klasseninstanz abgerufen wird.

**So rufen Sie eine Klasseninstanz ab**

1.  Initialisieren Sie eine Zeichenfolge, die den Objektpfad enthält, mit einem Aufruf der [**SysAllocString-Funktion.**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
2.  Initialisieren Sie ein -Objekt, das die -Instanz empfängt.
3.  Rufen Sie das -Objekt mit einem Aufruf von [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)ab.

    Um [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)zu verwenden, müssen Sie die [**IWbemSink-Schnittstelle**](swbemsink.md) implementieren.

Die folgende \# include-Anweisung ist erforderlich, damit der Code, der weiter unten in diesem Thema aufgeführt ist, ordnungsgemäß kompiliert werden kann.


```C++
#include <wbemidl.h>
```



Im folgenden Codebeispiel wird beschrieben, wie eine Klasseninstanz mithilfe eines Objektpfads abgerufen wird.


```C++
IWbemServices* pWbemSvcs = 0;

BSTR Path = SysAllocString(L"ComPort=2");    
IWbemClassObject *pComPort = 0;
pWbemSvcs->GetObject(Path, 0, 0, &pComPort, 0);
```



Für Instanzen von Klassen, die mehrere Eigenschaften als Schlüssel angeben, erfordert WMI keine bestimmte Reihenfolge von Schlüsseleigenschaften in Objektpfaden. Sie müssen nur den Wert der einzelnen Eigenschaften im Objektpfad angeben.

Im folgenden Codebeispiel werden zwei äquivalente Schlüsselbeschreibungen beschrieben.

``` syntax
MyClass.IntVal=33,StrVal="AAA"
MyClass.StrVal="AAA",IntVal=33
```

 

 
