---
description: 'Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Attribute für Formate auf einem Geräte Dienst. Diese Attribute werden von der iportabledeviceservicecapabili:: getformattribute-Methode zurückgegeben.'
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: Format Attribute (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Format
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 559f731ec7d61007b05e4625ff67488b5ef482fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371152"
---
# <a name="format-attributes"></a>Format Attribute

Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Attribute für Formate auf einem Geräte Dienst. Diese Attribute werden von der [**iportabledeviceservicecapabili:: getformattribute**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) -Methode zurückgegeben.




| **Attribut**                        | **VarType**    | **Beschreibung**                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| **WPD- \_ Format \_ Attribut \_ MimeType** | **VT \_ LPWSTR** | Der MIME-Typ des Formats.                                                                                                     |
| **\_ \_ Attribut \_ Name für WPD-Format**     | **VT \_ LPWSTR** | Eine Zeichenfolge, die den Skript freundlichen Namen des Formats angibt. Gültige Zeichen sind alphanumerisch \[ a-Za-z0-9 \] und ' \_ '. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften und Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




