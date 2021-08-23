---
description: Um eine WMI-Methode zu erstellen, definieren Sie die Eingabe- und Ausgabeparameter für die Methode.
ms.assetid: 71cbecde-33c4-4bf1-9793-bef6d823dcac
ms.tgt_platform: multiple
title: Erstellen einer WMI-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689f69518f440e7c1983a92fbf86877c5c6dd2149ce2b31b8459aa08b9e94c4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612530"
---
# <a name="creating-a-wmi-method"></a>Erstellen einer WMI-Methode

Um eine WMI-Methode zu erstellen, definieren Sie die Eingabe- und Ausgabeparameter für die Methode. Die Eingabe- und Ausgabeparameter werden durch eine spezielle WMI-Systemklasse [**\_ \_ PARAMETERS**](--parameters.md)dargestellt. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md) und Schreiben eines [Methodenanbieters.](writing-a-method-provider.md)

Die folgenden Abschnitte werden in diesem Thema erläutert:

-   [Erstellen einer WMI-Klassenmethode in MOF](#creating-a-wmi-class-method-in-mof)
-   [Erstellen einer WMI-Klassenmethode in C++](#creating-a-wmi-class-method-in-c)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a>Erstellen einer WMI-Klassenmethode in MOF

In WMI sind Anbietermethoden im Allgemeinen unterschiedliche Aktionen im Zusammenhang mit dem Objekt, das von der -Klasse dargestellt wird. Anstatt den Wert einer Eigenschaft zu ändern, um eine Aktion auszuführen, sollte eine Methode erstellt werden. Beispielsweise können Sie ein Netzwerkinformationscenter (Network Information Center, NIC), das durch [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) dargestellt wird, mithilfe der [**Methoden Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) und [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) aktivieren oder deaktivieren. Diese Aktionen können zwar als Lese-/Schreibeigenschaft dargestellt werden, es wird jedoch empfohlen, eine Methode zu erstellen. Wenn Sie einen Zustand oder Wert für die Klasse sichtbar machen möchten, empfiehlt es sich alternativ, eine Lese-/Schreibeigenschaft anstelle einer Methode zu erstellen. In **Win32 \_ NetworkAdapter** macht die **NetEnabled-Eigenschaft** den Zustand des Adapters sichtbar, aber Änderungen zwischen den Zuständen werden durch die **Enable-** oder **Disable-Methoden** ausgeführt.

Klassendeklarationen können die Deklaration einer oder mehrerer Methoden enthalten. Sie können entweder die Methoden einer übergeordneten Klasse erben oder eine eigene implementieren. Wenn Sie ihre eigenen Methoden implementieren möchten, müssen Sie die Methode deklarieren und die Methode mit bestimmten Qualifizierertags markieren.

Das folgende Verfahren beschreibt, wie eine Methode in einer Klasse deklariert wird, die nicht von einer Basisklasse erbt.

**So deklarieren Sie eine Methode**

1.  Definieren Sie den Namen Ihrer Methode zwischen den geschweiften Klammern einer Klassendeklaration, gefolgt von allen Qualifizierern.

    Im folgenden Codebeispiel wird die Syntax für eine Methode beschrieben.

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  Fügen Sie abschließend Ihren MOF-Code (Managed Object Format) mit einem Aufruf des MOF-Compilers in das WMI-Repository ein.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien.](compiling-mof-files.md)

Die folgende Liste definiert die Elemente der Methodendeklaration.

<dl> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Anbieter**](/windows/desktop/api/Provider/nl-provider-provider)
</dt> <dd>

Verknüpft einen bestimmten Anbieter mit Ihrer Klassenbeschreibung. Der Wert des [**Anbieterqualifizierers**](/windows/desktop/api/Provider/nl-provider-provider) ist der Name des Anbieters, der WMI mitgibt, wo sich der Code befindet, der Die Methode unterstützt. Ein Anbieter sollte auch mit dem **dynamischen** Qualifizierer jede Klasse markieren, die über dynamische Instanzen verfügt. Verwenden Sie im Gegensatz dazu nicht den **dynamischen** Qualifizierer, um eine Klasse zu markieren, die eine statische Instanz mit **implementierten** Methoden enthält.

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implementiert**
</dt> <dd>

