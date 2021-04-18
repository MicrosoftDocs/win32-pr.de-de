---
description: Im folgenden werden die für WMI spezifischen Standard Qualifizierer aufgelistet.
ms.assetid: 63bdbafc-51f3-4714-8b7e-9d5a61cef45e
ms.tgt_platform: multiple
title: WMI-Standard Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: e73b053354d86c4a56698a7a65c17e302425f56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368039"
---
# <a name="standard-wmi-qualifiers"></a>WMI-Standard Qualifizierer

Im folgenden werden die für WMI spezifischen Standard Qualifizierer aufgelistet.

<dt>

<span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Trag**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Klassen

Gibt an, dass eine Klasse geänderte Qualifizierer enthält, die lokalisiert werden. Der Standardwert ist " **true**".

Die zugeordnete Klasse kann übersetzt werden. Um auf die übersetzte Version zuzugreifen, verwenden Sie den Gebiets Schema Bezeichner, um einen Namespace Namen zu erstellen.

</dd> <dt>

<span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**\_GetObject umgehen**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Methoden

Gibt an, dass der Methodenaufruf direkt an den **ExecMethodAsync** -Aufruf des Anbieters übergeben werden soll, statt an den Anbieter, der zuerst einen Aufruf von **GetObject** zum Überprüfen des Objekt Pfads durchführen soll. Der Standardwert ist **false**. Die Verwendung von **\_ GetObject umgehen** kann die Leistung erheblich verbessern.

Stellen Sie vor der Verwendung der **Umgehung \_ GetObject** sicher, dass keine der folgenden Aktionen durchgeführt wird:

-   Leiten Sie eine Klasse von der-Klasse ab.
-   Überschreiben Sie die-Methode, die den **\_ GetObject** -Qualifizierer umgeht.

Wenn Sie diese Vorsichtsmaßnahmen nicht befolgen, kann dies dazu führen, dass die Methoden Implementierung der übergeordneten Klasse anstelle der untergeordneten Klasse aufgerufen wird. Weitere Informationen finden Sie unter Using the Bypass \_ GetObject Qualifizierer.

</dd> <dt>

<span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**CIM- \_ Taste**
</dt> <dd>

Datentyp: **CIM \_ Boolean**

Gilt für: Eigenschaften

Gibt an, dass die zugeordnete Eigenschaft eine Schlüsseleigenschaft in CIM, aber nicht in WMI ist.

</dd> <dt>

<span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CimType**](cimtype-qualifier.md)
</dt> <dd>

Datentyp: **VT \_ BSTR**

Gilt für: Eigenschaften, Methoden, Parameter

Enthält Text, der den Typ einer Eigenschaft beschreibt.

</dd> <dt>

<span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**
</dt> <dd>

Datentyp: **VT \_ BSTR**

Gilt für: Klassen

Gibt an, dass eine Klasse über Instanzen verfügt, die anderen von einem Anbieter dynamisch bereitgestellten Informationen zugeordnet sind.

</dd> <dt>

<span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Veraltet**
</dt> <dd>

Datentyp: **CIM \_ Boolean**

Gilt für: Eigenschaften, Klassen

Gibt an, dass die Eigenschaft durch eine andere Eigenschaft abgelöst wurde.

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Ausgestellten**
</dt> <dd>

Gilt für: Klassen, Eigenschaften

Die **UUID** der zugeordneten-Klasse.

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Schem**](dynamic-qualifier.md)
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Klassen, Eigenschaften

Gibt eine Klasse an, deren Instanzen dynamisch erstellt werden. Der Wert dieses Qualifizierers muss auf " **true**" festgelegt werden.

</dd> <dt>

<span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**Dyn-Eigenschaften**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Klassen, Instanzen

Gibt an, dass eine Instanz Werte enthält, die von dynamischen Eigenschaften Anbietern bereitgestellt werden. Der Standardwert ist " **true**".

Sie müssen diesen Qualifizierer für eine solche Instanz angeben. Nur der Wert " **true** " ist zulässig.

</dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Festen**
</dt> <dd>

Datentyp: **CIM \_ Boolean**

Gilt für: Instanzen

Gibt an, dass der Wert dieser Eigenschaft während der Lebensdauer der Instanz nicht geändert werden kann.

</dd> <dt>

<span id="ID"></span><span id="id"></span>**Name**
</dt> <dd>

Datentyp: **VT \_ I4**

Gilt für: Eigenschaften, Parameter

Identifiziert und erstellt eine Eigenschaft oder einen Methoden Parameter eindeutig, wenn MOF-Anweisungen automatisch generiert werden.

