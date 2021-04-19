---
description: Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Parameter Attribute für Methoden und Ereignisse eines Geräte Dienstanbieter.
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: Parameter Attribute (portabledevice. h)
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
ms.openlocfilehash: 113b2b35a5b6e61cd2cc1d3666d1a13fbade5ec7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106363209"
---
# <a name="parameter-attributes"></a>Parameterattribute

Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Parameter Attribute für Methoden und Ereignisse eines Geräte Dienstanbieter. Diese Attribute werden von den folgenden Methoden zurückgegeben:

-   [**Iportabletoviceservicecapabili:: getmethodparameterattribute**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [**Iportabletoviceservicecapabili:: geteventparameterattribute**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| Attribut                                            | VarType         | BESCHREIBUNG                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Standardwert des WPD- \_ Parameter \_ Attributs \_ \_**        | VT \_ *xxxx*      | Der Standardwert des Parameters.                                                                                                                                                         |
| **\_ \_ \_ Enumerationselemente für WPD-Parameter Attribute \_** | **VT \_ unbekannt** | Eine [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Schnittstelle, die die Enumerationswerte für den Parameter enthält.                                   |
| **WPD- \_ Parameter- \_ Attribut \_ Formular**                  | **VT \_ UI4**     | Die Form gültiger zulässiger Parameterwerte.                                                                                                                                                 |
| **maximale Größe des WPD- \_ Parameter \_ Attributs \_ \_**             | **VT \_ UI8**     | Die maximale Größe des Parameters in Byte.                                                                                                                                               |
| **Name des WPD- \_ Parameter \_ Attributs \_**                  | **VT \_ LPWSTR**  | Eine Zeichenfolge, die den Skript freundlichen Namen eines Ereignisses oder Methoden Parameters angibt. Gültige Zeichen sind alphanumerisch \[ a-Za-z0-9 \] und ' \_ '.                                                 |
| **Reihenfolge der WPD- \_ Parameter \_ Attribute \_**                 | **VT \_ UI4**     | Der null basierte Index für die Parameterreihenfolge, sodass der Auftragswert 0 dem ersten Parameter entspricht.                                                                                       |
| **Bereich des WPD- \_ Parameter \_ \_ Bereichs \_ Min.**            | VT \_ *xxxx*      | Der maximale Wert für einen Parameter im Formular Bereich des WPD- \_ Parameter \_ Attributs \_ \_ .                                                                                                       |
| **Bereich des WPD- \_ Parameter \_ Attributs \_ \_ Max**            | VT \_ *xxxx*      | Der minimale Wert für einen Parameter im Formular Bereich des WPD- \_ Parameter \_ Attributs \_ \_ .                                                                                                       |
| **Bereich für \_ den \_ Attribut \_ Bereich \_ für WPD-Parameter**           | VT \_ *xxxx*      | Der Schrittwert für einen Parameter im Formular Bereich des WPD- \_ Parameter \_ Attributs \_ \_ .                                                                                                          |
| **regulärer Ausdruck des WPD- \_ Parameter \_ Attributs \_ \_**   | **VT \_ LPWSTR**  | Ein regulärer Ausdruck, der akzeptable Werte für die Parameter der Form eines regulären Ausdrucks der Form des WPD- \_ Parameter \_ Attributs angibt \_ \_ \_ .                                                      |
| **Benutzertyp des WPD- \_ Parameter \_ Attributs \_ \_**           | **VT \_ UI4**     | Eine ganze Zahl, die die Verwendung eines Methoden Parameters angibt, z. b. in/out. Gültige Werte sind der Enumerationstyp für die [**Verwendung von WPD- \_ Parametern \_ \_**](wpd-parameter-usage-types.md) . |
| **WPD- \_ Parameter \_ Attribut \_ VarType**               | **VT \_ UI4**     | Der VarType-Parameter.                                                                                                                                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften und Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




