---
title: ConnectionOptions. Password-Eigenschaft (WSManDisp. h)
description: Legt das Kennwort eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer fest. Diese Eigenschaft bestimmt das Kennwort für die Authentifizierung.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Kenn Wort Eigenschaft Windows-Remoteverwaltung
- Password-Eigenschaft Windows-Remoteverwaltung, ConnectionOptions-Objekt
- ConnectionOptions-Objekt Windows-Remoteverwaltung, Password-Eigenschaft
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
ms.openlocfilehash: 2d4d553bf3f2a0a245e358e09a89eb1c00751e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104588"
---
# <a name="connectionoptionspassword-property"></a>ConnectionOptions. Password (Eigenschaft)

Legt das Kennwort eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer fest. Diese Eigenschaft bestimmt das Kennwort für die Authentifizierung. Weitere Informationen finden Sie unter [Authentifizierung für Remote Verbindungen](authentication-for-remote-connections.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a>Eigenschaftswert

Zeichenfolge, die das Kennwort eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer enthält.

Wenn kein Wert angegeben ist und das **wsmanflagkredusernamepassword** -Flag nicht festgelegt ist, wird das Kennwort des Kontos verwendet, von dem das Skript ausgeführt wird.

Wenn kein Wert angegeben und das **wsmanflagdedusernamepassword** -Flag festgelegt ist, fordert das Skript den Benutzer zur Eingabe des Kennworts auf (und den Benutzernamen, wenn dieser nicht angegeben ist). Wenn kein gültiger Benutzername und kein gültiger Kennwort eingegeben werden, wird ein Fehler vom Typ "Zugriff verweigert" zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass Sie das Kennwort nicht abrufen können. Das Kennwort kann nur mit dieser Eigenschaft festgelegt werden.

Wenn Sie ein [**ConnectionOptions**](connectionoptions.md) -Objekt erstellen und einen Benutzernamen und ein Kennwort verwenden, um eine Verbindung mit Windows-Remoteverwaltung herzustellen, sollte das **wsmanflagkredusernamepassword** -Flag für den [**WSMAN. kreatesession**](wsman-createsession.md)-aufrufen festgelegt werden.

Weitere Informationen zum Festlegen von Kenn Wörtern finden Sie im Abschnitt "Hinweise" unter [**ConnectionOptions**](connectionoptions.md).

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird ein [**ConnectionOptions**](connectionoptions.md) -Objekt erstellt und das **Kennwort** festgelegt.


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
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





