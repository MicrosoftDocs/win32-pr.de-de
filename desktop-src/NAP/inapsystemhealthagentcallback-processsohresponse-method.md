---
title: INapSystemHealthAgentCallback ProcessSoHResponse-Methode (NapSystemHealthAgent.h)
description: Wird aufgerufen, wenn der NapAgent eine SoHResponse empfängt, die für diesen Integritäts-Agent bestimmt ist.
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- ProcessSoHResponse-Methode NAP
- ProcessSoHResponse-Methode NAP, INapSystemHealthAgentCallback-Schnittstelle
- INapSystemHealthAgentCallback-Schnittstelle NAP, ProcessSoHResponse-Methode
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
ms.openlocfilehash: 1f5aaca7833560dbb53422da08ced158bb172610c3bacef931866d74d416fcce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367755"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a>INapSystemHealthAgentCallback::P rocessSoHResponse-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapSystemHealthAgentCallback::P rocessSoHResponse-Methode** wird aufgerufen, wenn der NapAgent eine Für diesen Integritäts-Agent bestimmte [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) empfängt.

## <a name="syntax"></a>Syntax


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anforderung* \[ In\]
</dt> <dd>

Ein COM-Zeiger auf ein [**INapSystemHealthAgentRequest-Objekt,**](inapsystemhealthagentrequest.md) das das Anforderungsobjekt identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                            | Beschreibung                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Gibt die erfolgreiche Ausführung an.<br/>                                                            |
| <dl> <dt>**NAP \_ E \_ UNGÜLTIGES \_ PAKET**</dt> </dl> | Wird von dieser Implementierung zurückgegeben, wenn die Antwort nicht im richtigen Format vor liegt.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Rückrufmethode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.

Wenn der NapAgent eine [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) empfängt, die für diesen Integritäts-Agent bestimmt ist, ruft er diese Methode auf. Der Integritäts-Agent muss die SoHResponse aus dem Anforderungsobjekt abfragen. Sie darf keine Verweise auf das Anforderungsobjekt enthält, nachdem dieser Aufruf abgeschlossen wurde.

Die **INapSystemHealthAgentCallback::P rocessSoHResponse-Methode** darf nicht blockiert werden. Wenn eine Korrekturverarbeitung erforderlich ist, muss jede Implementierung von **ProcessSoHResponse** einen neuen Thread starten, um die Korrekturverarbeitung durchzuführen. Der NapAgent muss [**INapSystemHealthAgentCallBack::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) aufrufen, um den Fixupstatus des SHA zu ermitteln.

Diese Methode muss **NAP E INVALID PACKET \_ \_ \_ zurückgeben,** wenn die Antwort nicht im richtigen Format vor liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





