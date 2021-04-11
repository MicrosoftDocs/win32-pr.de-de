---
description: Um eine WMI-Methode zu erstellen, definieren Sie die Eingabe-und Ausgabeparameter für die Methode.
ms.assetid: 71cbecde-33c4-4bf1-9793-bef6d823dcac
ms.tgt_platform: multiple
title: Erstellen einer WMI-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2489a5dd4e97ed6c8d26eeb292c45fa66901cbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217965"
---
# <a name="creating-a-wmi-method"></a>Erstellen einer WMI-Methode

Um eine WMI-Methode zu erstellen, definieren Sie die Eingabe-und Ausgabeparameter für die Methode. Die Eingabe-und Ausgabeparameter werden durch einen speziellen WMI-System Klassen [**\_ \_ Parameter**](--parameters.md)dargestellt. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md) und [Schreiben eines Methoden Anbieters](writing-a-method-provider.md).

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Erstellen einer WMI-Klassenmethode in MOF](#creating-a-wmi-class-method-in-mof)
-   [Erstellen einer WMI-Klassenmethode in C++](#creating-a-wmi-class-method-in-c)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a>Erstellen einer WMI-Klassenmethode in MOF

In WMI sind Anbieter Methoden in der Regel unterschiedliche Aktionen im Zusammenhang mit dem Objekt, das die-Klasse darstellt. Anstatt den Wert einer Eigenschaft zu ändern, um eine Aktion auszuführen, sollte eine Methode erstellt werden. Beispielsweise können Sie ein Netzwerk Informations Center (Network Information Center, NIC), das durch den [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-networkadapter) -Netzwerkadapter dargestellt wird, mithilfe der Methoden [**enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) und [**Deaktivieren**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) aktivieren oder deaktivieren. Diese Aktionen können zwar als Lese-/Schreibeigenschaft dargestellt werden, aber der empfohlene Entwurf ist das Erstellen einer Methode. Wenn Sie einen Status oder Wert für die Klasse sichtbar machen möchten, wird empfohlen, anstelle einer Methode eine Lese-/Schreibeigenschaft zu erstellen. In **Win32 \_ Network Adapter** bewirkt die Eigenschaft " **nettenabled** ", dass der Status des Adapters sichtbar ist, aber Änderungen zwischen Zuständen durch die Methoden " **enable** " und " **Deaktivieren** " ausgeführt werden.

Klassen Deklarationen können die Deklaration von einer oder mehreren Methoden einschließen. Sie können entweder die Methoden einer übergeordneten Klasse erben oder Ihre eigene Klasse implementieren. Wenn Sie sich für die Implementierung Ihrer eigenen Methoden entscheiden, müssen Sie die-Methode deklarieren und die Methode mit bestimmten qualifizierertags markieren.

Im folgenden Verfahren wird beschrieben, wie Sie eine Methode in einer Klasse deklarieren, die nicht von einer Basisklasse erbt.

**So deklarieren Sie eine Methode**

1.  Definieren Sie den Namen der Methode zwischen den geschweiften Klammern einer Klassen Deklaration, gefolgt von allen Qualifizierern.

    Im folgenden Codebeispiel wird die Syntax für eine-Methode beschrieben.

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  Wenn Sie fertig sind, fügen Sie den MOF-Code (Managed Object Format) in das WMI-Repository ein, indem Sie den MOF-Compiler aufzurufen.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).

In der folgenden Liste sind die Elemente der Methoden Deklaration definiert.

<dl> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Ab**](/windows/desktop/api/Provider/nl-provider-provider)
</dt> <dd>

Verknüpft einen bestimmten Anbieter mit ihrer Klassen Beschreibung. Der Wert des [**Anbieter**](/windows/desktop/api/Provider/nl-provider-provider) Qualifizierers ist der Name des Anbieters, der WMI anweist, wo sich der Code befindet, der die Methode unterstützt. Ein Anbieter sollte auch eine beliebige Klasse mit dynamischen Instanzen mit dem **dynamischen** Qualifizierer markieren. Verwenden Sie hingegen nicht den **dynamischen** Qualifizierer, um eine Klasse zu markieren, die eine statische Instanz mit **implementierten** Methoden enthält.

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Realisierte**
</dt> <dd>

