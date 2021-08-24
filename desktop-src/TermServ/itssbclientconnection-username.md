---
title: ITsSbClientConnection UserName (Eigenschaft)
description: Ruft einen Wert ab, der den Namen des Benutzers angibt, der die Verbindung initiiert hat.
ms.assetid: 74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54
ms.tgt_platform: multiple
keywords:
- UserName-Remotedesktopdienste
- UserName-Eigenschaft Remotedesktopdienste , ITsSbClientConnection-Schnittstelle
- ITsSbClientConnection-Schnittstelle Remotedesktopdienste , UserName-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbClientConnection.UserName
- ITsSbClientConnection.get_UserName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec6961e6c911b24df2e6c3adbea14b31a2ce8e5a66a9be9082357db957e646a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511330"
---
# <a name="itssbclientconnectionusername-property"></a>ITsSbClientConnection::UserName (Eigenschaft)

Ruft einen Wert ab, der den Namen des Benutzers angibt, der die Verbindung initiiert hat.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_UserName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen Benutzernamen. Wenn Sie die Verwendung der Zeichenfolge abgeschlossen haben, geben Sie sie frei, indem Sie die [**SysFreeString-Funktion**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

