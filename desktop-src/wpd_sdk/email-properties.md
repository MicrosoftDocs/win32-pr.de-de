---
description: Windows Portable Geräte unterstützen die folgenden E-Mail-Eigenschaften.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: E-Mail-Eigenschaften (PortableDevice.h)
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
ms.openlocfilehash: 4c67a341bcc7fcac041f02cc183c02e024e60b121150aba0ce62da2f973ccbec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843232"
---
# <a name="email-properties"></a>E-Mail-Eigenschaften

Windows Portable Geräte unterstützen die folgenden E-Mail-Eigenschaften.



| Eigenschaft                         | VarType        | Beschreibung                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ EMAIL \_ BCC \_ LINE**        | **VT \_ LPWSTR** | Die BCC-Empfänger der E-Mail. BCC-Empfänger erhalten eine Kopie der E-Mail, aber ihre Namen werden nicht als Empfänger angezeigt.   |
| **WPD \_ EMAIL \_ CC \_ LINE**         | **VT \_ LPWSTR** | Die CC-Empfänger der E-Mail. CC-Empfänger erhalten eine Kopie der E-Mail-Nachricht, und ihre Namen werden als Empfänger angezeigt. |
| **WPD \_ EMAIL \_ HAS \_ ATTACHMENTS (WPD-E-MAIL ENTHÄLT ANLAGEN)** | **VT \_ BOOL**   | Ein boolescher Wert, der angibt, ob diese E-Mail-Nachricht Anlagen enthält.                                                               |
| **\_ \_ WPD-E-MAIL \_ WURDE \_ GELESEN**  | **VT \_ BOOL**   | Ein boolescher Wert, der angibt, ob diese E-Mail-Nachricht gelesen wurde.                                                                 |
| **\_WPD-E-MAIL-EMPFANGENE \_ \_ ZEIT**   | **VT \_ DATE**   | Ein -Wert, der angibt, wann die E-Mail empfangen wurde.                                                                              |
| **\_WPD-E-MAIL-ABSENDERADRESSE \_ \_**  | **VT \_ LPWSTR** | Die E-Mail-Adresse des Absenders.                                                                                                         |
| **\_WPD-E-MAIL \_ AN \_ ZEILE**         | **VT \_ LPWSTR** | Die Hauptempfänger der E-Mail-Nachricht.                                                                                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




