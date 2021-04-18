---
description: Windows Portable Devices (WPD) unterstützt die folgenden Eigenschaften von Befehlsparametern.
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: Befehlsparameter (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Command
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7687488c38f95fd6d7e7b69d64ad6ae32631700d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371221"
---
# <a name="command-parameters"></a>Befehlsparameter

Windows Portable Devices (WPD) unterstützt die folgenden Eigenschaften von Befehlsparametern.




| **Eigenschaft**                                            | **VarType**     | **Beschreibung**                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ allgemeine \_ Client \_ Informationen für WPD-Eigenschaften**          | **VT \_ unbekannt** | Eine [**iportableendvicevalues**](iportabledevicevalues.md) -Schnittstelle, die der Treiber verwendet, um den Client zu identifizieren.                                                             |
| **WPD- \_ Eigenschaft allgemeiner \_ \_ Client \_ Informations \_ Kontext** | **VT \_ LPWSTR**  | Ein vom Treiber angegebener Kontext, der einen Client für alle nachfolgenden Vorgänge identifiziert.                                                                                          |
| **\_ \_ allgemeine \_ Befehls \_ Kategorie der WPD-Eigenschaft**            | **VT \_ CLSID**   | Der **GUID** -Teil des **PropertyKey** -Werts des Befehls.                                                                                                            |
| **\_ \_ allgemeine \_ Befehls- \_ ID für WPD-Eigenschaft**                  | **VT \_ UI4**     | Der persistente eindeutige ID-Teil (PID) des **PropertyKey** -Werts des Befehls.                                                                                          |
| **Allgemeine WPD- \_ Eigenschaft ( \_ \_ Befehls \_ Ziel)**              | **VT \_ LPWSTR**  | Der Zielobjekt Bezeichner.                                                                                                                                                |
| **WPD- \_ Eigenschaft allgemeiner \_ \_ Treiber \_ Fehler \_ Code**          | **VT \_ UI4**     | Ein Treiber spezifischer Fehlercode, der von einem WPD-Treiber zurückgegeben wird.                                                                                                                       |
| **WPD- \_ Eigenschaft allgemeiner \_ \_ HRESULT**                      | **VT- \_ Fehler**   | Der **HRESULT** -Wert, der von einem WPD-Treiber für einen bestimmten Vorgang zurückgegeben wird.                                                                                                   |
| **\_ \_ allgemeine \_ Objekt- \_ IDs der WPD-Eigenschaft**                  | **VT \_ unbekannt** | Eine [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Schnittstelle vom Variant-Typ **VT \_ LPWSTR** , die eine Liste von Objekt bezeichgern enthält. |
| **WPD- \_ Eigenschaft \_ allgemeine \_ persistente \_ eindeutige \_ IDs**      | **VT \_ unbekannt** | Eine [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Schnittstelle vom Variant-Typ **VT \_ LPWSTR** , die eine Liste von PIDs enthält.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften und Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




