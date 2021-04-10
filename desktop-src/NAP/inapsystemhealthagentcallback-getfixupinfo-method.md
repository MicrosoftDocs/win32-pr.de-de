---
title: Inapsystemhealthagentcallback getfixupinfo-Methode (napsystemhealthagent. h)
description: Wird von NAPAgent aufgerufen, um den Zustand des Systemintegritäts-Agents zu ermitteln, während er eine sohresponse verarbeitet.
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- Getfixupinfo-Methode NAP
- Getfixupinfo-Methode NAP, inapsystemhealthagentcallback-Schnittstelle
- Inapsystemhealthagentcallback-Schnittstelle NAP, getfixupinfo-Methode
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
ms.openlocfilehash: 1227cbe870c722189c995bff0c967eb187548cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104139"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a>Inapsystemhealthagentcallback:: getfixupinfo-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentcallback:: getfixupinfo** -Methode wird vom NAPAgent aufgerufen, um den Status des Systemintegritäts-Agents zu ermitteln, während er eine [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh)verarbeitet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Info* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**fixupinfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) -Struktur, die den Korrektur Status des Agents enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                          | Beschreibung                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Gibt die erfolgreiche Ausführung an.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Rückruf Methode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.

Der Systemintegritäts-Agent muss " **S \_ OK** " sofort ohne Blockierung zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napsystemhealthagent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthagent. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapsystemhealthagentcallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





