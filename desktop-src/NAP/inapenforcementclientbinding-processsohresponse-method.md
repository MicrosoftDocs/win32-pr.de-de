---
title: Inapenforcementclientbinding processsohresponse-Methode (napforcementclient. h)
description: Wird von Erzwingungs Clients verwendet, um eine sohresponse zu verarbeiten, wenn Sie ein sohresponse-datenblob von dem Erzwingungs Server erhalten.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- Processsohresponse-Methode NAP
- Processsohresponse-Methode NAP, inapenforcementclientbinding-Schnittstelle
- Inapenforcementclientbinding-Schnittstelle NAP, processsohresponse-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.ProcessSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ac8c87314ca1e28163428bf53e4a1fc6e31106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519175"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a>Inapenforcementclientbinding::P rocesssohresponse-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientbinding::P rocesssohresponse** -Methode wird von Erzwingungs Clients verwendet, um eine sohresponse zu verarbeiten, wenn Sie ein sohresponse-datenblob von dem Erzwingungs Server erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verbindung* \[ in\]
</dt> <dd>

Ein com-Zeiger auf die [**inapenforcementclientconnection**](inapenforcementclientconnection.md) -Schnittstelle der Client Verbindung. Der NAPAgent enthält keine Verweise auf das Objekt, das dieser Schnittstelle zugeordnet ist, nachdem dieser Methoden Aufrufvorgang abgeschlossen wurde.

Sie müssen eine zuvor festgelegte Verbindung für die Verarbeitung von sohresponse-datenblobvorgängen verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                             | Beschreibung                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Der Vorgang ist erfolgreich.<br/>                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>            | Auf dem Erzwingungs Client wurden zuvor keine Verbindungen erstellt. <br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl>         | Berechtigungs Fehler, Zugriff verweigert.<br/>                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>          | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/>                                                                                                                                                                                                                                                                 |
| <dl> <dt>**\_ \_ Ungültiges NAP- \_ Paket**</dt> </dl>  | Wenn dieser Wert zurückgegeben wird, muss der Erzwingungs Client das Paket löschen, wenn der NAPAgent ein ungültiges NAP-Paket zurückgibt \_ \_ \_ . In diesem Fall muss der Enforcer davon ausgehen, dass der Server, mit dem er kommuniziert, nicht NAP-fähig ist, und die Verbindung aus der aktiven Liste entfernen (d. h., der NAPAgent wird über einen Verbindungsstatus benachrichtigt).<br/> |
| <dl> <dt>**nicht \_ \_ übereinstimmende NAP- \_ ID**</dt> </dl>   | Wenn dieser Wert zurückgegeben wird, weist dies darauf hin, dass die Korrelations-ID im SoH-Response Paket nicht mit der ausstehenden SoH-Antwort identisch war. In diesem Fall sollte der Enforcer das Paket löschen und auf ein anderes neueres SoH-Response Paket warten.<br/> Dies kann durch eine Antwort auf eine ältere Anforderungs Nachricht verursacht werden.<br/>        |
| <dl> <dt>**NAP \_ E \_ nicht \_ Initialisiert**</dt> </dl> | Der Enforcer wurde nicht bereits initialisiert.<br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Der NAPAgent fragt den SoH-Response Data BLOB aus dem Verbindungs Objekt ab, verarbeitet ihn und legt die resultierende Entscheidung fest (z. b. vollständiger/eingeschränkter Zugriff/usw.) für das Verbindungs Objekt.

Der Erzwingungs Client muss die [**inapenforcementclientbinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) -Methode aufrufen, bevor diese oder eine andere Methode der [**inapenforcementclientbinding**](inapenforcementclientbinding.md) -Schnittstelle aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napforcementclient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napforcementclient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>


</dt> <dt>

[**Inapenforcementclientbinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**Inapenforcementclientconnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





