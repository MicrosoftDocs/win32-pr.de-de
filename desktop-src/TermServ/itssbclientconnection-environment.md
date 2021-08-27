---
title: ITsSbClientConnection-Umgebungseigenschaft
description: Ruft ein -Objekt ab, das Informationen über die Umgebung enthält, die den Zielcomputer hostet.
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- Umgebungseigenschaft Remotedesktopdienste
- Umgebungseigenschaft Remotedesktopdienste , ITsSbClientConnection-Schnittstelle
- ITsSbClientConnection-Schnittstelle Remotedesktopdienste , Umgebungseigenschaft
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33cc1c3c8a13a21135ee834950e8c0a60d2794cd4b1edb618e5e67c0744fe3e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072210"
---
# <a name="itssbclientconnectionenvironment-property"></a>ITsSbClientConnection::Environment (Eigenschaft)

Ruft ein -Objekt ab, das Informationen über die Umgebung enthält, die den Zielcomputer hostet. In einem Szenario mit virtuellem Desktop würde dieses Objekt beispielsweise Informationen über den Computer enthalten, der den virtuellen Computer hostet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen Zeiger auf ein [**ITsSbEnvironment-Umgebungsobjekt.**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)

## <a name="error-codes"></a>Fehlercodes

Wenn die Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Mögliche Werte sind u. a. die in der folgenden Liste angegebenen Werte.

<dl> <dt>

\_E-ZEIGER
</dt> <dd>

Die Umgebung wurde nicht gefunden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Orchestrierungs-Plug-In kann diese Methode aufrufen, um Umgebungsinformationen zu einem virtuellen Zielcomputer abzurufen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





