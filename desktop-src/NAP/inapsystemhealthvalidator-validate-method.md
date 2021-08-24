---
title: INapSystemHealthValidator Validate-Methode (NapSystemHealthValidator.h)
description: Das NAP-System zum Überprüfen der soHRequest, die von einem Client empfangen wurde.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Überprüfen der NAP-Methode
- Überprüfen der NAP-Methode, INapSystemHealthValidator-Schnittstelle
- INapSystemHealthValidator-Schnittstelle NAP , Validate-Methode
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
ms.openlocfilehash: f1c200e96024075d0c2880b294c197938a5ec0a6f3e1da4cb019d5ecd3ed32b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802770"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a>INapSystemHealthValidator::Validate-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthValidator::Validate-Methode** wird vom SHV-Entwickler definiert und vom NAP-System aufgerufen, um die von einem Client empfangene [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) zu überprüfen.

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

*Anforderung* \[ In\]
</dt> <dd>

Ein COM-Zeiger auf ein [**INapSystemHealthValidationRequest-Objekt,**](inapsystemhealthvalidationrequest.md) das das Validierungsanforderungsobjekt identifiziert.

</dd> <dt>

*hintTimeOutInMsec* \[ In\]
</dt> <dd>

Die Dauer des Kommunikationstimeoutzeitraums in Millisekunden. Das System health Validator (SHV) sollte innerhalb dieser Zeitspanne reagieren. andernfalls wird die Antwort gelöscht.

> [!Note]  
> Das Standardtimeout für alle SHVs beträgt 2000 Millisekunden. Wenn Sie einen anderen Wert als den Standardwert verwenden, ändert sich das Timeout für alle registrierten SHVs.

 

</dd> <dt>

*Rückruf* \[ In\]
</dt> <dd>

Ein Zeiger auf das Rückrufobjekt [**INapServerCallback**](inapservercallback.md). Dieser Rückrufzeiger wird von den SHVs verwendet, wenn sie **E \_ PENDING** aus dem Aufruf von **INapSystemHealthValidator::Validate** zurückgeben. Dies wird für die asynchrone Validierung verwendet. Es wird erwartet, dass die SHVs innerhalb der *HintTimeOutInMsec-Zeit* reagieren, andernfalls wird die Antwort gelöscht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein anderer Fehlercode zurückgegeben wird, geht das System davon aus, dass ein serverComponent-Fehler aufgetreten ist, und die entsprechende Zuordnung erfolgt, um den Fehler zu übergeben bzw. zu fehlschlagen.



| Rückgabecode                                                                                                | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Gibt an, dass das Validierungszeichen eine SoHResponse für das Request-Objekt festgelegt hat.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**E \_ AUSSTEHEND**</dt> </dl>                  | Gibt an, dass OnComplete() in einem separaten Thread aufgerufen wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>**\_ \_ RPC-S-SERVER \_ NICHT VERFÜGBAR**</dt> </dl> | Gibt an, dass der SHV-Prozess (System Health Validator) beendet wurde, ohne dass der NapServer tatsächlich einen Verweis darauf freigibt. Der NapServer versucht, einen neuen Verweis auf die SHV neu zu erstellen, und führt den Validate-Aufruf einmal erneut durch. Wenn bei der Erstellung des Objekts oder der erneut ausgeführten Validate-Anweisung ein Fehler auftritt, wird die SHV aus der Liste der geladenen SHVs entfernt. Diese SHV kann jetzt nur erneut geladen werden, indem Sie die Registrierung aufheben und die SHV erneut registrieren oder wenn der NapServer neu gestartet wird.<br/> |



 

## <a name="remarks"></a>Hinweise

Zur Unterstützung der Angriffserkennung werden SHVs aufgefordert, den Clientcomputer unabhängig davon zu überprüfen, ob der Client eine [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) für die SHV gesendet hat.

Die SHV muss folgende Schritte ausführen:

