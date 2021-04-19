---
description: Der \_ \_ Enumerationstyp SMS-Nachrichten Typen beschreibt den Inhaltstyp einer SMS (Short Message Service)-Nachricht.
ms.assetid: 882886a6-ecce-443f-a7e9-2e4e367ad804
title: SMS_MESSAGE_TYPES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS_MESSAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a2e1ccfd074ff1f5287af22c5a8ebb3c6b3c661d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369631"
---
# <a name="sms_message_types-enumeration"></a>SMS- \_ Nachrichten \_ Typen-Enumeration

Der Enumerationstyp **SMS- \_ Nachrichten \_ Typen** beschreibt den Inhaltstyp einer SMS (Short Message Service)-Nachricht.

## <a name="syntax"></a>Syntax


```C++
typedef enum SMS_MESSAGE_TYPES { 
  SMS_TEXT_MESSAGE    = 0,
  SMS_BINARY_MESSAGE  = 1
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS- \_ Text \_ Nachricht**
</dt> <dd>

Eine Textnachricht.

</dd> <dt>

<span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**binäre SMS- \_ \_ Nachricht**
</dt> <dd>

Eine binäre Nachricht.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird vom Befehl [**\_ \_ SMS \_ Senden des WPD-Befehls**](wpd-command-sms-send-command.md)verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




