---
description: Die SetExternalT120Address-Methode wird von einer Anwendung aufgerufen, um eine externe T. 120-Adresse für den Datenaustausch zu konfigurieren.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: 'IH323LineEx:: SetExternalT120Address-Methode (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09756aaf77ba36497b3059f7e93829d7d6a57b42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357593"
---
# <a name="ih323lineexsetexternalt120address-method"></a>IH323LineEx:: SetExternalT120Address-Methode

\[**SetExternalT120Address** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **SetExternalT120Address** -Methode wird von einer Anwendung aufgerufen, um eine externe T. 120-Adresse für den Datenaustausch zu konfigurieren. Die Funktion "t. 120" wird während der H. 245-Aushandlung angekündigt, und die Adresse wird in der Bestätigung des Open Logic-Kanals verwendet, sodass der andere Endpunkt T. 120-Sitzungen einrichten kann, in denen der Dienst diese Adresse überwacht. Wenn diese Funktion nicht aufgerufen wird, kündigt der Dienstanbieter H. 323 keine T. 120-Funktion an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetExternalT120Address(
  [in] BOOL  fEnable,
  [in] DWORD dwIP,
  [in] WORD  wPort
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fenckbar* \[ in\]
</dt> <dd>

**True** , um T. 120-Funktion zu aktivieren; **False** , um die T. 120-Funktion zu deaktivieren.

</dd> <dt>

*dwip* \[ in\]
</dt> <dd>

**DWORD** mit der IP-Adresse in der Host-Byte Reihenfolge des externen T. 120-Diensts.

</dd> <dt>

*wport* \[ in\]
</dt> <dd>

**Word** , das den Port des externen T. 120-dienstangs enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                          | Beschreibung                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Methode war erfolgreich.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