-   Rufen Sie [**die SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) von *der Anforderung* ab, indem Sie die [**Anforderung aufrufen. GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).
-   Wenn das [**SoHRequest-Paket**](/windows/win32/api/naptypes/ns-naptypes-soh) NULL ist:
    -   Wenn die SHV ein Angriffserkennungssystem ist, füllen Sie ein [**SoHRequest-Paket**](/windows/win32/api/naptypes/ns-naptypes-soh) mit dem entsprechenden [**NAP-Fehlercode**](nap-error-constants.md) auf, um zu verstehen, warum der Clientcomputer schädlich ist.
    -   Alle anderen SHVs sollten ein [**SoHRequest-Paket**](/windows/win32/api/naptypes/ns-naptypes-soh) mit dem Fehlercode [**NAP E MISSING \_ \_ \_ SOH**](nap-error-constants.md)auffüllen.
-   Wenn *napSystemGenerated* **vom** Aufruf der Anforderung true [**ist. GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), sollte die SHV ein [**SoH-Paket**](/windows/win32/api/naptypes/ns-naptypes-soh) mit den folgenden drei TLVs erwarten: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**. Diese **SoHRequest** wird vom NapAgent im Auftrag des System Health Agent (SHA) generiert, da beim Abrufen eines Anforderungspakets aus dem SHA ein Fehler aufgetreten ist.
-   Überprüfen Sie das [**SoHRequest-Paket.**](/windows/win32/api/naptypes/ns-naptypes-soh)
    -   Wenn [**die SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) falsch formatiert ist, erstellen Sie ein **SoHResponse-Paket** mit dem Fehlercode [**NAP E INVALID \_ \_ \_ PACKET**](nap-error-constants.md).
    -   Wenn der SHV nur zwischengespeicherte Informationen verwendet, um das [**SoHRequest-Paket**](/windows/win32/api/naptypes/ns-naptypes-soh) zu überprüfen (d.h. es wird keine E/A ausgeführt), kann er **das SoHResponse-Objekt** erstellen, es für das Objekt in *der Anforderung* festlegen und **S \_ OK** zurückgeben.
    -   Wenn der SHV E/A ausführt, um mit seinen Back-End-Servern zu kommunizieren, um die Integrität des Clients zu überprüfen, muss er die E/A in die Warteschlange stellen und diese Funktion mit **E \_ PENDING** zurückgeben. In diesem Fall muss die SHV [**einen Rückruf aufrufen. OnComplete()**](inapservercallback-oncomplete-method.md) für einen separaten Thread innerhalb des Timeoutzeitraums, *hintTimeOutInMsec.* Andernfalls wird die Antwort der SHV gelöscht.
-   Geben Sie keinen anderen Fehler als die oben aufgeführten zurück. Wenn ein anderer Fehlercode von der SHV zurückgegeben wird (z. B. systemfehler), wird das Paket verworfen.

Eine SHV muss entweder **sohAttributeTypeComplianceResultCodes** oder **sohAttributeTypeFailureCategory** TLV in ihrer [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)zurückgeben.

-   [**sohAttributeTypeComplianceResultCodes TLV:**](sohattributetype-enum.md)Wenn die SHV die Integrität des Clients überprüfen konnte (d. h. fehlerfrei oder fehlerhaft), wird diese TLV zurückgegeben.
-   [**sohAttributeTypeFailureCategory TLV:**](sohattributetype-enum.md)Wenn komponenten- oder kommunikationsfehler auf dem Client oder Server aufgetreten sind, muss dies von dieser TLV angegeben werden. Diese TLV wird je nach Shv-Konfiguration weiterhin fehlerfrei oder fehlerhaft zugeordnet. Weitere Informationen finden Sie unter der [**INapServerManagement-Schnittstelle**](inapservermanagement.md) und der [**FailureCategoryMapping-Struktur.**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping)

Die SHV darf keine Verweise auf *Anforderungen* oder *Rückrufe* enthalten, sobald der asynchrone Aufruf abgeschlossen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapSystemHealthValidator**](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