Deklariert, dass Sie eine Methode implementieren, anstatt die Methodenimplementierungen von der übergeordneten Klasse zu erben. Standardmäßig gibt WMI die Implementierung der übergeordneten Klasse an eine abgeleitete Klasse weiter, es sei denn, die abgeleitete Klasse stellt eine Implementierung bereit. Wenn Der **implementierte** Qualifizierer ausgelassen wird, wird angegeben, dass die Methode keine Implementierung in dieser Klasse hat. Wenn Sie eine Methode ohne **implementierten** Qualifizierer erneut deklarieren, geht WMI weiterhin davon aus, dass Sie diese Methode nicht implementieren möchten, und ruft die Implementierung der übergeordneten Klassenmethode auf, wenn sie aufgerufen wird. Daher ist das erneute Deklarieren einer Methode in einer abgeleiteten Klasse ohne Anfügen des **implementierten** Qualifizierers nur nützlich, wenn Sie der Methode einen Qualifizierer hinzufügen oder daraus entfernen.

</dd> <dt>

<span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType
</dt> <dd>

Beschreibt, welchen Wert die Methode zurückgibt. Der Rückgabewert für eine Methode muss ein boolescher, numerischer, **CHAR-,** **STRING-,** [DATETIME-](datetime.md)oder Schemaobjekt sein. Sie können den Rückgabetyp auch als [VOID](void.md)deklarieren, was darauf hinweist, dass die Methode nichts zurückgibt. Sie können ein Array jedoch nicht als Rückgabewerttyp deklarieren.

</dd> <dt>

<span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>Methodname
</dt> <dd>

Definiert den Namen der Methode. Jede Methode muss über einen eindeutigen Namen verfügen. WMI lässt nicht zu, dass zwei Methoden mit dem gleichen Namen und unterschiedlichen Signaturen in einer Klasse oder innerhalb einer Klassenhierarchie vorhanden sind. Daher können Sie auch keine Methode überladen.

</dd> <dt>

<span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>Parameterdirection
</dt> <dd>

Enthält Qualifizierer, die beschreiben, ob ein Parameter ein Eingabeparameter, ein Ausgabeparameter oder beides ist. Verwenden Sie den gleichen Parameternamen nicht mehr als einmal als Eingabeparameter oder mehr als einmal als Ausgabeparameter. Wenn der gleiche Parametername sowohl mit den [**In-**](standard-qualifiers.md) als auch mit dem Out-Qualifizierer angezeigt wird, ist die Funktionalität konzeptionell identisch mit der Verwendung der  **In-, Out-Qualifizierer** für einen einzelnen Parameter.  Wenn Sie jedoch separate Deklarationen verwenden, müssen die Eingabe- und Ausgabeparameter in [](standard-wmi-qualifiers.md) allen anderen Aspekten identisch sein, einschließlich Anzahl und Typ der ID-Qualifizierer, und der Qualifizierer muss identisch sein und explizit für beide deklariert werden. Es wird dringend empfohlen, die **Qualifizierer In**, **Out** innerhalb einer einzelnen Parameterdeklaration zu verwenden.

</dd> <dt>

<span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**
</dt> <dd>

Enthält [](standard-wmi-qualifiers.md) den ID-Qualifizierer, der die Position jedes Parameters innerhalb der Parametersequenz in der Methode eindeutig identifiziert. Standardmäßig markiert der MOF-Compiler Parameter  automatisch mit einem ID-Qualifizierer. Der Compiler markiert den ersten Parameter mit dem Wert 0 (null), der zweite Parameter den Wert 1 (eins) usw. Bei Bedarf können Sie die ID-Sequenz in Ihrem MOF-Code explizit angeben.

</dd> <dt>

<span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType
</dt> <dd>

Beschreibt, welchen Datentyp die Methode akzeptieren kann. Sie können einen Parametertyp als beliebigen MOF-Datenwert definieren, einschließlich eines Arrays, Schemaobjekts oder Verweises. Wenn Sie ein Array als Parameter verwenden, verwenden Sie das Array als ungebunden oder mit einer expliziten Größe.

</dd> <dt>

<span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>Parametername
</dt> <dd>

Enthält den Namen des Parameters. Sie können auch den Standardwert des Parameters an diesem Punkt definieren. Parameter, die keine Anfangswerte aufweisen, bleiben nicht zugewiesen.

</dd> </dl>

Im folgenden Codebeispiel werden die Parameterauflistung und die Qualifizierer beschrieben.

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] sint32 InParam);
    [Implemented] 
    void MyMethod2 ([in, id(0)] sint32 InParam, 
       [out, id(1)] sint32 OutParam);
    [Implemented] 
    sint32 MyMethod3 ([in, out, id(0)] sint32 InOutParam);
};
```

Im folgenden Codebeispiel wird die Verwendung eines Arrays in einem MOF-Parameter beschrieben.

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskParam[]);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskParam[32]);
};
```

