---
description: Tragbare Windows-Geräte unterstützen die folgenden e-Mail-Eigenschaften.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: E-Mail-Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Email
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: de25d73e9fb331538ecdbf5f22306d85c282b338
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361535"
---
# <a name="email-properties"></a>E-Mail-Eigenschaften

Tragbare Windows-Geräte unterstützen die folgenden e-Mail-Eigenschaften.



| Eigenschaft                         | VarType        | BESCHREIBUNG                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ -e-Mail \_ Bcc- \_ Zeile**        | **VT \_ LPWSTR** | Die Bcc-Empfänger der e-Mail-Nachricht. BCC-Empfänger erhalten eine Kopie der e-Mail, deren Namen jedoch nicht als Empfänger angezeigt werden.   |
| **WPD \_ -e-Mail- \_ \_ Leitung**         | **VT \_ LPWSTR** | Die CC-Empfänger der e-Mail-Nachricht. CC-Empfänger erhalten eine Kopie der e-Mail-Nachricht, deren Namen als Empfänger angezeigt werden. |
| **WPD \_ -e-Mail \_ enthält \_ Anlagen** | **VT \_ bool**   | Ein boolescher Wert, der angibt, ob diese e-Mail über Anlagen verfügt.                                                               |
| **WPD \_ -e-Mail \_ \_ wurde \_ gelesen**  | **VT \_ bool**   | Ein boolescher Wert, der angibt, ob diese e-Mail-Nachricht gelesen wurde.                                                                 |
| **\_empfangene WPD-e-Mail \_ \_**   | **VT- \_ Datum**   | Ein Wert, der angibt, wann die e-Mail-Nachricht empfangen wurde.                                                                              |
| **WPD \_ -e-Mail \_ \_**  | **VT \_ LPWSTR** | Die E-Mail-Adresse des Absenders.                                                                                                         |
| **WPD \_ -e-Mail \_ an \_ Zeile**         | **VT \_ LPWSTR** | Die Hauptempfänger der e-Mail-Nachricht.                                                                                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