Deklariert, dass Sie eine Methode implementieren, anstatt die Methoden Implementierung von der übergeordneten Klasse zu erben. Standardmäßig wird die Implementierung der übergeordneten Klasse von WMI an eine abgeleitete Klasse weitergegeben, es sei denn, die abgeleitete Klasse stellt eine-Implementierung bereit. Das Weglassen des **implementierten** Qualifizierers gibt an, dass die Methode in dieser Klasse keine Implementierung aufweist. Wenn Sie eine Methode ohne den **implementierten** Qualifizierer erneut deklarieren, geht WMI weiterhin davon aus, dass Sie diese Methode nicht implementieren, und ruft die Implementierung der übergeordneten Klassenmethode auf, wenn aufgerufen wird. Daher ist es hilfreich, eine Methode in einer abgeleiteten Klasse erneut zu deklarieren, ohne den **implementierten** Qualifizierer anzufügen, wenn Sie der Methode einen Qualifizierer hinzufügen oder daraus entfernen.

</dd> <dt>

<span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType
</dt> <dd>

Beschreibt den Wert, den die Methode zurückgibt. Der Rückgabewert einer Methode muss ein boolesches, numerisches, **char**-, **String**-, [DateTime](datetime.md)-oder Schema-Objekt sein. Sie können den Rückgabetyp auch als [void](void.md)deklarieren, um anzugeben, dass die Methode nichts zurückgibt. Es ist jedoch nicht möglich, ein Array als Rückgabe Werttyp zu deklarieren.

</dd> <dt>

<span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName
</dt> <dd>

Definiert den Namen der Methode. Jede Methode muss einen eindeutigen Namen aufweisen. WMI lässt nicht zu, dass zwei Methoden mit demselben Namen und unterschiedlichen Signaturen in einer Klasse oder innerhalb einer Klassenhierarchie vorhanden sind. Daher ist es auch nicht möglich, eine Methode zu überladen.

</dd> <dt>

<span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection
</dt> <dd>

Enthält Qualifizierer, die beschreiben, ob ein Parameter ein Eingabeparameter, ein Ausgabeparameter oder beides ist. Verwenden Sie nicht denselben Parameternamen mehrmals als Eingabeparameter oder mehr als einen Zeitparameter als Ausgabeparameter. Wenn derselbe Parameter Name sowohl [**für den in**](standard-qualifiers.md) -als auch für den **out** -Qualifizierer angezeigt wird, ist die Funktionalität konzeptionell identisch mit der Verwendung der **in**-, **out** -Qualifizierer für einen einzelnen Parameter. Wenn jedoch separate Deklarationen verwendet werden, müssen die Eingabe-und Ausgabeparameter in allen anderen Punkten genau übereinstimmen, einschließlich Anzahl und Typ der [**ID**](standard-wmi-qualifiers.md) -Qualifizierer. der Qualifizierer muss gleich sein und explizit für beide deklariert werden. Es wird dringend empfohlen, die **in**-, **out** -Qualifizierer innerhalb einer einzelnen Parameter Deklaration zu verwenden.

</dd> <dt>

<span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**Idqualifizierer**
</dt> <dd>

Enthält den [**ID**](standard-wmi-qualifiers.md) -Qualifizierer, der die Position jedes Parameters innerhalb der Sequenz von Parametern in der Methode eindeutig identifiziert. Standardmäßig markiert der MOF-Compiler Parameter automatisch mit einem **ID** -Qualifizierer. Der Compiler markiert den ersten Parameter mit einem Wert von 0 (null), dem zweiten Parameter dem Wert 1 (eins) usw. Falls erforderlich, können Sie die ID-Sequenz explizit im MOF-Code angeben.

</dd> <dt>

<span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>Parameter Type
</dt> <dd>

Beschreibt den Datentyp, der von der Methode akzeptiert werden kann. Sie können einen Parametertyp als einen beliebigen MOF-Datenwert definieren, einschließlich eines Arrays, Schema Objekts oder Verweises. Wenn Sie ein Array als Parameter verwenden, verwenden Sie das Array als ungebunden oder mit einer expliziten Größe.

</dd> <dt>

<span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>Parameter Name
</dt> <dd>

Enthält den Namen des Parameters. An dieser Stelle können Sie auch den Standardwert des Parameters definieren. Parameter, die anfängliche Werte fehlen, bleiben nicht zugewiesen.

</dd> </dl>

