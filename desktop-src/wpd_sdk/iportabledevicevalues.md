---
description: Die IPortableDeviceValues-Schnittstelle enthält eine Auflistung von PROPERTYKEY/PROPVARIANT-Paaren.
ms.assetid: a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f
title: IPortableDeviceValues-Schnittstelle (PortableDeviceTypes.h)
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
ms.openlocfilehash: 7f7aaceff66cd817666dd05b92243239f860b2f59a993e4afca1831fc8085de0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930000"
---
# <a name="iportabledevicevalues-interface"></a>IPortableDeviceValues-Schnittstelle

Die **IPortableDeviceValues-Schnittstelle** enthält eine Auflistung von **PROPERTYKEY** / **PROPVARIANT-Paaren.** Werte in der Auflistung müssen nicht derselbe VARTYPE sein.

Werte werden als Schlüssel-Wert-Paare gespeichert. Jeder Schlüssel muss in der Auflistung eindeutig sein. Clients können nach Elementen mit **PROPERTYKEY oder** einem nullbasierten Index suchen. Datenwerte werden als **PROPVARIANT-Strukturen** gespeichert. Sie können Werte eines beliebigen Typs hinzufügen oder abrufen, indem Sie die generischen Methoden **SetValue** und **GetValue** verwenden, oder Sie fügen Elemente hinzu, indem Sie die -Methode verwenden, die für den Typ der hinzugefügten Daten spezifisch ist.

Die **Get...-Methoden** erfordern, dass der Aufrufer alle abgerufenen Werte entsprechend frei gibt. Die **Set...-Methoden** kopieren den Wert in die Auflistung.

Wenn eine **IPortableDeviceValues-Schnittstelle** freigegeben wird, ruft sie **Clear** auf, wodurch der Arbeitsspeicher freigegeben wird, der allen Membern entsprechend zugeordnet wurde.

Diese Schnittstelle kann von einer Methode abgerufen werden. Wenn ein neues Objekt erforderlich ist, rufen Sie **CoCreate** mit **CLSID \_ PortableDeviceValues auf.**

## <a name="members"></a>Member

