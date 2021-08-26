---
title: INapSystemHealthAgentCallback GetFixupInfo-Methode (NapSystemHealthAgent.h)
description: Wird vom NapAgent aufgerufen, um den Zustand des Systemzustands-Agents zu bestimmen, während er eine SoHResponse verarbeitet.
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- NAP-Methode "GetFixupInfo"
- GetFixupInfo-Methode NAP, INapSystemHealthAgentCallback-Schnittstelle
- INapSystemHealthAgentCallback-Schnittstelle NAP , GetFixupInfo-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetFixupInfo
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d82f84acbc759f8459c7eeb904ab4f08a108093fa30c3b27c033fbfef1dcf15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037750"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a>INapSystemHealthAgentCallback::GetFixupInfo-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthAgentCallback::GetFixupInfo-Methode** wird vom NapAgent aufgerufen, um den Zustand des Systemzustands-Agents zu bestimmen, während er eine [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)verarbeitet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Info zu* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**FixupInfo-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) die den Fixupstatus des Agents enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                          | Beschreibung                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Gibt die erfolgreiche Ausführung an.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Rückrufmethode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.

Der Systemzustands-Agent muss **S \_ OK** sofort ohne Blockierung zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





