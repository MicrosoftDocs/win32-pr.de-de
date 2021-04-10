---
description: Tritt auf, wenn in der Anwendung ein Laufzeitfehler auftritt.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: 'Iwinhttprequestevents:: OnError-Ereignis'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8582deec90eb6bfc2985460f3127d5c7ee9c01b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960691"
---
# <a name="iwinhttprequesteventsonerror-event"></a>Iwinhttprequestevents:: OnError-Ereignis

Das **OnError** -Ereignis tritt auf, wenn ein Laufzeitfehler in der Anwendung vorliegt.

## <a name="syntax"></a>Syntax


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Errornumber* \[ in\]
</dt> <dd>

Empfängt den numerischen Wert des Fehlers. Die unteren 16 Bits dieser Fehlernummer entsprechen einem der in [**Fehlermeldungen**](error-messages.md)aufgeführten Fehler.

</dd> <dt>

*ErrorDescription* \[ in\]
</dt> <dd>

Gibt eine kurze Beschreibung des aufgetretenen Fehlers an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

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

 

 