Dieser Qualifizierer ist nur für Methoden Parameter erforderlich. Beim Erstellen von Parametern für eine Methode sollten Klassen-Designer für den ersten Parameter mit der ID (0) beginnen und jede aufeinander folgende Ganzzahl für jeden aufeinander folgenden Parameter verwenden. Wenn die **ID** -Qualifizierer versehentlich ausgelassen werden, generiert der MOF-Compiler automatisch **ID** -Qualifizierer.

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Realisierte**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Methoden

Gibt an, dass eine Methode eine Implementierung hat, die von einem Anbieter bereitgestellt wird.

</dd> <dt>

<span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**
</dt> <dd>

Datentyp: **VT \_ BSTR**

Gilt für: Instanzen

Gibt an, dass eine Instanz Werte enthält, die von einem dynamischen Eigenschaften Anbieter bereitgestellt werden.

Der Wert wird als Argument an die [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) -Methode an den Eigenschaften Anbieter übermittelt.

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Konfigurations**
</dt> <dd>

Datentyp: **VT \_ BSTR**

Gilt für: Klassen oder Instanzen

Gibt die Ursprungssprache für eine Klasse oder eine Instanz an. Weitere Informationen zu Gebiets Schema Werten finden Sie unter Gebiets Schema [Codes](#locale-codes).

</dd> <dt>

<span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**Namespacesecuritysddl**
</dt> <dd>

Datentyp: **Zeichen folgen Array**

Gilt für: Namespace Instanzen

Gibt eine Sicherheits Beschreibung für den Namespace im [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) -Format an. Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit, wenn der Namespace erstellt wird](setting-namespace-security-when-the-namespace-is-created.md). Die SDDL-Zeichenfolge wird von WMI verarbeitet, um die Namespace Sicherheit festzulegen, die jedoch nicht als Zeichenfolge gespeichert wird. Wenn kein Sicherheits Deskriptor angegeben wird, wird die Standard Sicherheit verwendet. Weitere Informationen finden Sie unter [Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md).

</dd> <dt>

<span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Optionale**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Parameter

Gibt an, dass ein Parameter nicht erforderlich ist und dass er über einen gut verhaltenen Standardwert verfügt.

</dd> <dt>

<span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Berechtigungen**
</dt> <dd>

Datentyp: **Zeichen folgen Array**

Gilt für: Eigenschaften, Methoden

Ein Satz von Werten, mit denen der Client darüber informiert wird, welche Berechtigungen zum Erstellen von Instanzen, zum Ausfüllen von Eigenschaften oder zum Ausführen von Methoden erforderlich sind. Der Standardwert ist **false**.

</dd> <dt>

<span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**Propertycontext**
</dt> <dd>

Datentyp: **VT \_ BSTR**

Gilt für: Eigenschaften

Gibt an, dass eine Instanzeigenschaft von dynamischen Eigenschafts Anbietern bereitgestellte Werte enthält.

Dieser Qualifizierer muss für eine solche Eigenschaft angegeben werden. Der Wert wird an den Eigenschaften Anbieter als Argument an [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty)übermittelt.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Ab**
</dt> <dd>

Datentyp: **VT \_ BSTR**

Gilt für: Klassen

Der Wert dieses Qualifizierers ist der Name des dynamischen Anbieters, der Klassen Instanzen bereitstellt und Instanzdaten aktualisiert. Dieser Name muss bei WMI registriert werden, indem eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse mit der **Name** -Eigenschaft erstellt wird, die diesen Namen enthält. Wenn dieser Qualifizierer für eine Klasse angegeben wird, deren Instanzen dynamisch bereitgestellt werden, muss auch der **dynamische** Qualifizierer angegeben werden.

</dd> <dt>

<span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**Requirements-Verschlüsselung**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Namespace Instanzen

Wenn diese Einstellung auf " **true**" festgelegt ist, markiert "Requirements **sencryption** " einen Namespace, sodass Client Anwendungen und Skripts eine Verbindung mit verschlüsselter Authentifizierung Die Authentifizierungs Ebene muss in C++ auf **RPC \_ C \_ authn \_ Level \_ Pkt \_ Privacy** festgelegt werden. Bei der Skripterstellung oder Visual Basic muss die Authentifizierungs Ebene auf **wbemauthenticationlevelpktprivacy** festgelegt werden. Weitere Informationen finden Sie unter [Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md). Der Qualifizierer wird in [*MOF*](gloss-m.md) mit dem Pragma Namespace Präprozessor-Befehl verwendet.

Weitere Informationen finden Sie unter [Festlegen der Standardprozess-Sicherheitsstufe mithilfe von C++](setting-the-default-process-security-level-using-c-.md) oder [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md). Skript Authentifizierungs Ebenen werden in [**wbemauthenticationlevelerum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)definiert.

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Klassen

Gibt eine Klasse an, die nur über eine Instanz verfügen kann, die keine Schlüsseleigenschaften enthält.

Nur der Wert **true** (Standard) ist zulässig.

</dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Kum**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Methoden

Gibt an, ob eine Methode mithilfe der Klassendefinition oder ihrer Instanzen aufgerufen werden kann.

Die-Methode kann nicht von einer-Instanz aufgerufen werden.

</dd> <dt>

<span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**Untertyp**
</dt> <dd>

Datentyp: **VT \_ BSTR**

Gilt für: Eigenschaften

Gibt an, dass eine Eigenschaft vom Typ **CIM \_ DateTime** ein Zeitintervall anstelle eines bestimmten Zeitraums darstellt.

Um die Eigenschaft als Intervall zu identifizieren, muss der Wert dieses Qualifizierers "Interval" lauten. Alle anderen Werte für diesen Qualifizierer sind für die zukünftige Verwendung reserviert.

</dd> <dt>

<span id="UUID"></span><span id="uuid"></span>**UUID**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Klassen

Universell eindeutiger Bezeichner für die Klasse.

</dd> <dt>

<span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**Classversion**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Klassen

Die Versionsnummer des-Klassen Objekts. Der Standardwert ist **null**. Die Versionsnummer wird erhöht, wenn Änderungen an der-Klasse vorgenommen werden.

</dd> <dt>

<span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**Schreibberechtigungen**
</dt> <dd>

Datentyp: **Zeichen folgen Array**

Gilt für: Eigenschaften

Ein Satz von Werten, der angibt, welche System Privilegien verfügbar sein müssen und für einen erfolgreichen Schreibvorgang aktiviert werden müssen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

### <a name="locale-codes"></a>Gebiets Schema Codes

Ein Gebiets Schema Code hat die Form "MS \_ <Three Digit Language ID> ". Beispielsweise ist das englische Gebiets Schema MS \_ 409. In der folgenden Tabelle werden die Sprach-IDs aufgelistet.



| Sprache              | Sprach-ID (hexadezimal) |
|-----------------------|---------------------------|
| Arabisch                | 401                       |
| Portugiesisch (Brasilien)   | 416                       |
| Chinesisch (vereinfacht)  | 804                       |
| Chinesisch (traditionell) | 404                       |
| Tschechisch                 | 405                       |
| Dänisch                | 406                       |
| Niederländisch                 | 413                       |
| Englisch (Standard)     | 409                       |
| Finnisch               | 40 b                       |
| Französisch                | 40 c                       |
| Deutsch                | 407                       |
| Griechisch                 | 408                       |
| Hebräisch                | 40 d                       |
| Ungarisch             | 40 e                       |
| Italienisch               | 410                       |
| Japanisch              | 411                       |
| Koreanisch                | 412                       |
| Norwegisch             | 414                       |
| Polnisch                | 415                       |
| Portugiesisch (Portugal) | 816                       |
| Russisch               | 419                       |
| Spanisch               | c0a                       |
| Schwedisch               | 41d                       |
| Türkisch               | 41F                       |



 

### <a name="using-the-bypass_getobject-qualifier"></a>Verwenden des " \_ GetObject"-Qualifizierers umgehen

Wenn Sie **den \_ GetObject** -Qualifizierer für eine Methode umgehen, können verwirrende Ergebnisse erzeugt werden.

Im folgenden Beispiel werden die **Form** -und **Kreis** Klassen definiert. Beachten Sie, dass die **Circle** -Klasse von der **Shape** -Klasse abgeleitet ist.


```VB
class Shape
{
   string Name;
   uint32 DrawIt();  // - draws an irregular geometric shape
};

class Circle : Shape
{
   uint32 DrawIt();  // - draws a circle
};
```



Der folgende Befehl von **ExecMethod** verwendet ein **Kreis** Objekt mit dem Namen "mycircle", um einen Kreis zu zeichnen.


```VB
ExecMethod("Shape.Name='MyCircle'","DrawIt");
```



Im vorherigen Szenario ruft WMI " **GetObject**;" auf. ermittelt, dass "Shape. Name = ' mycircle '" ein **Kreis** ist. und führt die **Zirkel** Implementierung von **drawit** aus. Wenn Sie jedoch den Qualifizierer " **\_ GetObject umgehen** " für **drawit** verwenden, ruft WMI " **GetObject**" nicht auf, erkennt nicht, dass "Shape. Name = ' mycircle '" ein **Kreis** ist, und führt die **Shape** -Implementierung von **drawit** anstelle der **Circle** -Implementierung von **drawit** aus.

Der folgende Aufruf von **ExecMethod** ruft immer die korrekte Implementierung von **drawit** auf.


```VB
ExecMethod("Circle.Name='MyCircle'","DrawIt");
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[WMI Qualifizierer](wmi-qualifiers.md)
</dt> <dt>

[Fügen eines Qualifizierers](adding-a-qualifier.md)
</dt> </dl>

 

