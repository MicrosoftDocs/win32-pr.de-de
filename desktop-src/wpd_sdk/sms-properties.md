---
description: Windows Portable Devices unterstützt die folgenden SMS-Eigenschaften.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: SMS-Eigenschaften (PortableDevice.h)
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
ms.openlocfilehash: 12b68a962fc79dd75d6ff90635be5dbe99f36c3170f06cd7d79af2eb23317e98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193581"
---
# <a name="sms-properties"></a>SMS-Eigenschaften

Windows Portable Devices unterstützt die folgenden SMS-Eigenschaften.



| Eigenschaft                   | VarType        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ WPD-SMS-CODIERUNG**     | **VT \_ LPWSTR** | Ein -Wert, der angibt, wie der Treiber die vom Client gesendete Textnachricht codiert. Dies ist eine schreibgeschützte Eigenschaft. Der Client kann nicht angeben, welchen Codierungstyp ein Gerät zum Senden von Nachrichten verwendet. Diese Werte duplizieren die enumerationierten [**WPD \_ SMS ENCODING \_ \_ TYPES-Werte.**](wpd-sms-encoding-types.md) |
| **WPD \_ SMS \_ MAX \_ PAYLOAD** | **VT \_ UI4**    | Die maximale Anzahl von Bytes, die in einer Nachricht enthalten sein können.                                                                                                                                                                                                                                             |
| **WPD \_ SMS \_ PROVIDER**     | **VT \_ LPWSTR** | Der Name des Dienstanbieters.                                                                                                                                                                                                                                                                                |
| **WPD \_ SMS \_ TIMEOUT**      | **VT \_ UI4**    | Die Anzahl von Millisekunden, bis ein Timeout zurückgegeben wird.                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




