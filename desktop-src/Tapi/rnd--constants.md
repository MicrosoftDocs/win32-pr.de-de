---
description: Die folgenden Konstanten können als Fehler zurückgegeben werden.
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: RND_ Konstanten (Rnderr.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ed1b55b0ed18215fb17e27504c309c67b0cea3351acea6cffadc4b3ff31c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773370"
---
# <a name="rnd_-constants"></a>\_RND-Konstanten

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die folgenden Konstanten können als Fehler zurückgegeben werden.

<dl> <dt>

<span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**RND \_ UNGÜLTIGE \_ ZEIT**
</dt> <dd> <dl> <dt>

 0xe0000200
</dt> <dt>



Der eingegebene Zeitwert ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**RND \_ NULL \_ SERVER \_ NAME**
</dt> <dd> <dl> <dt>

 0xe0000201
</dt> <dt>



Der Servername ist **NULL,** wahrscheinlich weil [**ITConferenceBlob::Init**](itconferenceblob-init.md) nicht ausgeführt wurde oder nicht erfolgreich war.


</dt> </dl> </dd> <dt>

<span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND \_ BEREITS \_ VERBUNDEN**
</dt> <dd> <dl> <dt>

 0xe0000202
</dt> <dt>



Die [**ITDirectory::Verbinden-Methode**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) wurde aufgerufen, aber es ist bereits eine Verbindung vorhanden.


</dt> </dl> </dd> <dt>

<span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND \_ NICHT \_ VERBUNDEN**
</dt> <dd> <dl> <dt>

 0xe0000203
</dt> <dt>



Die [**ITDirectory::Verbinden-Methode**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) wurde nicht aufgerufen oder ist fehlgeschlagen.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                               |
| Header<br/>       | <dl> <dt>Rnderr.h</dt> </dl> |



 

 