Im folgenden Codebeispiel werden die Parameter Auflistung und die Qualifizierer beschrieben.

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

Im folgenden Codebeispiel wird beschrieben, wie ein Array in einem MOF-Parameter verwendet wird.

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

Im folgenden Codebeispiel wird die Verwendung eines Schema Objekts als Parameter und Rückgabewert beschrieben.

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

Im folgenden Codebeispiel wird beschrieben, wie zwei Verweise eingeschlossen werden: eine für eine Instanz der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse und die andere für eine Instanz eines unbekannten Objekt Typs.

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

Im folgenden Verfahren wird beschrieben, wie eine WMI-Klassenmethode Programm gesteuert erstellt wird.

**So erstellen Sie eine WMI-Klassenmethode Programm gesteuert**

1.  Erstellen Sie die Klasse, zu der die Methode gehört.

    Bevor Sie die-Methode erstellen, muss zunächst eine-Klasse vorhanden sein, in der die-Methode platziert werden soll.

2.  Rufen Sie mithilfe von [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)zwei untergeordnete Klassen der [**\_ \_ Parameters**](--parameters.md) -System Klasse ab.

    Verwenden Sie die erste untergeordnete Klasse, um die in-Parameter zu beschreiben, und die zweite, um die Out-Parameter zu beschreiben. Falls erforderlich, können Sie einen einzelnen Abruf ausführen, gefolgt von einem-Befehl der [**IWbemClassObject:: Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) -Methode.

3.  Schreiben Sie die in-Parameter in die erste Klasse und die Out-Parameter in die zweite Klasse mit einem oder mehreren Aufrufen von [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Beachten Sie beim Beschreiben von Parametern für eine Methode die folgenden Regeln und Einschränkungen:

    -   Behandeln \[ Sie die in \] -und out-Parameter als separate Einträge, eine in dem-Objekt, das die in-Parameter enthält, und eines in dem-Objekt, das die Out-Parameter enthält.
    -   Abgesehen von den \[ in-, out- \] Qualifizierern müssen die verbleibenden Qualifizierer exakt identisch sein.
    -   Geben Sie die [**ID**](standard-wmi-qualifiers.md) -Qualifizierer an, beginnend bei 0 (null), eine für jeden Parameter.

        Die Reihenfolge der Eingabe-oder Ausgabeparameter wird durch den Wert des [**ID**](standard-wmi-qualifiers.md) -Qualifizierers für jeden Parameter festgelegt. Alle Eingabeargumente müssen allen Ausgabe Argumenten vorangestellt sein. Wenn Sie die Reihenfolge der Eingabe-und Ausgabeparameter der Methode beim Aktualisieren eines vorhandenen Methoden Anbieters ändern, kann dies dazu führen, dass Anwendungen, die die-Methode aufruft Fügen Sie am Ende der vorhandenen Parameter neue Eingabeparameter hinzu, anstatt Sie in die bereits festgelegte Sequenz einzufügen.

        Stellen Sie sicher, dass keine Lücken in der [**ID**](standard-wmi-qualifiers.md) -qualifizierersequenz bestehen.

    -   Legen Sie den Rückgabewert in der Out-Parameter-Klasse als Eigenschaft mit dem Namen " **ReturnValue**" ab.

        Dadurch wird die-Eigenschaft als Rückgabewert der-Methode identifiziert. Der CIM-Typ dieser Eigenschaft ist der Rückgabetyp der Methode. Wenn die Methode den Rückgabetyp "void" aufweist, verfügen Sie nicht über eine **ReturnValue** -Eigenschaft. Außerdem kann die **ReturnValue** -Eigenschaft nicht über einen [**ID**](standard-wmi-qualifiers.md) -Qualifizierer wie die Argumente der Methode verfügen. Das Zuweisen eines **ID** -Qualifizierers zur **ReturnValue** -Eigenschaft erzeugt einen WMI-Fehler.

    -   Ausgedrückt alle Standardparameter Werte für die-Eigenschaft in der-Klasse.

4.  Fügen Sie beide [**\_ \_ Parameter**](--parameters.md) Objekte in die übergeordnete Klasse ein, indem Sie " [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)" aufruft.

    Mit einem einzelnen [**CALLMETHOD**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) -Befehl können beide [**\_ \_ Parameter**](--parameters.md) Objekte in die-Klasse platziert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Klasse](creating-a-class.md)
</dt> </dl>

 

 
