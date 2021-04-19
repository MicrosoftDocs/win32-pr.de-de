---
description: Sie können die Methoden und Eigenschaften des Objekts "errbewbject" verwenden, um eine Windows-Verwaltungsinstrumentation (WMI)-Klassendefinition oder-Objektinstanz darzustellen.
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: Errbebobject-Objekt (wbemdisp. h)
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
ms.openlocfilehash: 287395b976177170c8bdffa0e1817a8755a4d397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360165"
---
# <a name="swbemobject-object"></a>Errbejebject-Objekt

Sie können die Methoden und Eigenschaften des Objekts " **errbewbject** " verwenden, um eine Windows-Verwaltungsinstrumentation (WMI)-Klassendefinition oder-Objektinstanz darzustellen. Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](/previous-versions//xzysf6hc(v=vs.85)) " erstellt werden.

Dieses Objekt unterstützt zwei Typen von Eigenschaften und Methoden. Die in diesem Abschnitt definierten generischen Eigenschaften und Methoden, die für alle WMI-Objekte gelten. Darüber hinaus macht dieses-Objekt die Eigenschaften und Methoden des zugrunde liegenden Objekts als dynamische Automatisierungs Eigenschaften und-Methoden von " **errbemubject**" verfügbar. Die Namen und Typen dieser Eigenschaften und Methoden hängen vom zugrunde liegenden WMI-Objekt ab. Weitere Informationen darüber, wie diese dynamischen Eigenschaften und Methoden verfügbar gemacht werden, finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).

In der WMI-Client Perspektive ist dieses Objekt immer in Verarbeitung. Schreibvorgänge wirken sich nur auf die lokale Kopie des Objekts aus, und Lesevorgänge rufen immer Werte aus der lokalen Kopie ab. Updates für WMI werden nur ausgeführt, wenn ganze Objekte mithilfe eines Aufrufes der Methode " [**errbemubject \_ . Put**](swbemobject-put-.md) " geschrieben werden. Wenn Sie die Eigenschaften oder Methoden in einem " **errbemubject** "-Objekt ändern, werden die Änderungen erst in WMI geschrieben, wenn Sie " **errbemubject. Put \_**" aufgerufen haben.

Die in diesem Abschnitt definierten generischen Methoden-und Eigenschaftsnamen enden immer mit einem nachfolgenden Unterstrich (" \_ "), um Sie von den dynamischen WMI-Methoden und-Eigenschaften des zugrunde liegenden Objekts zu unterscheiden.

Beachten Sie **, dass das-** Objekt mit der VBScript-Methode " [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx). Method" nicht erstellt werden kann. Wenn Sie eine neue, leere Klasse erstellen möchten [**, verwenden Sie**](swbemservices-get.md) die-Klasse mit einem leeren path-Parameter. Dieser Befehl gibt ein leeres **errbejebject** -Objekt zurück, das eine Klasse werden kann. Sie können dann einen Klassennamen für die [**Class**](swbemobjectpath-class.md) -Eigenschaft des " [**errbemubjectpath**](swbemobjectpath.md) "-Objekts angeben, das vom [**path \_**](swbemobject-path-.md) -Befehl zurückgegeben wird. Fügen Sie der neuen Klasse mithilfe der [**Properties \_**](swbemobject-properties-.md) -Methode Eigenschaften hinzu. Um eine Instanz zu erstellen, rufen Sie **GetObject** für die neue Klasse auf.

Im folgenden Codebeispiel wird gezeigt, wie Sie eine neue Klasse abrufen und ihr eine Eigenschaft hinzufügen. Das-Objekt, das die-Klasse darstellt, muss durch einen- **Befehl** [**Put \_**](swbemobject-put-.md)zurück in das WMI-Repository geschrieben werden.


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



Sie können das Repository mit einem Anzeige Tool wie [CIM Studio](further-information.md) untersuchen, um zu überprüfen, ob die neue Klasse und Instanz angezeigt werden. Ein Beispiel für das Entfernen einer Klasse und einer Instanz aus dem Repository finden Sie unter " [**errbemservices. Delete**](swbemservices-delete.md) " oder " [**errbemubject. Delete \_**](swbemobject-delete-.md)".

## <a name="members"></a>Member

Das " **errbemubject** "-Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das Objekt " **errbemubject** " verfügt über diese Methoden.



