---
description: Ein instanzobjektpfad beschreibt den Speicherort einer Instanz einer bestimmten Klasse in einem bestimmten Namespace.
ms.assetid: 78a194f0-cd21-4622-9242-be7e430b96c0
ms.tgt_platform: multiple
title: Beschreiben eines instanzobjektpfads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f977359ea9c3c4346052f1edd076c0cce5544441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347048"
---
# <a name="describing-an-instance-object-path"></a>Beschreiben eines instanzobjektpfads

Ein instanzobjektpfad beschreibt den Speicherort einer Instanz einer bestimmten Klasse in einem bestimmten Namespace.

Sie können verschiedene Arten von instanzobjektpfaden haben:

-   Vollständig

    Ein vollständiger instanzobjektpfad fügt den Namen und den Wert der Schlüsseleigenschaft für die Klasse an einen vollständigen Klassenobjekt Pfad an.

    Das folgende Beispiel zeigt die Definition des vollständigen instanzobjektpfads.

    ``` syntax
    \\Server\Namespace:Class.KeyName="KeyValue"
    ```

-   Relativ

    Ein relativer Objekt Pfad verweist auf eine Instanz, die sich im aktuellen Namespace auf dem aktuellen Server befindet. Der relative Pfad besteht aus dem Klassennamen, gefolgt von den Namen und Werten der Schlüsseleigenschaften dieser Instanz.

    Das folgende Beispiel zeigt die Definition des relativen instanzobjektpfads.

    ``` syntax
    MyClass.MyProp="e:"
    ```

-   Relativ zu einem einzelnen Schlüssel

    Für Klassen, die nur eine Eigenschaft als Schlüssel festgelegt haben, können Sie den Namen der Schlüsseleigenschaft weglassen.

    Das folgende Beispiel zeigt die Definition des relativen instanzobjektpfads mit einem einzelnen Schlüssel.

    ``` syntax
    MyClass="e:"
    ```

-   Relativ zu mehreren Schlüsseln

    Verwenden Sie ein Komma, um zwischen den Schlüsseln einer Instanz mit mehreren Schlüsseln zu unterscheiden.

    Das folgende Beispiel zeigt die Definitionen des relativen instanzobjektpfades mit mehreren Schlüsseln.

    ``` syntax
    MyOtherClass.FirstKey=1,SecondKey=2
    ```

-   Relativ für eine Singleton-Klasse

    Der relative Objekt Pfad für eine Singleton-Klasse besteht aus dem Klassennamen, gefolgt von der Notation "= @".

    Das folgende Beispiel zeigt die Definition des relativen instanzobjektpfads für eine Singleton-Klasse.

    ``` syntax
    MySingletonClass=@
    ```

Im folgenden Verfahren wird beschrieben, wie eine Klasseninstanz abgerufen wird.

**So rufen Sie eine Klasseninstanz ab**

1.  Initialisieren Sie eine Zeichenfolge, die den Objekt Pfad mit einem Rückruf der [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) -Funktion enthält.
2.  Initialisieren Sie ein Objekt, das die-Instanz empfängt.
3.  Rufen Sie das-Objekt mit einem Befehl von [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)ab.

    Um [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)zu verwenden, müssen Sie die [**iwbemsink**](swbemsink.md) -Schnittstelle implementieren.

Die folgende \# include-Anweisung ist erforderlich, damit der Code, der weiter unten in diesem Thema aufgelistet ist, ordnungsgemäß kompiliert wird.


```C++
#include <wbemidl.h>
```



Im folgenden Codebeispiel wird beschrieben, wie eine-Klasseninstanz mit einem Objekt Pfad abgerufen wird.


```C++
IWbemServices* pWbemSvcs = 0;

BSTR Path = SysAllocString(L"ComPort=2");    
IWbemClassObject *pComPort = 0;
pWbemSvcs->GetObject(Path, 0, 0, &pComPort, 0);
```



Für Instanzen von Klassen, die mehrere Eigenschaften als Schlüssel angeben, erfordert WMI keine bestimmte Reihenfolge von Schlüsseleigenschaften in Objekt Pfaden. Sie müssen nur den Wert der einzelnen Eigenschaften im Objekt Pfad angeben.

Im folgenden Codebeispiel werden zwei äquivalente Schlüssel Beschreibungen beschrieben.

``` syntax
MyClass.IntVal=33,StrVal="AAA"
MyClass.StrVal="AAA",IntVal=33
```

 

 