Die **IPortableDeviceValues-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPortableDeviceValues** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IPortableDeviceValues-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                                     | BESCHREIBUNG                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**Klar**](iportabledevicevalues-clear.md)                                                                               | Löscht alle Elemente aus der Auflistung.<br/>                                                                      |
| [**CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)                                   | Kopiert den Inhalt eines **IPropertyStore in** die Auflistung.<br/>                                           |
| [**CopyValuesToPropertyStore**](iportabledevicevalues-copyvaluestopropertystore.md)                                       | Kopiert alle Werte aus einer Auflistung in eine **IPropertyStore-Schnittstelle.**<br/>                               |
| [**GetAt**](iportabledevicevalues-getat.md)                                                                               | Ruft mithilfe des angegebenen nullbasierten Indexes einen Wert aus der Auflistung ab.<br/>                                  |
| [**GetBoolValue**](iportabledevicevalues-getboolvalue.md)                                                                 | Ruft einen **BOOL-Wert** (Typ VT BOOL) ab, \_ der durch einen Schlüssel angegeben wird.<br/>                                              |
| [**GetBufferValue**](iportabledevicevalues-getbuffervalue.md)                                                             | Ruft einen Bytearraywert (Typ VT \_ VECTOR \| VT UI1) ab, der durch einen Schlüssel angegeben \_ wird.<br/>                               |
| [**GetCount**](iportabledevicevalues-getcount.md)                                                                         | Ruft die Anzahl der Elemente in der Auflistung ab.<br/>                                                            |
| [**GetErrorValue**](iportabledevicevalues-geterrorvalue.md)                                                               | Ruft einen **HRESULT-Wert** (Typ VT ERROR) ab, \_ der durch einen Schlüssel angegeben wird.<br/>                                         |
| [**GetFloatValue**](iportabledevicevalues-getfloatvalue.md)                                                               | Ruft einen **FLOAT-Wert** (Typ VT \_ R4) ab, der durch einen Schlüssel angegeben wird.<br/>                                               |
| [**GetGuidValue**](iportabledevicevalues-getguidvalue.md)                                                                 | Ruft einen **GUID-Wert** (Typ VT \_ CLSID) ab, der durch einen Schlüssel angegeben wird.<br/>                                             |
| [**GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)                 | Ruft einen **IPortableDeviceKeyCollection-Wert** (Typ VT UNKNOWN) ab, der \_ durch einen Schlüssel angegeben wird.<br/>                  |
| [**GetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md) | Ruft einen **IPortableDevicePropVariantCollection-Wert** (Typ VT UNKNOWN) ab, der \_ durch einen Schlüssel angegeben wird.<br/>          |
| [**GetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)           | Ruft einen **IPortableDeviceValuesCollection-Wert** (Typ VT UNKNOWN) ab, der \_ durch einen Schlüssel angegeben wird.<br/>               |
| [**GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md)                               | Ruft einen **IPortableDeviceValues-Wert** (Typ VT UNKNOWN) ab, der \_ durch einen Schlüssel angegeben wird.<br/>                         |
| [**GetIUnknownValue**](iportabledevicevalues-getiunknownvalue.md)                                                         | Ruft einen **IUnknown-Schnittstellenwert** (Typ VT UNKNOWN) ab, \_ der durch einen Schlüssel angegeben wird.<br/>                            |
| [**GetKeyValue**](iportabledevicevalues-getkeyvalue.md)                                                                   | Ruft einen durch einen **Schlüssel angegebenen PROPERTYKEY-Wert** ab.<br/>                                                       |
| [**GetSignedIntegerValue**](iportabledevicevalues-getsignedintegervalue.md)                                               | Ruft einen **LONG-Wert** (Typ VT \_ I4) ab, der durch einen Schlüssel angegeben wird.<br/>                                                |
| [**GetSignedLargeIntegerValue**](iportabledevicevalues-getsignedlargeintegervalue.md)                                     | Ruft einen **LONGLONG-Wert** (Typ VT I8) ab, \_ der durch einen Schlüssel angegeben wird.<br/>                                            |
| [**GetStringValue**](iportabledevicevalues-getstringvalue.md)                                                             | Ruft einen durch einen Schlüssel angegebenen Zeichenfolgenwert (Typ VT \_ LPWSTR) ab.<br/>                                              |
| [**GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)                                           | Ruft einen **ULONG-Wert** (Typ VT UI4) ab, \_ der durch einen Schlüssel angegeben wird.<br/>                                              |
| [**GetUnsignedLargeIntegerValue**](iportabledevicevalues-getunsignedlargeintegervalue.md)                                 | Ruft einen **ULONGLONG-Wert** (Typ VT UI8) ab, \_ der durch einen Schlüssel angegeben wird.<br/>                                          |
| [**GetValue**](iportabledevicevalues-getvalue.md)                                                                         | Ruft einen **PROPVARIANT-Wert** ab, der durch einen Schlüssel angegeben wird.<br/>                                                       |
| [**RemoveValue**](iportabledevicevalues-removevalue.md)                                                                   | Entfernt ein Element aus der Auflistung.<br/>                                                                        |
| [**SetBoolValue**](iportabledevicevalues-setboolvalue.md)                                                                 | Fügt einen neuen **booleschen Wert** hinzu (Typ VT \_ BOOL) oder überschreibt einen vorhandenen.<br/>                                 |
| [**SetBufferValue**](iportabledevicevalues-setbuffervalue.md)                                                             | Fügt einen neuen **BYTE-Wert** \* hinzu (Typ VT \_ VECTOR \| VT \_ UI1) oder überschreibt einen vorhandenen.<br/>                     |
| [**SetErrorValue**](iportabledevicevalues-seterrorvalue.md)                                                               | Fügt einen neuen **HRESULT-Wert** hinzu (Typ VT \_ ERROR) oder überschreibt einen vorhandenen.<br/>                                |
| [**SetFloatValue**](iportabledevicevalues-setfloatvalue.md)                                                               | Fügt einen neuen **FLOAT-Wert** (Typ VT \_ R4) hinzu oder überschreibt einen vorhandenen.<br/>                                     |
| [**SetGuidValue**](iportabledevicevalues-setguidvalue.md)                                                                 | Fügt einen neuen **GUID-Wert** hinzu (Typ VT \_ CLSID) oder überschreibt einen vorhandenen.<br/>                                   |
| [**SetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)                 | Fügt einen neuen **IPortableDeviceKeyCollectionValue-Wert** hinzu (Typ VT UNKNOWN) oder \_ überschreibt einen vorhandenen Wert.<br/>    |
| [**SetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md) | Fügt einen neuen **IPortableDevicePropVariantCollection-Wert** (Typ VT UNKNOWN) hinzu oder überschreibt \_ einen vorhandenen.<br/> |
| [**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)           | Fügt einen neuen **IPortableDeviceValuesCollection-Wert** hinzu (Typ VT UNKNOWN) oder \_ überschreibt einen vorhandenen Wert.<br/>      |
| [**SetIPortableDeviceValuesValue**](iportabledevicevalues-setiportabledevicevaluesvalue.md)                               | Fügt einen neuen **IPortableDeviceValues-Wert** hinzu (Typ VT UNKNOWN) oder \_ überschreibt einen vorhandenen Wert.<br/>                |
| [**SetIUnknownValue**](iportabledevicevalues-setiunknownvalue.md)                                                         | Fügt einen neuen **IUnknown-Wert** hinzu (Typ VT \_ UNKNOWN) oder überschreibt einen vorhandenen.<br/>                             |
| [**SetKeyValue**](iportabledevicevalues-setkeyvalue.md)                                                                   | Fügt einen neuen **PROPERTYKEY-Wert** (Typ VT UNKNOWN) hinzu oder \_ überschreibt einen vorhandenen Wert.<br/>                          |
| [**SetSignedIntegerValue**](iportabledevicevalues-setsignedintegervalue.md)                                               | Fügt einen neuen **LONG-Wert** hinzu (Typ VT \_ I4) oder überschreibt einen vorhandenen.<br/>                                      |
| [**SetSignedLargeIntegerValue**](iportabledevicevalues-setsignedlargeintegervalue.md)                                     | Fügt einen neuen **LONGLONG-Wert** (Typ VT \_ I8) hinzu oder überschreibt einen vorhandenen.<br/>                                  |
| [**SetStringValue**](iportabledevicevalues-setstringvalue.md)                                                             | Fügt einen neuen Zeichenfolgenwert (Typ VT \_ LPWSTR) hinzu oder überschreibt einen vorhandenen.<br/>                                    |
| [**SetUnsignedIntegerValue**](iportabledevicevalues-setunsignedintegervalue.md)                                           | Fügt einen neuen **ULONG-Wert** hinzu (Typ VT \_ UI4) oder überschreibt einen vorhandenen.<br/>                                    |
| [**SetUnsignedLargeIntegerValue**](iportabledevicevalues-setunsignedlargeintegervalue.md)                                 | Fügt einen neuen **ULONGLONG-Wert** hinzu (Typ VT \_ UI8) oder überschreibt einen vorhandenen.<br/>                                |
| [**SetValue**](iportabledevicevalues-setvalue.md)                                                                         | Fügt einen neuen **PROPVARIANT-Wert** hinzu oder überschreibt einen vorhandenen.<br/>                                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sammlungsschnittstellen**](collection-interfaces.md)
</dt> </dl>

 

