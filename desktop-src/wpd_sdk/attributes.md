---
description: Windows Portable Geräte unterstützen die folgenden Eigenschaftsattribute.
ms.assetid: 129ee2b8-075c-457a-85ef-658a56eed541
title: Eigenschaftenattribute (PortableDevice.h)
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
ms.openlocfilehash: 85bf37b716349aae164594eeb8085e8c6df9dc5445728bbf7d9222705a9cb8c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843563"
---
# <a name="property-attributes-portabledeviceh"></a>Eigenschaftenattribute (PortableDevice.h)

Windows Portable Geräte unterstützen die folgenden Eigenschaftsattribute. Diese Attribute werden von den folgenden Methoden zurückgegeben:

-   [**IPortableDeviceCapabilities::GetFixedPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)
-   [**IPortableDeviceProperties::GetPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getpropertyattributes)
-   [**IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatpropertyattributes)



| attribute                                           | VarType         | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ WPD-EIGENSCHAFTSATTRIBUT \_ KANN GELÖSCHT \_ WERDEN**           | **VT \_ BOOL**    | Ein boolescher Wert, der angibt, ob der Client die Eigenschaft löschen kann. Um eine Eigenschaft zu löschen, legen Sie ihren Wert auf VT \_ EMPTY fest.                                                                                                                                                                                                                                                                   |
| **\_ \_ WPD-EIGENSCHAFTSATTRIBUT \_ KANN GELESEN \_ WERDEN**             | **VT \_ BOOL**    | Ein boolescher Wert, der angibt, ob der Client die Eigenschaft lesen kann.                                                                                                                                                                                                                                                                                                                       |
| **\_ \_ WPD-EIGENSCHAFTSATTRIBUT \_ KANN \_ SCHREIBEN**            | **VT \_ BOOL**    | Ein boolescher Wert, der angibt, ob der Client die Eigenschaft ändern kann.                                                                                                                                                                                                                                                                                                                     |
| **STANDARDWERT DES \_ WPD-EIGENSCHAFTSATTRIBUTS \_ \_ \_**        | VT \_ *XXXX*      | Ein -Wert, der vom Gerät definiert wird, das den Standardwert einer Eigenschaft angibt. Dies gilt nur für schreibbare Eigenschaften.                                                                                                                                                                                                                                                               |
| **\_ \_ WPD-EIGENSCHAFTENATTRIBUT-ENUMERATIONSELEMENTE \_ \_** | **VT \_ UNKNOWN** | Eine [**IPortableDevicePropVariantCollection-Schnittstelle,**](iportabledevicepropvariantcollection.md) die eine Auflistung von Werten für eine Eigenschaft enthält, deren **WPD \_ PROPERTY ATTRIBUTE \_ \_ FORM-Attribut** **WPD PROPERTY ATTRIBUTE \_ FORM \_ \_ \_ ENUMERATION** ist. Der Datentyp hängt von der abgefragten Eigenschaft ab.                                                                              |
| **\_ \_ WPD-EIGENSCHAFTSATTRIBUT \_ \_ FAST-EIGENSCHAFT**        | **VT \_ BOOL**    | True gibt an, dass diese Eigenschaft zur *Schnellen Eigenschaftengruppe* gehört. Dies sind Eigenschaften, die schnell vom Gerät abgerufen werden können.                                                                                                                                                                                                                                                        |
| **\_ \_ WPD-EIGENSCHAFTENATTRIBUTFORMULAR \_**                  | **VT \_ UI4**     | Ein [**wpdAttributeForm-Enumerationswert,**](wpdattributeform.md) der die Form der gültigen Werte angibt, die für diese Eigenschaft zulässig sind.                                                                                                                                                                                                                                                         |
| **\_ \_ WPD-EIGENSCHAFTENATTRIBUTNAME \_**                  | **VT \_ LPWSTR**  | Eine Zeichenfolge, die den skriptfreundlichen Namen der Eigenschaft angibt. Gültige Zeichen sind alphanumerische \[ Zeichen a-zA-Z0-9 \] und ' \_ '.                                                                                                                                                                                                                                                                    |
| **WPD \_ PROPERTY \_ ATTRIBUTE \_ RANGE \_ MAX**            | VT \_ *XXXX*      | Der Maximale Wert für eine Eigenschaft, deren **WPD \_ PROPERTY ATTRIBUTE \_ \_ FORM-Attribut** **WPD PROPERTY ATTRIBUTE FORM \_ \_ \_ \_ RANGE** ist. Der Datentyp kann jeder der numerischen Typen sein.                                                                                                                                                                                                               |
| **\_ \_ WPD-EIGENSCHAFTSATTRIBUTBEREICH \_ \_ MIN**            | VT \_ *XXXX*      | Der Mindestwert für eine Eigenschaft, deren **WPD \_ PROPERTY ATTRIBUTE \_ \_ FORM-Attribut** **WPD PROPERTY ATTRIBUTE FORM \_ \_ \_ \_ RANGE** ist. Der Datentyp kann jeder der numerischen Typen sein.                                                                                                                                                                                                               |
| **SCHRITT \_ \_ "WPD-EIGENSCHAFTENATTRIBUTBEREICH" \_ \_**           | VT \_ *XXXX*      | Der Schrittwert für eine Eigenschaft, deren **WPD \_ PROPERTY ATTRIBUTE \_ \_ FORM-Attribut** **WPD PROPERTY ATTRIBUTE FORM \_ \_ \_ \_ RANGE** ist. Der Schritt gibt an, wie stark sich eine Bereichseigenschaft ändern muss. Eine Eigenschaft mit einem Mindestwert von 10, einem Maximalwert von 20 und einem Schritt 5 kann beispielsweise die folgenden Werte aufweisen: **10**, **15**, **20**. Der Datentyp kann jeder der numerischen Typen sein. |
| **\_ \_ WPD-EIGENSCHAFTSATTRIBUT \_ REGULÄRER \_ AUSDRUCK**   | **VT \_ LPWSTR**  | Eine Zeichenfolge für reguläre Ausdrücke, die zulässige Werte für Eigenschaften angibt, deren Formular **WPD \_ PROPERTY ATTRIBUTE FORM REGULAR \_ \_ \_ \_ EXPRESSION** ist.                                                                                                                                                                                                                                             |
| **\_ \_ WPD-EIGENSCHAFTSATTRIBUT \_ VARTYPE**               | **VT \_ UI4**     | Eine ganze Zahl, die den VARTYPE der Eigenschaft angibt, z. B. **VT \_ BOOL**.                                                                                                                                                                                                                                                                                                              |
| **MAXIMALE \_ GRÖßE DES WPD-EIGENSCHAFTSATTRIBUTS \_ \_ \_**             | **VT \_ UI8**     | Ein -Wert, der die maximale Größe für den Wert dieser Eigenschaft in Bytes angibt.                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Eigenschaften**](properties-and-attributes.md)
</dt> </dl>

 

 




