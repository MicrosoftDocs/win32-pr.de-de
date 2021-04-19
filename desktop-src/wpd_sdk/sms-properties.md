---
description: Tragbare Windows-Geräte unterstützen die folgenden SMS-Eigenschaften.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: SMS-Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c43917c8c26027713b4e5076e8eb3789b95f08e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359302"
---
# <a name="sms-properties"></a>SMS-Eigenschaften

Tragbare Windows-Geräte unterstützen die folgenden SMS-Eigenschaften.



| Eigenschaft                   | VarType        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD- \_ SMS- \_ Codierung**     | **VT \_ LPWSTR** | Ein Wert, der angibt, wie der Treiber die vom Client gesendete Textnachricht codieren soll. Dies ist eine schreibgeschützte Eigenschaft. der Client kann nicht angeben, welchen Codierungstyp ein Gerät zum Senden von Nachrichten verwendet. Diese Werte duplizieren die Enumerationswerte der [**WPD- \_ SMS- \_ Codierungen \_**](wpd-sms-encoding-types.md) . |
| **\_ \_ Maximale Nutzlast für WPD SMS \_** | **VT \_ UI4**    | Die maximale Anzahl von Bytes, die in einer Nachricht enthalten sein können.                                                                                                                                                                                                                                             |
| **WPD- \_ SMS- \_ Anbieter**     | **VT \_ LPWSTR** | Der Name des Dienstanbieters.                                                                                                                                                                                                                                                                                |
| **WPD- \_ SMS- \_ Timeout**      | **VT \_ UI4**    | Die Anzahl von Millisekunden, bis ein Timeout zurückgegeben wird.                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




