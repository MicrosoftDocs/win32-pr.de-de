---
title: Inapsystemhealthagentcallback getsohrequest-Methode (napsystemhealthagent. h)
description: Wird von NAPAgent aufgerufen, um die SoH-Anforderung des Systemintegritäts-Agents abzufragen.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- Getsohrequest-Methode NAP
- Getsohrequest-Methode NAP, inapsystemhealthagentcallback-Schnittstelle
- Inapsystemhealthagentcallback-Schnittstelle NAP, getsohrequest-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fd95ce79587b5e7e259323286cfce138dd2df2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392001"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a>Inapsystemhealthagentcallback:: getsohrequest-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentcallback:: getsohrequest** -Methode wird von NAPAgent aufgerufen, um die SoH-Anforderung des Systemintegritäts-Agents abzufragen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoHRequest(
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



| Rückgabecode                                                                                                                      | Beschreibung                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                             | Gibt die erfolgreiche Ausführung an.<br/>                                                                                                                      |
| <dl> <dt>**HRESULT \_ von \_ Win32 (RPC \_ S- \_ Server nicht \_ verfügbar)**</dt> </dl> | Wenn dieser Code von ihrer Implementierung zurückgegeben wird, entfernt der NAPAgent den SHA-Eintrag aus der gebundenen SHA-Liste und leert seinen Cache Eintrag.<br/> |



 

Wenn ein beliebiger Rückgabewert (mit Ausnahme **von HRESULT \_ von \_ Win32 (RPC \_ S-Server nicht \_ \_ verfügbar)**) von ihrer Implementierung zurückgegeben wird, erstellt das NAP-System eine [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) und gibt Sie mit den folgenden Attributtypen und Werten an den entsprechenden SHV zurück:

-   [**sohattributetypesystemhealthid**](sohattributetype-enum.md)= <id>
-   [**sohattributetypefailurecategory**](sohattributetype-enum.md) =  [ **failurecategoryclientcomponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohattributetypeerrorcodes**](sohattributetype-enum.md) = <Fehlercode>

## <a name="remarks"></a>Bemerkungen

Diese Rückruf Methode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.

Diese Methode muss die Anforderung verarbeiten und sofort zurückgeben. Das Verzögern der Rückgabe dieser Methode wirkt sich negativ auf die Systemleistung und die Reaktionsfähigkeit aus und kann dazu führen, dass für andere Teile des Betriebssystems ein Timeout auftritt.

Die Überwachung des Integritäts Zustands sollte nicht als Teil dieses Aufrufes erfolgen, insbesondere wenn es sich um eine rechenintensive Berechnung handelt und einige Zeit in Anspruch nimmt. Die Integritäts Zustandsüberwachung und die SoH-Berechnung sollten in einem separaten Thread oder Dienst durchgeführt werden. Die einzige Funktion dieser Methode sollte sein, das SoH von SHA festzulegen und zurückzugeben.

Wenn es lange dauern wird, bis das SHA ein SoH generiert, sollte das zwischengespeicherte SoH an den NAPAgent zurückgegeben werden. Wenn kein zwischengespeichertes SoH vorhanden ist, sollte das SHA sofort ein SoH mit den folgenden Attributtypen und Werten zurückgeben:

-   [**sohattributetypesystemhealthid**](sohattributetype-enum.md)= <id>
-   [**sohattributetypefailurecategory**](sohattributetype-enum.md) =  [ **failurecategoryclientcommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohattributetypeerrorcodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ kein \_ zwischengespeichertes \_ SoH**](nap-error-constants.md)

Wenn das SoH generiert wurde, muss das SHA [**inapsystemhealthagentbinding:: notifysohchange**](inapsystemhealthagentbinding-notifysohchange-method.md) aufgerufen werden, um den NAPAgent über die System Integritäts Änderung zu benachrichtigen.

Der NAPAgent ruft diese Methode auf, um den sohrequest des Systemintegritäts-Agents abzufragen. Der SHA kann das bestandene [**inapsystemhealthagentrequest**](inapsystemhealthagentrequest.md) -Objekt nach Parametern Abfragen, die es benötigt, um den sohrequest zu berechnen. Der SHA muss die berechnete sohrequest für das Anforderungs Objekt festlegen. Der SHA darf keine Verweise auf das Anforderungs Objekt enthalten, nachdem dieser-Vorgang abgeschlossen wurde.

Wenn diese Methode aufgerufen wird und ein SoH im Cache von NAPAgent vorhanden ist, wird Sie für das Anforderungs Objekt festgelegt. Der SHA kann ihn mithilfe von **getsohrequest** Abfragen. Wenn das SHA kein neues SoH festgelegt, wird das zwischengespeicherte verwendet.

Für ungebundene SHAs, die beim System registriert sind, erstellt das NAP-System eine sohrequest und sendet Sie an den entsprechenden SHV mit den folgenden Attributtypen und Werten:

-   [**sohattributetypesystemhealthid**](sohattributetype-enum.md)= <id>
-   [**sohattributetypefailurecategory**](sohattributetype-enum.md) =  [ **failurecategoryclientcomponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohattributetypeerrorcodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ nicht \_ Initialisiert**](nap-error-constants.md)

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

 

 





