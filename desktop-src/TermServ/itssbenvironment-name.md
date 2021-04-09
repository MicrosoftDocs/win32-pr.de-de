---
title: Name der itssbenvironment-Eigenschaft
description: Ruft einen Wert ab, der den Namen der Umgebung angibt, die den Zielcomputer hostet.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Name-Eigenschaft Remotedesktopdienste
- Name-Eigenschaft Remotedesktopdienste, itssbenvironment-Schnittstelle
- Itssbenvironment-Schnittstelle Remotedesktopdienste, Name-Eigenschaft
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
ms.openlocfilehash: 2b5ac2fd725ec07102c08e93b2bfb39dabe701ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949620"
---
# <a name="itssbenvironmentname-property"></a>Itssbenvironment:: Name-Eigenschaft

Ruft einen Wert ab, der den Namen der Umgebung angibt, die den Zielcomputer hostet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine **BSTR** -Variable, die den Namen der Umgebung enthält.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt eine Zeichenfolge zurück, die nicht direkt von Remotedesktopverbindung Broker (RD-Verbindungsbroker) verwendet wird. RD-Verbindungsbroker übergibt diese Zeichenfolge an Ressourcen-Plug-ins.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itssbenvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





