---
description: Tritt auf, wenn Daten aus der Antwort verfügbar sind.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: 'Iwinhttprequestevents:: onresponabdataavailable-Ereignis'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cb2fbc680b1f6739a66bb68565188c8a5d78b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351759"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a>Iwinhttprequestevents:: onresponabdataavailable-Ereignis

Das **onresponondataavailable** -Ereignis tritt auf, wenn Daten aus der Antwort verfügbar sind.

## <a name="syntax"></a>Syntax


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Daten* \[ in\]
</dt> <dd>

Ein NULL basiertes Bytearray, das die von Microsoft Windows HTTP-Diensten (WinHTTP) empfangenen Antwortdaten bis zu dem Punkt empfängt, an dem dieses Ereignis auftritt. Dies ist eine **Variante** vom Typ VT \_ array \| VT \_ UI1.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Da Daten in Bytes vorliegen, müssen Sie in breit Zeichen konvertiert werden, wenn Sie in eine Zeichenfolge mit breit Zeichen (Unicode) eingefügt werden.

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

 

 




