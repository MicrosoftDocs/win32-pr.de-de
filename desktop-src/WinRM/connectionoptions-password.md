---
title: ConnectionOptions.Password-Eigenschaft (WSManDisp.h)
description: Legt das Kennwort eines lokalen kontos oder eines Domänenkontos auf dem Remotecomputer fest. Diese Eigenschaft bestimmt das Kennwort für die Authentifizierung.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Kennworteigenschaft Windows Remoteverwaltung
- Kennworteigenschaft Windows Remoteverwaltung, ConnectionOptions-Objekt
- ConnectionOptions-Objekt Windows Remoteverwaltung , Password-Eigenschaft
topic_type:
- apiref
api_name:
- ConnectionOptions.Password
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ffc992b5a0560175d6562a16cf4cb3fd6bc4259eb3b712e26708dc713baba14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898990"
---
# <a name="connectionoptionspassword-property"></a>ConnectionOptions.Password-Eigenschaft

Legt das Kennwort eines lokalen kontos oder eines Domänenkontos auf dem Remotecomputer fest. Diese Eigenschaft bestimmt das Kennwort für die Authentifizierung. Weitere Informationen finden Sie unter [Authentifizierung für Remoteverbindungen.](authentication-for-remote-connections.md)

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a>Eigenschaftswert

Zeichenfolge, die das Kennwort eines lokalen kontos oder eines Domänenkontos auf dem Remotecomputer enthält.

Wenn kein Wert angegeben wird und das **Flag WSManFlagCredUsernamePassword** nicht festgelegt ist, wird das Kennwort des Kontos verwendet, das das Skript ausführt.

Wenn kein Wert angegeben wird und das **Flag WSManFlagCredUsernamePassword** festgelegt ist, fordert das Skript den Benutzer auf, das Kennwort einzugeben (und den Benutzernamen, wenn dieser nicht angegeben wird). Wenn kein gültiger Benutzername und kein Kennwort eingegeben werden, wird ein Zugriffsverweigerungsfehler zurückgegeben.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass Sie das Kennwort nicht abrufen können. Das Kennwort kann nur mit dieser Eigenschaft festgelegt werden.

Wenn Sie ein [**ConnectionOptions-Objekt**](connectionoptions.md) erstellen und einen Benutzernamen und ein Kennwort zum Herstellen einer Verbindung mit Windows Remoteverwaltung verwenden, sollte das **Flag WSManFlagCredUserNamePassword** beim Aufruf von [**WSMan.CreateSession**](wsman-createsession.md)festgelegt werden.

Weitere Informationen zum Festlegen von Kennwörtern finden Sie im Abschnitt Hinweise unter [**ConnectionOptions**](connectionoptions.md).

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird ein [**ConnectionOptions-Objekt**](connectionoptions.md) erstellt und das **Kennwort** festgelegt.


```VB
' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "<password>"
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Connectionoptions**](connectionoptions.md)
</dt> </dl>

 

 





