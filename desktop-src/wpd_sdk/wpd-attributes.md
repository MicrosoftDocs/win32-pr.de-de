---
description: Für Windows 7 unterstützt Windows Portable Devices die folgenden Parameterattribute für Methoden und Ereignisse eines Gerätediensts.
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: Parameterattribute (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Parameter
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 8004f4e2f9f7c22d795b6ce4e4cb0affac1b55ecd876c21288c02e226ee14262
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006110"
---
# <a name="parameter-attributes"></a>Parameterattribute

Für Windows 7 unterstützt Windows Portable Devices die folgenden Parameterattribute für Methoden und Ereignisse eines Gerätediensts. Diese Attribute werden von den folgenden Methoden zurückgegeben:

-   [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| attribute                                            | VarType         | BESCHREIBUNG                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **STANDARDWERT DES \_ WPD-PARAMETERATTRIBUTS \_ \_ \_**        | VT \_ *XXXX*      | Der Standardwert des Parameters.                                                                                                                                                         |
| **\_ \_ WPD-PARAMETERATTRIBUT-ENUMERATIONSELEMENTE \_ \_** | **VT \_ UNKNOWN** | Eine [**IPortableDevicePropVariantCollection-Schnittstelle,**](iportabledevicepropvariantcollection.md) die die Enumerationswerte für den Parameter enthält.                                   |
| **\_ \_ \_ WPD-PARAMETERATTRIBUTFORMULAR**                  | **VT \_ UI4**     | Die Form der zulässigen gültigen Parameterwerte.                                                                                                                                                 |
| **MAXIMALE \_ GRÖßE DES WPD-PARAMETERATTRIBUTS \_ \_ \_**             | **VT \_ UI8**     | Die maximale Größe des Parameters in Bytes.                                                                                                                                               |
| **\_ \_ WPD-PARAMETERATTRIBUTNAME \_**                  | **VT \_ LPWSTR**  | Eine Zeichenfolge, die den skriptfreundlichen Namen eines Ereignis- oder Methodenparameters angibt. Gültige Zeichen sind alphanumerische \[ Zeichen a-zA-Z0-9 \] und ' \_ '.                                                 |
| **\_ \_ WPD-PARAMETERATTRIBUTREIHENFOLGE \_**                 | **VT \_ UI4**     | Der nullbasierte Index der Parameterreihenfolge, sodass der Reihenfolgenwert 0 dem ersten Parameter entspricht.                                                                                       |
| **WPD \_ PARAMETER \_ ATTRIBUTE \_ RANGE \_ MIN**            | VT \_ *XXXX*      | Der Höchstwert für einen Parameter im Format WPD \_ PARAMETER \_ ATTRIBUTE FORM \_ \_ RANGE.                                                                                                       |
| **WPD \_ PARAMETER \_ ATTRIBUTE \_ RANGE \_ MAX**            | VT \_ *XXXX*      | Der Mindestwert für einen Parameter im Format WPD \_ PARAMETER \_ ATTRIBUTE FORM \_ \_ RANGE.                                                                                                       |
| **SCHRITT \_ \_ "WPD-PARAMETERATTRIBUTBEREICH" \_ \_**           | VT \_ *XXXX*      | Der Schrittwert für einen Parameter im Format WPD \_ PARAMETER \_ ATTRIBUTE FORM \_ \_ RANGE.                                                                                                          |
| **WPD \_ PARAMETER \_ ATTRIBUTE \_ REGULAR \_ EXPRESSION**   | **VT \_ LPWSTR**  | Ein regulärer Ausdruck, der akzeptable Werte für Parameter der Form WPD \_ PARAMETER ATTRIBUTE FORM REGULAR EXPRESSION \_ \_ \_ \_ angibt.                                                      |
| **\_VERWENDUNGSTYP DES WPD-PARAMETERATTRIBUTS \_ \_ \_**           | **VT \_ UI4**     | Eine ganze Zahl, die die Verwendung eines Methodenparameters angibt, z. B. in/out. Gültige Werte sind vom [**WPD \_ PARAMETER USAGE \_ TYPES-Enumerationstyp. \_**](wpd-parameter-usage-types.md) |
| **\_ \_ WPD-PARAMETERATTRIBUT \_ VARTYPE**               | **VT \_ UI4**     | Der VarType-Parameter.                                                                                                                                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften und Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




