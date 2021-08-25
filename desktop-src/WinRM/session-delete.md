---
title: Session.Delete-Methode (WSManDisp.h)
description: Löscht die im Ressourcen-URI angegebene Ressource.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- Delete-Methode Windows Remoteverwaltung
- Delete-Methode Windows Remoteverwaltung, Sitzungsobjekt
- Sitzungsobjekt Windows Remoteverwaltung , Delete-Methode
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
ms.openlocfilehash: 769ef3f462fa542e9afc6859b564e1a32ed87578894df4008fb6a19ad8aadad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858670"
---
# <a name="sessiondelete-method"></a>Session.Delete-Methode

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

*resourceUri* \[ In\]
</dt> <dd>

Der URI der zu löschenden Ressource. Sie können auch ein [**ResourceLocator-Objekt verwenden,**](resourcelocator.md) um die Ressource anzugeben.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Für die zukünftige Verwendung reserviert. Muss auf 0 festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die folgende Syntax wird zum Aufrufen dieser Methode verwendet.


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
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sitzungskonsistenz**](session.md)
</dt> </dl>

 

 





