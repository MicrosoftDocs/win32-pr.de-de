---
title: INapEnforcementClientBinding ProcessSoHResponse-Methode (NapEnforcementClient.h)
description: Wird von Erzwingungsclients verwendet, um eine SoHResponse zu verarbeiten, wenn sie ein SoHResponse-Datenblob vom Erzwingungsserver empfangen.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- ProcessSoHResponse-Methode NAP
- ProcessSoHResponse-Methode NAP, INapEnforcementClientBinding-Schnittstelle
- INapEnforcementClientBinding-Schnittstelle NAP , ProcessSoHResponse-Methode
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
ms.openlocfilehash: 4cffd2caeaf3a39bd5c28b4850fc560dc9567a3552aad88929581efd2729acce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621709"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a>INapEnforcementClientBinding::P rocessSoHResponse-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapEnforcementClientBinding::P rocessSoHResponse-Methode** wird von Erzwingungsclients verwendet, um eine SoHResponse zu verarbeiten, wenn sie ein SoHResponse-Datenblob vom Erzwingungsserver empfangen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verbindung* \[ In\]
</dt> <dd>

Ein COM-Zeiger auf die [**INapEnforcementClientConnection-Schnittstelle**](inapenforcementclientconnection.md) der Clientverbindung. NapAgent enthält keine Verweise auf das Objekt, das dieser Schnittstelle zugeordnet ist, nachdem dieser Methodenaufruf abgeschlossen wurde.

Sie müssen eine zuvor hergestellte Verbindung für die Verarbeitung von SOHResponse-Datenblobs verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                             | Beschreibung                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Der Vorgang ist erfolgreich.<br/>                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Zuvor wurden keine Verbindungen auf dem Erzwingungsclient erstellt. <br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Berechtigungsfehler, Zugriff verweigert.<br/>                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/>                                                                                                                                                                                                                                                                 |
| <dl> <dt>**NAP \_ E \_ INVALID \_ PACKET**</dt> </dl>  | Wenn dieser Wert zurückgegeben wird, muss der Erzwingungsclient das Paket löschen, wenn NapAgent NAP \_ E INVALID PACKET zurückgibt. \_ \_ In diesem Fall muss der Erzwingende davon ausgehen, dass der Server, mit dem er spricht, nicht NAP-fähig ist, und die Verbindung aus der aktiven Liste entfernen (d. h. napAgent über einen Verbindungsstatus benachrichtigen).<br/> |
| <dl> <dt>**NICHT \_ \_ ÜBEREINSTIMMENDE \_ NAP E-ID**</dt> </dl>   | Wenn dieser Wert zurückgegeben wird, gibt er an, dass die Korrelations-ID im SoH-Response Paket nicht mit der ausstehenden SoH-Response übereinstimmt. In diesem Fall sollte der Erzwingende das Paket löschen und auf ein anderes neueres SoH-Response Paket warten.<br/> Dies kann durch eine Antwort auf eine ältere Anforderungsnachricht verursacht werden.<br/>        |
| <dl> <dt>**NAP \_ E \_ NICHT \_ INITIALISIERT**</dt> </dl> | Der Enforcer wurde zuvor nicht initialisiert.<br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a>Hinweise

NapAgent fragt das SoH-Response Datenblob aus dem Verbindungsobjekt ab, verarbeitet es und legt die resultierende Entscheidung fest (z. B. vollständiger/eingeschränkter Zugriff/usw.) für das Verbindungsobjekt.

Der Erzwingungsclient muss die [**INapEnforcementClientBinding::Initialize-Methode**](inapenforcementclientbinding-initialize-method.md) aufrufen, bevor er diese oder eine andere Methode der [**INapEnforcementClientBinding-Schnittstelle aufruft.**](inapenforcementclientbinding.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





