---
title: ITsSbEnvironment Name (Eigenschaft)
description: Ruft einen Wert ab, der den Namen der Umgebung angibt, die den Zielcomputer hostet.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Name-Remotedesktopdienste
- Name-Remotedesktopdienste , ITsSbEnvironment-Schnittstelle
- ITsSbEnvironment-Schnittstelle Remotedesktopdienste , Name-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbEnvironment.Name
- ITsSbEnvironment.get_Name
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d60f64cf8bc350ca80072b2c7a43ecabf2fbe5d4650188b7d5a5e5c05a4fbc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072200"
---
# <a name="itssbenvironmentname-property"></a>ITsSbEnvironment::Name (Eigenschaft)

Ruft einen Wert ab, der den Namen der Umgebung angibt, die den Zielcomputer hostet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine **BSTR-Variable,** die den Namen der Umgebung enthält.

## <a name="remarks"></a>Hinweise

Diese Methode gibt eine Zeichenfolge zurück, die nicht direkt von Remotedesktopverbindung Broker (RD-Verbindungsbroker) verwendet wird. Der RD-Verbindungsbroker übergibt diese Zeichenfolge an Ressourcen-Plug-Ins.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





