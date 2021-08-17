---
title: WSMan.CreateConnectionOptions-Methode (WSManDisp.h)
description: Erstellt ein ConnectionOptions-Objekt, das den Benutzernamen und das Kennwort angibt, die beim Erstellen einer Sitzung verwendet werden.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- CreateConnectionOptions-Methode Windows Remoteverwaltung
- CreateConnectionOptions-Methode Windows Remoteverwaltung , WSMan-Objekt
- WSMan-Objekt Windows Remoteverwaltung , CreateConnectionOptions-Methode
topic_type:
- apiref
api_name:
- WSMan.CreateConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4bd1218fcf6ca228cbc7538434b00b7b4e80d4c5b2df54807e031c11c14f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742667"
---
# <a name="wsmancreateconnectionoptions-method"></a>WSMan.CreateConnectionOptions-Methode

Erstellt ein [**ConnectionOptions-Objekt,**](connectionoptions.md) das den Benutzernamen und das Kennwort angibt, die beim Erstellen einer Sitzung verwendet werden.

## <a name="syntax"></a>Syntax


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Ein [**ConnectionOptions-Objekt,**](connectionoptions.md) mit dem ein Benutzername-Kennwort-Paar angegeben wird, das zum Identifizieren eines Benutzers für die Authentifizierung verwendet wird.

## <a name="remarks"></a>Hinweise

Die folgende Syntax wird zum Aufrufen dieser Methode verwendet.


```VB
Set options = wsman.CreateConnectionOptions
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

[**Wsman**](wsman.md)
</dt> <dt>

[**Connectionoptions**](connectionoptions.md)
</dt> </dl>

 

 





