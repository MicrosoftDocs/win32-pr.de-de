---
title: Session. Delete-Methode (WSManDisp. h)
description: Löscht die im Ressourcen-URI angegebene Ressource.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- Delete-Methode Windows-Remoteverwaltung
- Delete-Methode Windows-Remoteverwaltung, Session-Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, DELETE-Methode
topic_type:
- apiref
api_name:
- Session.Delete
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf4b46997a7e3cf50dbf50c2828de78a814a513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949609"
---
# <a name="sessiondelete-method"></a>Session. Delete-Methode

Löscht die im Ressourcen-URI angegebene Ressource.

## <a name="syntax"></a>Syntax


```VB
Session.Delete( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*resourceUri* \[ in\]
</dt> <dd>

Der URI der zu löschenden Ressource. Sie können auch ein [**ResourceLocator**](resourcelocator.md) -Objekt verwenden, um die Ressource anzugeben.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Für die zukünftige Verwendung reserviert. Muss auf 0 festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die folgende Syntax wird verwendet, um diese Methode aufzurufen.


```VB
session.Delete("<resourceUri>")
```



## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel werden die für den HTTP-Transport konfigurierten Listener gelöscht.


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
  "config/Listener?Address=*+Transport=HTTP"
objSession.Delete(strResource)
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

[**Sitzung**](session.md)
</dt> </dl>

 

 





