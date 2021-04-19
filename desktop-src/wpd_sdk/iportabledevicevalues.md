---
description: Die iportabletovicevalues-Schnittstelle enthält eine Auflistung von PropertyKey/PROPVARIANT-Paaren.
ms.assetid: a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f
title: Iportabledebug-Schnittstelle (portabletvicetypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ecdfd91c9ea4ab5202a72015f579d560b37fbffd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365905"
---
# <a name="iportabledevicevalues-interface"></a>Iportabledebug-Schnittstelle

Die **iportabletovicevalues** -Schnittstelle enthält eine Auflistung von **PropertyKey**- / **PROPVARIANT** -Paaren. Werte in der Auflistung müssen nicht den gleichen VarType aufweisen.

Werte werden als Schlüssel-Wert-Paare gespeichert. Jeder Schlüssel muss in der Sammlung eindeutig sein. Clients können nach Elementen durch einen **PropertyKey** oder einen NULL basierten Index suchen. Datenwerte werden als **PROPVARIANT** -Strukturen gespeichert. Sie können Werte eines beliebigen Typs mithilfe der generischen Methoden **SetValue** und **GetValue** hinzufügen oder abrufen, oder Sie fügen Elemente hinzu, indem Sie die Methode verwenden, die für den Typ der hinzugefügten Daten spezifisch ist.

Die **Get...** -Methode erfordert, dass der Aufrufer alle abgerufenen Werte entsprechend freigibt. Die **Set...** -Methoden kopieren den Wert in die Auflistung.

Wenn eine **iportabledevicevalues** -Schnittstelle freigegeben wird, wird **Clear** aufgerufen, wodurch der Arbeitsspeicher, der für alle seine Mitglieder reserviert wurde, entsprechend freigegeben wird.

Diese Schnittstelle kann aus einer-Methode abgerufen werden. Wenn ein neues-Objekt erforderlich ist, rufen Sie **CoCreate** mit der **CLSID \_ portabledevicevalues** auf.

## <a name="members"></a>Member

Die **iportabledebug** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iportabletovicevalues** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iportabledevicevalues** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                                     | BESCHREIBUNG                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**Klartext**](iportabledevicevalues-clear.md)                                                                               | Löscht alle Elemente aus der Auflistung.<br/>                                                                      |
| [**Copyvaluesfrompropertystore**](iportabledevicevalues-copyvaluesfrompropertystore.md)                                   | Kopiert den Inhalt eines **IPropertyStore** in die Auflistung.<br/>                                           |
| [**Copyvaluestopropertystore**](iportabledevicevalues-copyvaluestopropertystore.md)                                       | Kopiert alle Werte aus einer Auflistung in eine **IPropertyStore** -Schnittstelle.<br/>                               |
| [**GetAt**](iportabledevicevalues-getat.md)                                                                               | Ruft mit dem angegebenen Null basierten Index einen Wert aus der Auflistung ab.<br/>                                  |
| [**GetBoolValue**](iportabledevicevalues-getboolvalue.md)                                                                 | Ruft einen **booleschen** Wert (Typ VT \_ bool) ab, der durch einen Schlüssel angegeben wird.<br/>                                              |
| [**Getbuffervalue**](iportabledevicevalues-getbuffervalue.md)                                                             | Ruft einen Byte Array Wert (Type VT \_ Vector \| VT UI1) ab, \_ der von einem Schlüssel angegeben wird.<br/>                               |
| [**GetCount**](iportabledevicevalues-getcount.md)                                                                         | Ruft die Anzahl der Elemente in der Auflistung ab.<br/>                                                            |
| [**Geterrorvalue**](iportabledevicevalues-geterrorvalue.md)                                                               | Ruft einen **HRESULT** -Wert (Type VT \_ Error) ab, der durch einen Schlüssel angegeben wird.<br/>                                         |
| [**GetFloatValue**](iportabledevicevalues-getfloatvalue.md)                                                               | Ruft einen Gleit **Komma Wert (** Typ VT \_ R4) ab, der durch einen Schlüssel angegeben wird.<br/>                                               |
| [**Getguidvalue**](iportabledevicevalues-getguidvalue.md)                                                                 | Ruft einen **GUID** -Wert (Type VT \_ CLSID) ab, der von einem Schlüssel angegeben wird.<br/>                                             |
| [**Getiportabledevicekeycollectionvalue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)                 | Ruft einen **iportabledevicekeycollection** -Wert (Typ VT \_ unknown) ab, der durch einen Schlüssel angegeben wird.<br/>                  |
| [**Getiportabledevicepropvariantcollectionvalue**](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md) | Ruft einen **iportabledevicepropvariantcollection** -Wert (Typ VT \_ unknown) ab, der durch einen Schlüssel angegeben wird.<br/>          |
| [**Getiportableabvicevaluescollectionvalue**](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)           | Ruft einen **iportabledevicevaluescollection** -Wert (Typ VT \_ unknown) ab, der durch einen Schlüssel angegeben wird.<br/>               |
| [**Getiportableendvicevaluesvalue**](iportabledevicevalues-getiportabledevicevaluesvalue.md)                               | Ruft einen **iportabledevicevalues** -Wert (Typ VT \_ unknown) ab, der durch einen Schlüssel angegeben wird.<br/>                         |
| [**Getiunknownvalue**](iportabledevicevalues-getiunknownvalue.md)                                                         | Ruft einen **IUnknown** -Schnittstellen Wert (Typ VT \_ unknown) ab, der durch einen Schlüssel angegeben wird.<br/>                            |
| [**Getkeyvalue**](iportabledevicevalues-getkeyvalue.md)                                                                   | Ruft einen **PropertyKey** -Wert ab, der von einem Schlüssel angegeben wird.<br/>                                                       |
| [**Getsignedintegervalue**](iportabledevicevalues-getsignedintegervalue.md)                                               | Ruft einen **Long** -Wert (Type VT \_ I4) ab, der von einem Schlüssel angegeben wird.<br/>                                                |
| [**Getsignedlargeingetegervalue**](iportabledevicevalues-getsignedlargeintegervalue.md)                                     | Ruft einen **Longlong** -Wert (Typ VT \_ I8) ab, der durch einen Schlüssel angegeben wird.<br/>                                            |
| [**GetStringValue**](iportabledevicevalues-getstringvalue.md)                                                             | Ruft einen Zeichen folgen Wert (Typ VT \_ LPWSTR) ab, der von einem Schlüssel angegeben wird.<br/>                                              |
| [**Getunsignedintegervalue**](iportabledevicevalues-getunsignedintegervalue.md)                                           | Ruft einen **ulong** -Wert (Typ VT \_ UI4) ab, der von einem Schlüssel angegeben wird.<br/>                                              |
| [**Getunsignedlargeingetegervalue**](iportabledevicevalues-getunsignedlargeintegervalue.md)                                 | Ruft einen **ULONGLONG** -Wert (Typ VT \_ UI8) ab, der von einem Schlüssel angegeben wird.<br/>                                          |
| [**GetValue**](iportabledevicevalues-getvalue.md)                                                                         | Ruft einen durch einen Schlüssel angegebenen **PROPVARIANT** -Wert ab.<br/>                                                       |
| [**RemoveValue**](iportabledevicevalues-removevalue.md)                                                                   | Entfernt ein Element aus der Auflistung.<br/>                                                                        |
| [**SetBoolValue**](iportabledevicevalues-setboolvalue.md)                                                                 | Fügt einen neuen **booleschen** Wert (Typ VT \_ bool) hinzu oder überschreibt einen vorhandenen booleschen Wert.<br/>                                 |
| [**Setbuffervalue**](iportabledevicevalues-setbuffervalue.md)                                                             | Fügt einen neuen  \* Bytewert (Type VT \_ Vector \| VT \_ UI1) hinzu oder überschreibt eine vorhandene.<br/>                     |
| [**Wert von "Wert"**](iportabledevicevalues-seterrorvalue.md)                                                               | Fügt einen neuen **HRESULT** -Wert (Type VT \_ Error) hinzu oder überschreibt einen vorhandenen HRESULT-Wert.<br/>                                |
| [**Setfloatvalue**](iportabledevicevalues-setfloatvalue.md)                                                               | Fügt **einen neuen Gleit** Komma Wert (Typ VT \_ R4) hinzu oder überschreibt eine vorhandene.<br/>                                     |
| [**Setguidvalue**](iportabledevicevalues-setguidvalue.md)                                                                 | Fügt einen neuen **GUID** -Wert (Type VT \_ CLSID) hinzu oder überschreibt einen vorhandenen GUID-Wert.<br/>                                   |
| [**"Stiportabledevicekeycollectionvalue"**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)                 | Fügt einen neuen **iportabledevicekeycollectionvalue** -Wert (Typ VT \_ unknown) hinzu oder überschreibt eine vorhandene.<br/>    |
| [**"Stiportabledevicepropvariantcollectionvalue"**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md) | Fügt einen neuen **iportabledevicepropvariantcollection** -Wert hinzu (Typ VT \_ unknown) oder überschreibt eine vorhandene.<br/> |
| [**"Stiportableendvicevaluescollectionvalue"**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)           | Fügt einen neuen **iportabledevicevaluescollection** -Wert hinzu (Typ VT \_ unknown) oder überschreibt eine vorhandene.<br/>      |
| [**"Stiportableendvicevaluesvalue"**](iportabledevicevalues-setiportabledevicevaluesvalue.md)                               | Fügt einen neuen **iportabledevicevalues** -Wert hinzu (Typ VT \_ unknown) oder überschreibt eine vorhandene.<br/>                |
| [**"Enumerationswert"**](iportabledevicevalues-setiunknownvalue.md)                                                         | Fügt einen neuen **IUnknown** -Wert (Typ VT \_ unknown) hinzu oder überschreibt einen vorhandenen IUnknown-Wert.<br/>                             |
| [**SetKeyValue**](iportabledevicevalues-setkeyvalue.md)                                                                   | Fügt einen neuen **PropertyKey** -Wert (Type VT \_ unknown) hinzu oder überschreibt ein vorhandenes Element.<br/>                          |
| [**Setsignedintegervalue**](iportabledevicevalues-setsignedintegervalue.md)                                               | Fügt einen neuen **Long** -Wert (Type VT \_ I4) hinzu oder überschreibt ein vorhandenes.<br/>                                      |
| [**Setsignedlargeingetegervalue**](iportabledevicevalues-setsignedlargeintegervalue.md)                                     | Fügt einen neuen **Longlong** -Wert (Typ VT \_ I8) hinzu oder überschreibt eine vorhandene.<br/>                                  |
| [**SetStringValue**](iportabledevicevalues-setstringvalue.md)                                                             | Fügt einen neuen Zeichen folgen Wert (Typ VT \_ LPWSTR) hinzu oder überschreibt einen vorhandenen Zeichen folgen Wert.<br/>                                    |
| [**"Stunsignedintegervalue"**](iportabledevicevalues-setunsignedintegervalue.md)                                           | Fügt einen neuen **ulong** -Wert (Type VT \_ UI4) hinzu oder überschreibt eine vorhandene.<br/>                                    |
| [**"Stunsignedlargeintegervalue"**](iportabledevicevalues-setunsignedlargeintegervalue.md)                                 | Fügt einen neuen **ULONGLONG** -Wert (Type VT \_ UI8) hinzu oder überschreibt eine vorhandene.<br/>                                |
| [**SetValue**](iportabledevicevalues-setvalue.md)                                                                         | Fügt einen neuen **PROPVARIANT** -Wert hinzu oder überschreibt eine vorhandene.<br/>                                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sammlungs Schnittstellen**](collection-interfaces.md)
</dt> </dl>

 

