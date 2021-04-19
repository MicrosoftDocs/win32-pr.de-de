---
description: Tritt auf, wenn die Antwortdaten fertig sind.
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: 'Iwinhttprequestevents:: onresponabbeendete-Ereignis'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d3a596e23028cec0401a21a1ee866ef6e51d9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353570"
---
# <a name="iwinhttprequesteventsonresponsefinished-event"></a>Iwinhttprequestevents:: onresponabbeendete-Ereignis

Das **onresponabcomplete** -Ereignis tritt auf, wenn die Antwortdaten vollständig sind.

## <a name="syntax"></a>Syntax


```C++
void OnResponseFinished();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis signalisiert, dass alle Antwortdaten, die sich auf die letzte Anforderung beziehen, empfangen wurden. " [**Onresponondataavailable**](iwinhttprequestevents-onresponsedataavailable.md) " tritt bis zur nächsten Anforderung nicht wieder auf.

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

 

 




