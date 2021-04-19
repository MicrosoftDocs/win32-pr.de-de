---
description: Tritt auf, wenn die Antwortdaten empfangen werden.
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: 'Iwinhttprequestevents:: onresponserstart-Ereignis'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a299c535dd854bff07f2c24989096f7b9e49fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360643"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a>Iwinhttprequestevents:: onresponserstart-Ereignis

Das **onresponanstart** -Ereignis tritt auf, wenn die Antwortdaten empfangen werden.

## <a name="syntax"></a>Syntax


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Status* \[ in\]
</dt> <dd>

Empfängt den Standardstatus Code, der mit den Antwortdaten zurückgegeben wird. Status Codes werden in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)definiert.

</dd> <dt>

*ContentType* \[ in\]
</dt> <dd>

Gibt den Typ des empfangenen Inhalts an, z. b. "Text/HTML" oder "image/gif".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Damit dieses Ereignis auftritt, verwenden Sie [**Open**](iwinhttprequest-open.md) , um eine HTTP-Verbindung im asynchronen Modus zu senden, und senden Sie mit [**Send**](iwinhttprequest-send.md) eine Daten Anforderung an einen Internet Server.

Dies ist das erste WinHTTP-Ereignis, das nach dem [**senden**](iwinhttprequest-send.md)auftritt.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwinhttprequestevents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




