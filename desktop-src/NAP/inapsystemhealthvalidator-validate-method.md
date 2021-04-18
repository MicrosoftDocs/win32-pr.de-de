---
title: Inapsystemhealthvalidator Validate-Methode (napsystemhealthvalidator. h)
description: Das NAP-System zum Überprüfen der sohrequest, die von einem Client empfangen wurde.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Validate-Methode für NAP
- Validate-Methode, NAP, inapsystemhealthvalidator-Schnittstelle
- Inapsystemhealthvalidator-Schnittstelle NAP, Validate-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidator.Validate
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7589a67b9a3b1454e3c65b17ad6f584ce0e655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337920"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a>Inapsystemhealthvalidator:: Validate-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthvalidator:: Validate** -Methode wird vom SHV-Entwickler definiert und vom NAP-System aufgerufen, um die [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) zu validieren, die von einem Client empfangen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT Validate(
  [in] INapSystemHealthValidationRequest *request,
  [in] UINT32                            hintTimeOutInMsec,
  [in] INapServerCallback                *callback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anforderung* \[ in\]
</dt> <dd>

Ein com-Zeiger auf ein [**inapsystemhealthvalidationrequest**](inapsystemhealthvalidationrequest.md) -Objekt, das das Validierungs Anforderungs Objekt identifiziert.

</dd> <dt>

*hinttimeoutinmsec* \[ in\]
</dt> <dd>

Die Dauer des Kommunikations Timeout Zeitraums in Millisekunden. Der System Integritäts Prüfungs Punkt (System Health Validator, SHV) sollte innerhalb dieser Zeitspanne Antworten. Andernfalls wird die Antwort gelöscht.

> [!Note]  
> Das Standard Timeout für alle SHVs beträgt 2000 Millisekunden. Wenn Sie einen anderen Wert als den Standardwert verwenden, wird das Timeout für alle registrierten SHVs geändert.

 

</dd> <dt>

*Rückruf* \[ in\]
</dt> <dd>

Ein Zeiger auf das Rückruf Objekt [**inapservercallback**](inapservercallback.md). Dieser Rückruf Zeiger wird von den SHVs verwendet, wenn er aus dem Aufrufen von **inapsystemhealthvalidator:: Validate** **E \_** aussteht. Diese wird für die asynchrone Validierung verwendet. Es wird erwartet, dass die SHVs innerhalb der *hinttimeoutinmsec* -Zeit reagieren, oder andernfalls wird die Antwort gelöscht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein anderer Fehlercode zurückgegeben wird, geht das System davon aus, dass der Server Component-Fehler aufgetreten ist, und die entsprechende Zuordnung erfolgt, um erfolgreich bzw. fehlerhaft zu sein.



| Rückgabecode                                                                                                | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Gibt an, dass das Validierungs Steuerelement für das Objekt "Request" eine sohresponse festgelegt hat.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**E \_ Ausstehend**</dt> </dl>                  | Gibt an, dass OnComplete () in einem separaten Thread aufgerufen wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>**RPC \_ S- \_ Server nicht \_ verfügbar**</dt> </dl> | Gibt an, dass der SHV-Prozess (System Health Validator) beendet wurde, ohne dass der napserver einen Verweis darauf freigibt. Der napserver versucht erneut, einen neuen Verweis auf den SHV zu erstellen und führt den Validate-Rückruf einmal erneut aus. Wenn bei der Erstellung des Objekts oder der erneut ausgeführten Überprüfung ein Fehler auftritt, wird der SHV aus der Liste der geladenen SHVs entfernt. Dieser SHV kann nun nur erneut geladen werden, indem die Registrierung und die erneute Registrierung des SHV erneut aufgehoben werden, oder wenn der napserver neu gestartet wird.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Um die Erkennung von Eindring Versuchen zu unterstützen, werden SHVs aufgefordert, den Client Computer zu validieren, unabhängig davon, ob der Client einen für den SHV vorgesehenen [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) gesendet hat.

