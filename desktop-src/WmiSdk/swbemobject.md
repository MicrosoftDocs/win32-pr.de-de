---
description: Sie können die Methoden und Eigenschaften des SWbemObject-Objekts verwenden, um eine WMI-Klassendefinition (Windows Management Instrumentation) oder eine Objektinstanz zu darstellen.
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: SWbemObject-Objekt (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject
- ISWbemObject
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f8e33a3a0a5028292ce7cef7b44a37433b00f942ea9459ec18e6d53e1cf9a43c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504050"
---
# <a name="swbemobject-object"></a>SWbemObject-Objekt

Sie können die Methoden und Eigenschaften des **SWbemObject-Objekts** verwenden, um eine WMI-Klassendefinition (Windows Management Instrumentation) oder eine Objektinstanz zu darstellen. Dieses Objekt kann nicht durch den VBScript [CreateObject-Aufruf erstellt](/previous-versions//xzysf6hc(v=vs.85)) werden.

Dieses Objekt unterstützt zwei Typen von Eigenschaften und Methoden. Bei den in diesem Abschnitt definierten Eigenschaften und Methoden handelt es sich um generische Eigenschaften und Methoden, die für alle WMI-Objekte gelten. Darüber hinaus macht dieses Objekt die Eigenschaften und Methoden des zugrunde liegenden Objekts als dynamische Automatisierungseigenschaften und -methoden von **SWbemObject verfügbar.** Die Namen und Typen dieser Eigenschaften und Methoden hängen vom zugrunde liegenden WMI-Objekt ab. Weitere Informationen dazu, wie diese dynamischen Eigenschaften und Methoden verfügbar gemacht werden, finden Sie unter [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).

Aus Sicht des WMI-Clients befindet sich dieses Objekt immer im Prozess. Schreibvorgänge wirken sich nur auf die lokale Kopie des Objekts aus, und Lesevorgänge rufen immer Werte aus der lokalen Kopie ab. Updates für WMI werden nur ausgeführt, wenn ganze Objekte mithilfe eines Aufrufs der [**SWbemObject.Put-Methode geschrieben \_**](swbemobject-put-.md) werden. Wenn Sie die Eigenschaften oder Methoden in einem **SWbemObject-Objekt** ändern, werden Ihre Änderungen erst in WMI geschrieben, wenn Sie **SWbemObject.Put aufrufen. \_**

Die in diesem Abschnitt definierten generischen Methoden- und Eigenschaftsnamen enden immer mit einem nach unten liegenden Unterstrich (" "), um sie von den dynamischen WMI-Methoden und -Eigenschaften des zugrunde liegenden \_ Objekts zu unterscheiden.

Beachten **Sie, dass SWbemObject nicht** mit der VBScript [**GetObject -Methode**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)erstellt werden kann. Wenn Sie eine neue leere Klasse erstellen möchten, verwenden [**Sie SWbemServices.Get mit**](swbemservices-get.md) einem leeren Pfadparameter. Dieser Aufruf gibt ein leeres **SWbemObject-Objekt** zurück, das zu einer Klasse werden kann. Anschließend können Sie einen Klassennamen für die [**Class-Eigenschaft**](swbemobjectpath-class.md) des [**SWbemObjectPath-Objekts**](swbemobjectpath.md) angeben, das vom [**Path-Aufruf zurückgegeben \_**](swbemobject-path-.md) wird. Fügen Sie der neuen Klasse mit der [**Properties-Methode \_ Eigenschaften**](swbemobject-properties-.md) hinzu. Um eine -Instanz zu erstellen, rufen **Sie GetObject für** die neue Klasse auf.

Das folgende Codebeispiel zeigt, wie Sie eine neue Klasse abrufen und ihr eine -Eigenschaft hinzufügen. Das **SWbemObject-Objekt,** das die Klasse darstellt, muss durch einen Aufruf von Put in das WMI-Repository [**zurückgeschrieben werden. \_**](swbemobject-put-.md)


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

```



Sie können das Repository mit einem Anzeigetool wie [CIM Studio untersuchen,](further-information.md) um sicherzustellen, dass die neue Klasse und Instanz angezeigt werden. Ein Beispiel zum Entfernen einer Klasse und Instanz aus dem Repository finden Sie unter [**SWbemServices.Delete**](swbemservices-delete.md) oder [**SWbemObject.Delete. \_**](swbemobject-delete-.md)

## <a name="members"></a>Member

Das **SWbemObject-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SWbemObject-Objekt** verfügt über diese Methoden.



| Methode                                                        | Beschreibung                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Associators\_**](swbemobject-associators-.md)             | Ruft die Assoziatoren des -Objekts ab.<br/>                                                     |
| [**AssociatorsAsync\_**](swbemobject-associatorsasync-.md)   | Ruft die Assoziatoren des -Objekts asynchron ab.<br/>                                      |
| [**Klon\_**](swbemobject-clone-.md)                         | Erstellt eine Kopie des aktuellen -Objekts.<br/>                                                          |
| [**Compareto\_**](swbemobject-compareto-.md)                 | Testet zwei -Objekte auf Gleichheit.<br/>                                                              |
| [**Löschen\_**](swbemobject-delete-.md)                       | Löscht das -Objekt aus WMI.<br/>                                                                 |
| [**DeleteAsync\_**](swbemobject-deleteasync-.md)             | Löscht das Objekt asynchron aus WMI.<br/>                                                  |
| [**ExecMethod\_**](swbemobject-execmethod-.md)               | Führt eine Von einem Methodenanbieter exportierte Methode aus.<br/>                                             |
| [**ExecMethodAsync\_**](swbemobject-execmethodasync-.md)     | Führt eine von einem Methodenanbieter exportierte Methode asynchron aus.<br/>                              |
| [**GetObjectText\_**](swbemobject-getobjecttext-.md)         | Ruft die Textdarstellung des Objekts ab (MOF-Syntax).<br/>                             |
| [**Instanzen\_**](swbemobject-instances-.md)                 | Gibt eine Auflistung von Instanzen des -Objekts zurück (das eine WMI-Klasse sein muss).<br/>                 |
| [**InstancesAsync\_**](swbemobject-instancesasync-.md)       | Gibt eine Auflistung von Instanzen des -Objekts (das eine WMI-Klasse sein muss) asynchron zurück.<br/>  |
| [**Put\_**](swbemobject-put-.md)                             | Erstellt oder aktualisiert das -Objekt in WMI.<br/>                                                        |
| [**PutAsync\_**](swbemobject-putasync-.md)                   | Erstellt oder aktualisiert das Objekt asynchron in WMI.<br/>                                         |
| [**Referenzen\_**](swbemobject-references-.md)               | Gibt Verweise auf das -Objekt zurück.<br/>                                                            |
| [**ReferencesAsync\_**](swbemobject-referencesasync-.md)     | Gibt Verweise auf das -Objekt asynchron zurück.<br/>                                             |
| [**SpawnDerivedClass\_**](swbemobject-spawnderivedclass-.md) | Erstellt eine neue abgeleitete Klasse aus dem aktuellen -Objekt (das eine WMI-Klasse sein muss).<br/>             |
| [**SpawnInstance\_**](swbemobject-spawninstance-.md)         | Erstellt eine neue -Instanz aus dem aktuellen -Objekt.<br/>                                              |
| [**Unterklassen von  werden erstellt.\_**](swbemobject-subclasses-.md)               | Gibt eine Auflistung von Unterklassen des -Objekts zurück (das eine WMI-Klasse sein muss).<br/>                |
| [**UnterklassenAsync\_**](swbemobject-subclassesasync-.md)     | Gibt asynchron eine Auflistung von Unterklassen des -Objekts zurück (das eine WMI-Klasse sein muss).<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **SWbemObject-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                   | Zugriffstyp          | Beschreibung                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ableitung\_**](swbemobject-derivation-.md)<br/> | Schreibgeschützt<br/> | Enthält ein Array von Zeichenfolgen, das die Ableitungshierarchie für die -Klasse beschreibt.<br/>                                             |
| [**Methoden\_**](swbemobject-methods-.md)<br/>       | Schreibgeschützt<br/> | Ein [**SWbemMethodSet-Objekt,**](swbemmethodset.md) das die Auflistung von Methoden für dieses Objekt ist.<br/>                           |
| [**Pfad\_**](swbemobject-path-.md)<br/>             | Schreibgeschützt<br/> | Enthält ein [**SWbemObjectPath-Objekt,**](swbemobjectpath.md) das den Objektpfad der aktuellen Klasse oder Instanz darstellt.<br/> |
| [**Eigenschaften\_**](swbemobject-properties-.md)<br/> | Schreibgeschützt<br/> | Ein [**SWbemPropertySet-Objekt,**](swbempropertyset.md) das die Auflistung von Eigenschaften für dieses Objekt ist.<br/>                    |
| [**Qualifikation\_**](swbemobject-qualifiers-.md)<br/> | Schreibgeschützt<br/> | Ein [**SWbemQualifierSet-Objekt,**](swbemqualifierset.md) das die Auflistung von Qualifizierern für dieses Objekt ist.<br/>                  |
| [**Sicherheit\_**](swbemobject-security-.md)<br/>     | Schreibgeschützt<br/> | Enthält ein [**SWbemSecurity-Objekt,**](swbemsecurity.md) das zum Lesen oder Ändern der Sicherheitseinstellungen verwendet wird.<br/>                         |



 

## <a name="examples"></a>Beispiele

Im VBScript-Codebeispiel List [All the Properties and Methods for a WMI Class](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) (Alle Eigenschaften und Methoden für eine WMI-Klasse auflisten) im TechNet-Katalog wird das SWbemObject verwendet, um alle Methoden und Eigenschaften für eine angegebene WMI-Klasse auflisten zu können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[Skripterstellung für API-Objekte](scripting-api-objects.md)
</dt> </dl>

 

