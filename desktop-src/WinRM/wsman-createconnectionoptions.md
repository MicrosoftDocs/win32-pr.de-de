---
title: WSMAN. kreateconnectionoptions-Methode (WSManDisp. h)
description: Erstellt ein ConnectionOptions-Objekt, das den Benutzernamen und das Kennwort angibt, die beim Erstellen einer Sitzung verwendet werden.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- Windows-Remoteverwaltung der Methode "kreateconnectionoptions"
- Methode "kreateconnectionoptions" Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, Methode "kreateconnectionoptions"
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
ms.openlocfilehash: e051b65e7ab85f11d6a10b94573082da8823ce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858764"
---
# <a name="wsmancreateconnectionoptions-method"></a>WSMAN. kreateconnectionoptions-Methode

Erstellt ein [**ConnectionOptions**](connectionoptions.md) -Objekt, das den Benutzernamen und das Kennwort angibt, die beim Erstellen einer Sitzung verwendet werden.

## <a name="syntax"></a>Syntax


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Ein [**ConnectionOptions**](connectionoptions.md) -Objekt, mit dem ein Benutzername und ein Kennwort-Paar angegeben werden, mit dem ein Benutzer für die Authentifizierung identifiziert wird.

## <a name="remarks"></a>Bemerkungen

Die folgende Syntax wird verwendet, um diese Methode aufzurufen.


```VB
Set options = wsman.CreateConnectionOptions
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

[**WSMAN**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