Der SHV muss folgende Aktionen ausführen:

-   Rufen Sie den [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) aus der *Anforderung* ab, indem Sie [**Request aufrufen. Getsohrequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).
-   Wenn das [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket NULL ist:
    -   Wenn der SHV ein Angriffs Erkennungssystem ist, füllen Sie ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket mit dem entsprechenden [**NAP-Fehlercode**](nap-error-constants.md) aus, um zu ermitteln, warum der Client Computer schädlich ist.
    -   Alle anderen SHVs sollten ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket mit dem Fehlercode " [**NAP \_ E \_ Missing \_ SoH**](nap-error-constants.md)" auffüllen.
-   Wenn ' *napsystemgenerated* ' vom Anforderungs Aufrufwert ' **true** ' ist [**. Getsohrequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), der SHV sollte ein [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket mit den folgenden 3 TLVS erwarten: [**sohattributetypesystemhealthid**](sohattributetype-enum.md), **sohattributetypefailurecategory**, **sohattributetypeerrorcodes**. Dieser **sohrequest** wird vom NAPAgent im Auftrag des Systemintegritäts-Agents (SHA) generiert, weil beim Abrufen eines Anforderungs Pakets aus dem SHA ein Fehler aufgetreten ist.
-   Überprüfen Sie das [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket.
    -   Wenn die [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) falsch formatiert ist, erstellen Sie ein **sohresponse** -Paket mit dem Fehlercode [**NAP \_ E \_ ungültiges \_ Paket**](nap-error-constants.md).
    -   Wenn der SHV nur zwischengespeicherte Informationen für die Überprüfung des [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Pakets verwendet (d. h. keine e/a-Vorgänge durchgeführt werden), kann er **sohresponse** erstellen, ihn für das Objekt in der *Anforderung* festlegen und **S \_ OK** zurückgeben.
    -   Wenn der SHV e/a-Vorgänge ausführt, um mit den Back-End-Servern zum Überprüfen der Integrität des Clients zu kommunizieren, muss er die E/a in die Warteschlange stellen und diese Funktion mit **E \_ Pending** zurückgeben. In diesem Fall muss der SHV Callback aufrufen [**. OnComplete ()**](inapservercallback-oncomplete-method.md) in einem separaten Thread innerhalb des Timeout Zeitraums *hinttimeoutinmsec*. Andernfalls wird die Antwort des SHV gelöscht.
-   Geben Sie außer den oben aufgeführten Fehlern keinen anderen Fehler zurück. Wenn vom SHV ein anderer Fehlercode zurückgegeben wird (z. b. Systemfehler), wird das Paket verworfen.

Ein SHV muss entweder einen **sohattributetypecomplianceresultcodes** oder **sohattributetypefailurecategory** TLV in seinem [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh)zurückgeben.

-   [**sohattributetypecomplianceresultcodes TLV**](sohattributetype-enum.md): Wenn die Integrität des Clients von SHV überprüft werden konnte (d. h. fehlerfrei oder fehlerhaft), wird dieses TLV zurückgegeben.
-   [**sohattributetypefailurecategory TLV**](sohattributetype-enum.md): Wenn auf dem Client oder Server ein Komponenten-oder Kommunikationsfehler aufgetreten ist, muss dies von diesem TLV angegeben werden. Dieses TLV wird in Abhängigkeit von der Konfiguration des SHV weiterhin fehlerfrei oder fehlerfrei zugeordnet. Weitere Informationen finden Sie unter der [**inapservermanagement**](inapservermanagement.md) -Schnittstelle und der [**failurecategorymapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) -Struktur.

Der SHV darf keine Verweise auf die *Anforderung* oder den *Rückruf* enthalten, wenn der asynchrone-Befehl abgeschlossen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>Napsystemhealthvalidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthvalidator. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapsystemhealthvalidator**](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





