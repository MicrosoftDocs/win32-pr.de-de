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
# <a name="sms_message_types-enumeration"></a><span data-ttu-id="4d82d-103">SMS- \_ Nachrichten \_ Typen-Enumeration</span><span class="sxs-lookup"><span data-stu-id="4d82d-103">SMS\_MESSAGE\_TYPES enumeration</span></span>

<span data-ttu-id="4d82d-104">Der Enumerationstyp **SMS- \_ Nachrichten \_ Typen** beschreibt den Inhaltstyp einer SMS (Short Message Service)-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4d82d-104">The **SMS\_MESSAGE\_TYPES** enumeration type describes the content type of a short message service (SMS) message.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d82d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d82d-105">Syntax</span></span>


```C++
typedef enum SMS_MESSAGE_TYPES { 
  SMS_TEXT_MESSAGE    = 0,
  SMS_BINARY_MESSAGE  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="4d82d-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="4d82d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4d82d-107"><span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS- \_ Text \_ Nachricht**</span><span class="sxs-lookup"><span data-stu-id="4d82d-107"><span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS\_TEXT\_MESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="4d82d-108">Eine Textnachricht.</span><span class="sxs-lookup"><span data-stu-id="4d82d-108">A text message.</span></span>

</dd> <dt>

<span data-ttu-id="4d82d-109"><span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**binäre SMS- \_ \_ Nachricht**</span><span class="sxs-lookup"><span data-stu-id="4d82d-109"><span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**SMS\_BINARY\_MESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="4d82d-110">Eine binäre Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4d82d-110">A binary message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d82d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d82d-111">Remarks</span></span>

<span data-ttu-id="4d82d-112">Diese Enumeration wird vom Befehl [**\_ \_ SMS \_ Senden des WPD-Befehls**](wpd-command-sms-send-command.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="4d82d-112">This enumeration is used by the [**WPD\_COMMAND\_SMS\_SEND Command**](wpd-command-sms-send-command.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d82d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d82d-113">Requirements</span></span>



| <span data-ttu-id="4d82d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d82d-114">Requirement</span></span> | <span data-ttu-id="4d82d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4d82d-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d82d-116">Header</span><span class="sxs-lookup"><span data-stu-id="4d82d-116">Header</span></span><br/> | <dl> <span data-ttu-id="4d82d-117"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d82d-117"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d82d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d82d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d82d-119">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="4d82d-119">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




