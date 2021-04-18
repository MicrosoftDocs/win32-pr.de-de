---
description: Tragbare Windows-Geräte unterstützen die folgenden Eigenschafts Attribute.
ms.assetid: 129ee2b8-075c-457a-85ef-658a56eed541
title: Eigenschafts Attribute (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Property
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 9e48a4f81a6223ed034f6de14fe104a1a2aa4393
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358710"
---
# <a name="property-attributes-portabledeviceh"></a>Eigenschafts Attribute (portabledevice. h)

Tragbare Windows-Geräte unterstützen die folgenden Eigenschafts Attribute. Diese Attribute werden von den folgenden Methoden zurückgegeben:

-   [**Iportabledebug:: getfixedpropertyattribute**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)
-   [**Iportabledeviceproperties:: getpropertyattributs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getpropertyattributes)
-   [**Iportabletoviceservicecapabili:: getformatpropertyattribute**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatpropertyattributes)



| Attribut                                           | VarType         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD- \_ Eigenschafts \_ Attribut \_ kann \_ Löschen**           | **VT \_ bool**    | Ein boolescher Wert, der angibt, ob der Client die Eigenschaft löschen kann. Um eine Eigenschaft zu löschen, legen Sie Ihren Wert auf VT \_ Empty fest.                                                                                                                                                                                                                                                                   |
| **WPD- \_ Eigenschafts \_ Attribut \_ kann \_ Lesen**             | **VT \_ bool**    | Ein boolescher Wert, der angibt, ob der Client die Eigenschaft lesen kann.                                                                                                                                                                                                                                                                                                                       |
| **WPD- \_ Eigenschafts \_ Attribut \_ kann \_ schreiben**            | **VT \_ bool**    | Ein boolescher Wert, der angibt, ob der Client die Eigenschaft ändern kann.                                                                                                                                                                                                                                                                                                                     |
| **Standardwert des WPD- \_ Eigenschaften \_ Attributs \_ \_**        | VT \_ *xxxx*      | Ein Wert, der vom Gerät definiert wird, das den Standardwert einer Eigenschaft angibt. Dies gilt nur für beschreibbare Eigenschaften.                                                                                                                                                                                                                                                               |
| **\_ \_ \_ Enumerationselemente für WPD-Eigenschaften Attribute \_** | **VT \_ unbekannt** | Eine [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Schnittstelle, die eine Auflistung von Werten für eine Eigenschaft enthält, deren **WPD- \_ Eigenschafts \_ Attribut \_ Form** -Attribut die **\_ \_ \_ \_ Enumeration des WPD-Eigenschafts** Attributs ist. Der Datentyp hängt von der Eigenschaft ab, die abgefragt wird.                                                                              |
| **Eigenschaft ' schnelles WPD- \_ Eigenschaften \_ Attribut ' \_ \_**        | **VT \_ bool**    | True gibt an, dass diese Eigenschaft zur Gruppe der *schnellen Eigenschaften* gehört. Dies sind Eigenschaften, die schnell vom Gerät abgerufen werden können.                                                                                                                                                                                                                                                        |
| **WPD- \_ Eigenschafts \_ Attribut- \_ Formular**                  | **VT \_ UI4**     | Ein [**wpdattributeform**](wpdattributeform.md) -Enumerationswert, der die Form der gültigen Werte angibt, die für diese Eigenschaft zulässig sind.                                                                                                                                                                                                                                                         |
| **WPD- \_ Eigenschafts \_ Attribut \_ Name**                  | **VT \_ LPWSTR**  | Eine Zeichenfolge, die den Skript freundlichen Namen der Eigenschaft angibt. Gültige Zeichen sind alphanumerisch \[ a-Za-z0-9 \] und ' \_ '.                                                                                                                                                                                                                                                                    |
| **Wert des WPD- \_ Eigenschafts \_ Attribut \_ Bereichs \_ Max**            | VT \_ *xxxx*      | Der maximale Wert für eine Eigenschaft, deren Attribut Formular Attribut des WPD-Eigenschafts Attributs dem **\_ \_ \_ Formular \_ Bereich der WPD-Eigenschaft** entspricht. **\_ \_ \_** Der Datentyp kann ein beliebiger numerischer Typ sein.                                                                                                                                                                                                               |
| **Bereich des WPD- \_ Eigenschaften \_ Attributs \_ \_ Min.**            | VT \_ *xxxx*      | Der minimale Wert für eine Eigenschaft, deren Attribut Formular Attribut des WPD-Eigenschafts Attributs dem **\_ \_ \_ Formular \_ Bereich der WPD-Eigenschaft** entspricht. **\_ \_ \_** Der Datentyp kann ein beliebiger numerischer Typ sein.                                                                                                                                                                                                               |
| **Bereich des WPD- \_ Eigenschafts \_ Attribut \_ Bereichs \_**           | VT \_ *xxxx*      | Der Schrittwert für eine Eigenschaft, deren Attribut Formular Attribut für **WPD \_ \_ \_** -Eigenschaften **Attribut der \_ \_ \_ Formular \_ Bereich der WPD-Eigenschaft** ist. Der Schritt gibt an, wie viel eine Bereichs Eigenschaft geändert werden muss. Beispielsweise kann eine Eigenschaft mit einem Mindestwert von 10, einem maximalen Wert von 20 und einem Schritt von 5 die folgenden Werte aufweisen: **10**, **15**, **20**. Der Datentyp kann ein beliebiger numerischer Typ sein. |
| **\_ \_ \_ regulärer Ausdruck für WPD-Eigenschaften Attribut \_**   | **VT \_ LPWSTR**  | Eine Zeichenfolge für reguläre Ausdrücke, die zulässige Werte für Eigenschaften angibt, deren Form **\_ \_ \_ \_ regulärer \_ Ausdruck für das WPD-Eigenschafts Attribut** ist.                                                                                                                                                                                                                                             |
| **WPD- \_ Eigenschafts \_ Attribut \_ VarType**               | **VT \_ UI4**     | Eine ganze Zahl, die den VarType der Eigenschaft angibt, z. **b. VT \_ bool**.                                                                                                                                                                                                                                                                                                              |
| **maximale Größe des WPD- \_ Eigenschafts \_ Attributs \_ \_**             | **VT \_ UI8**     | Ein-Wert, der die maximale Größe für den Wert dieser Eigenschaft in Bytes angibt.                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften**](properties-and-attributes.md)
</dt> </dl>

 

 




