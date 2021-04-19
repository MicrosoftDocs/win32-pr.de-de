---
description: Die folgenden Konstanten können als Fehler zurückgegeben werden.
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: RND_ Konstanten (rnderr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a89b6747fb9fef775bbf40fac472081567ff1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356447"
---
# <a name="rnd_-constants"></a>Rnd- \_ Konstanten

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die folgenden Konstanten können als Fehler zurückgegeben werden.

<dl> <dt>

<span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**Rnd \_ ungültige \_ Zeit**
</dt> <dd> <dl> <dt>

 0xe0000200
</dt> <dt>



Der eingegebene Zeitwert ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**Rnd- \_ NULL- \_ Server \_ Name**
</dt> <dd> <dl> <dt>

 0xe0000201
</dt> <dt>



Der Servername ist **null**, wahrscheinlich weil [**itconferenceblob:: init**](itconferenceblob-init.md) nicht ausgeführt wurde oder nicht erfolgreich ausgeführt wurde.


</dt> </dl> </dd> <dt>

<span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**Rnd ist \_ bereits \_ verbunden.**
</dt> <dd> <dl> <dt>

 0xe0000202
</dt> <dt>



Die [**itdirectory:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) -Methode wurde aufgerufen, aber es ist bereits eine Verbindung vorhanden.


</dt> </dl> </dd> <dt>

<span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**Rnd ist \_ nicht \_ verbunden.**
</dt> <dd> <dl> <dt>

 0xe0000203
</dt> <dt>



Die [**itdirectory:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) -Methode wurde nicht aufgerufen oder ist fehlgeschlagen.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                               |
| Header<br/>       | <dl> <dt>Rnderr. h</dt> </dl> |



 

 




