---
description: Die SetExternalT120Address-Methode wird von einer Anwendung aufgerufen, um eine externe T.120-Adresse für den Datenaustausch zu konfigurieren.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: IH323LineEx::SetExternalT120Address-Methode (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8889887c396c427c28ac2906206b3e3cbbcb102daa937720b6b879472b47bbdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992090"
---
# <a name="ih323lineexsetexternalt120address-method"></a>IH323LineEx::SetExternalT120Address-Methode

\[**SetExternalT120Address** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **SetExternalT120Address-Methode** wird von einer Anwendung aufgerufen, um eine externe T.120-Adresse für den Datenaustausch zu konfigurieren. Die T.120-Funktion wird während der H.245-Aushandlung angekündigt, und die Adresse wird in der Bestätigung des geöffneten Logikkanals verwendet, damit der andere Endpunkt T.120-Sitzungen einrichten kann, bei denen der Dienst an dieser Adresse lausbt. Wenn diese Funktion nicht aufgerufen wird, gibt der H.323-Dienstanbieter die T.120-Funktion nicht an.

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

*fEnable* \[ In\]
</dt> <dd>

**TRUE,** um die T.120-Funktion zu aktivieren; **FALSE,** um die T.120-Funktion zu deaktivieren.

</dd> <dt>

*dwIP* \[ In\]
</dt> <dd>

**DWORD** mit der IP-Adresse in der Host-Byte-Reihenfolge des externen T.120-Diensts.

</dd> <dt>

*wPort* \[ In\]
</dt> <dd>

**WORD,** das den Port des externen T.120-Diensts enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                          | Beschreibung                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Methode war erfolgreich.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




