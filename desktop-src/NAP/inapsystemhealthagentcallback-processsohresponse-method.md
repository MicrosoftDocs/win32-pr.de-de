---
title: Inapsystemhealthagentcallback processsohresponse-Methode (napsystemhealthagent. h)
description: Wird aufgerufen, wenn der NAPAgent eine sohresponse empfängt, die für diesen Integritäts-Agent bestimmt ist.
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- Processsohresponse-Methode NAP
- Processsohresponse-Methode NAP, inapsystemhealthagentcallback-Schnittstelle
- Inapsystemhealthagentcallback-Schnittstelle NAP, processsohresponse-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.ProcessSoHResponse
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c62c585c36680dde2c54c95c255a85f69fc5ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956608"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a>Inapsystemhealthagentcallback::P rocesssohresponse-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentcallback::P rocesssohresponse** -Methode wird aufgerufen, wenn der NAPAgent eine [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) empfängt, die für diesen Integritäts-Agent bestimmt ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anforderung* \[ in\]
</dt> <dd>

Ein com-Zeiger auf ein [**inapsystemhealthagentrequest**](inapsystemhealthagentrequest.md) -Objekt, das das Anforderungs Objekt identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Gibt die erfolgreiche Ausführung an.<br/>                                                            |
| <dl> <dt>**\_ \_ Ungültiges NAP- \_ Paket**</dt> </dl> | Wird von dieser Implementierung zurückgegeben, wenn die Antwort nicht das richtige Format hat.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Rückruf Methode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.

Wenn der NAPAgent eine [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) empfängt, die für diesen Integritäts-Agent bestimmt ist, ruft er diese Methode auf. Der Integritäts-Agent muss die sohresponse vom Anforderungs Objekt Abfragen. Er darf keine Verweise auf das Anforderungs Objekt enthalten, nachdem dieser-Vorgang abgeschlossen wurde.

Die **inapsystemhealthagentcallback::P rocesssohresponse** -Methode darf nicht blockiert werden. Wenn eine Korrektur Verarbeitung erforderlich ist, muss jede Implementierung von **processsohresponse** einen neuen Thread starten, um die Verarbeitungs Verarbeitung auszuführen. Der NAPAgent muss [**inapsystemhealthagentcallback:: getfixupinfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) aufrufen, um den Korrektur Status des SHA zu ermitteln.

Diese Methode muss ein **\_ \_ Ungültiges NAP \_ E-Paket** zurückgeben, wenn die Antwort nicht das richtige Format hat.

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

 

 