| Methode                                                        | BESCHREIBUNG                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ASSOCIATORS\_**](swbemobject-associators-.md)             | Ruft die assoziatoren des-Objekts ab.<br/>                                                     |
| [**Associatorsasync\_**](swbemobject-associatorsasync-.md)   | Ruft die assoziatoren des-Objekts asynchron ab.<br/>                                      |
| [**Klon\_**](swbemobject-clone-.md)                         | Erstellt eine Kopie des aktuellen-Objekts.<br/>                                                          |
| [**CompareTo\_**](swbemobject-compareto-.md)                 | Testet zwei-Objekte auf Gleichheit.<br/>                                                              |
| [**Lösch\_**](swbemobject-delete-.md)                       | Löscht das-Objekt aus WMI.<br/>                                                                 |
| [**DeleteAsync\_**](swbemobject-deleteasync-.md)             | Löscht das Objekt asynchron aus WMI.<br/>                                                  |
| [**ExecMethod\_**](swbemobject-execmethod-.md)               | Führt eine Methode aus, die von einem Methoden Anbieter exportiert wird.<br/>                                             |
| [**ExecMethodAsync\_**](swbemobject-execmethodasync-.md)     | Führt eine Methode, die von einem Methoden Anbieter exportiert wurde, asynchron aus.<br/>                              |
| [**Getobjecttext\_**](swbemobject-getobjecttext-.md)         | Ruft die Textdarstellung des-Objekts (MOF-Syntax) ab.<br/>                             |
| [**Instanzen\_**](swbemobject-instances-.md)                 | Gibt eine Auflistung von Instanzen des-Objekts zurück (bei der es sich um eine WMI-Klasse handeln muss).<br/>                 |
| [**Instancesasync\_**](swbemobject-instancesasync-.md)       | Gibt asynchron eine Auflistung von Instanzen des-Objekts zurück (bei der es sich um eine WMI-Klasse handeln muss).<br/>  |
| [**Stellte\_**](swbemobject-put-.md)                             | Erstellt oder aktualisiert das Objekt in WMI.<br/>                                                        |
| [**Putasync\_**](swbemobject-putasync-.md)                   | Erstellt oder aktualisiert das Objekt asynchron in WMI.<br/>                                         |
| [**References\_**](swbemobject-references-.md)               | Gibt Verweise auf das-Objekt zurück.<br/>                                                            |
| [**Referencesasync\_**](swbemobject-referencesasync-.md)     | Gibt Verweise auf das-Objekt asynchron zurück.<br/>                                             |
| [**SpawnDerivedClass\_**](swbemobject-spawnderivedclass-.md) | Erstellt eine neue abgeleitete Klasse aus dem aktuellen-Objekt (das eine WMI-Klasse sein muss).<br/>             |
| [**SpawnInstance\_**](swbemobject-spawninstance-.md)         | Erstellt eine neue-Instanz aus dem aktuellen-Objekt.<br/>                                              |
| [**Unterklassen von  werden erstellt.\_**](swbemobject-subclasses-.md)               | Gibt eine Auflistung von Unterklassen des-Objekts zurück (bei dem es sich um eine WMI-Klasse handeln muss).<br/>                |
| [**Subclassesasync\_**](swbemobject-subclassesasync-.md)     | Gibt asynchron eine Auflistung von Unterklassen des-Objekts zurück (bei der es sich um eine WMI-Klasse handeln muss).<br/> |



 

### <a name="properties"></a>Eigenschaften

Das " **errbemubject** "-Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                   | Zugriffstyp          | BESCHREIBUNG                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ableitung\_**](swbemobject-derivation-.md)<br/> | Schreibgeschützt<br/> | Enthält ein Array von Zeichen folgen, das die abderivations Hierarchie für die-Klasse beschreibt.<br/>                                             |
| [**Methoden\_**](swbemobject-methods-.md)<br/>       | Schreibgeschützt<br/> | Ein " [**taubemmethodset**](swbemmethodset.md) "-Objekt, das die Auflistung von Methoden für dieses-Objekt ist.<br/>                           |
| [**ADS\_**](swbemobject-path-.md)<br/>             | Schreibgeschützt<br/> | Enthält ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt, das den Objekt Pfad der aktuellen Klasse oder Instanz darstellt.<br/> |
| [**Eigenschaften\_**](swbemobject-properties-.md)<br/> | Schreibgeschützt<br/> | Ein-Objekt, das die Auflistung von Eigenschaften für [**dieses Objekt ist**](swbempropertyset.md) .<br/>                    |
| [**Qualifikation\_**](swbemobject-qualifiers-.md)<br/> | Schreibgeschützt<br/> | Ein " [**taubemqualifierset**](swbemqualifierset.md) "-Objekt, das die Auflistung der Qualifizierer für dieses Objekt ist.<br/>                  |
| [**Sicherheit\_**](swbemobject-security-.md)<br/>     | Schreibgeschützt<br/> | Enthält ein " [**Swap Security**](swbemsecurity.md) "-Objekt, das zum Lesen oder Ändern der Sicherheitseinstellungen verwendet wird.<br/>                         |



 

## <a name="examples"></a>Beispiele

Die [Liste alle Eigenschaften und Methoden für ein WMI-Klassen](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) -VBScript-Codebeispiel in der TechNet Gallery verwendet das "slibemubject", um alle Methoden und Eigenschaften für eine angegebene WMI-Klasse aufzulisten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch Objekt<br/>                                                           |
| IID<br/>                      | IID \_ iswbemujekt<br/>                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Austauschen von "errbemubjectex"**](swbemobjectex.md)
</dt> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