Im folgenden Codebeispiel wird die Verwendung eines Schemaobjekts als Parameter und Rückgabewert beschrieben.

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk 
        DiskParam);
    [Implemented] 
    Win32_LogicalDisk MyMethod2 ([in, id(0)] string DiskVolLabel);
};
```

Im folgenden Codebeispiel wird beschrieben, wie zwei Verweise eingeschlossen werden: einer auf eine Instanz der [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) und der andere auf eine Instanz eines unbekannten Objekttyps.

``` syntax
[Dynamic, Provider("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk ref DiskRef);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] object ref AnyObject);
};
```

## <a name="creating-a-wmi-class-method-in-c"></a>Erstellen einer WMI-Klassenmethode in C++

Das folgende Verfahren beschreibt, wie eine WMI-Klassenmethode programmgesteuert erstellt wird.

**So erstellen Sie eine WMI-Klassenmethode programmgesteuert**

1.  Erstellen Sie die Klasse, zu der die Methode gehört.

    Sie müssen zuerst über eine -Klasse verfügen, in der die Methode vor dem Erstellen der -Methode platzieren wird.

2.  Rufen Sie zwei untergeordnete Klassen der [**\_ \_ PARAMETERS-Systemklasse**](--parameters.md) mithilfe von [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)ab.

    Verwenden Sie die erste untergeordnete Klasse, um die in-Parameter zu beschreiben, und die zweite , um die Out-Parameter zu beschreiben. Bei Bedarf können Sie einen einzelnen Abruf ausführen, gefolgt von einem Aufruf der [**IWbemClassObject::Clone-Methode.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone)

3.  Schreiben Sie die In-Parameters in die erste Klasse und die Out-Parameter in die zweite Klasse, indem Sie mindestens einen Aufruf von [**IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)verwenden.

    Beachten Sie beim Beschreiben von Parametern für eine Methode die folgenden Regeln und Einschränkungen:

    -   Behandeln Sie die \[ in-, \] out-Parameter als separate Einträge, einen im -Objekt, das die In-Parameters enthält, und einen im -Objekt, das die Out-Parameter enthält.
    -   Abgesehen von den \[ in-, \] out-Qualifizierern müssen die verbleibenden Qualifizierer genau identisch sein.
    -   Geben Sie die [**ID-Qualifizierer**](standard-wmi-qualifiers.md) an, beginnend bei 0 (null), einem für jeden Parameter.

        Die Reihenfolge der Eingabe- oder Ausgabeparameter wird durch den Wert des [**ID-Qualifizierers**](standard-wmi-qualifiers.md) für jeden Parameter festgelegt. Alle Eingabeargumente müssen allen Ausgabeargumenten vorangestellt werden. Das Ändern der Reihenfolge von Methodeneingabe- und -ausgabeparametern beim Aktualisieren eines vorhandenen Methodenanbieters kann dazu führen, dass Anwendungen, die die Methode aufrufen, fehlschlagen. Fügen Sie am Ende der vorhandenen Parameter neue Eingabeparameter hinzu, anstatt sie in die bereits eingerichtete Sequenz einzufügen.

        Stellen Sie sicher, dass [](standard-wmi-qualifiers.md) keine Lücken in der ID-Qualifizierersequenz bestehen.

    -   Platzieren Sie den Rückgabewert in der out-parameters-Klasse als Eigenschaft mit dem Namen **ReturnValue.**

        Dadurch wird die Eigenschaft als Rückgabewert der Methode identifiziert. Der CIM-Typ dieser Eigenschaft ist der Rückgabetyp der Methode. Wenn die Methode über den Rückgabetyp void verfügt, verfügen Sie überhaupt nicht über eine **ReturnValue-Eigenschaft.** Außerdem kann die **ReturnValue-Eigenschaft** keinen [**ID-Qualifizierer**](standard-wmi-qualifiers.md) wie die Argumente der -Methode aufweisen. Das Zuweisen eines **ID-Qualifizierers** zur **ReturnValue-Eigenschaft** erzeugt einen WMI-Fehler.

    -   Geben Sie alle Standardparameterwerte für die -Eigenschaft in der -Klasse an.

4.  Platzieren Sie beide [**\_ \_ PARAMETERS-Objekte**](--parameters.md) in der übergeordneten Klasse mit einem Aufruf von [**IWbemClassObject::P utMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

    Ein einzelner Aufruf von [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) kann beide [**\_ \_ PARAMETERS-Objekte**](--parameters.md) in der -Klasse platzieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Klasse](creating-a-class.md)
</dt> </dl>

 

 
