---
title: Itssbclientconnection-Domänen Eigenschaft
description: Ruft einen Wert ab, der den Domänen Namen des-Remotedesktopverbindung (RDC)-Clients angibt.
ms.assetid: 628f450d-10f4-4405-8d7c-ae58c72c2755
ms.tgt_platform: multiple
keywords:
- Domänen Eigenschaft Remotedesktopdienste
- Domänen Eigenschaft Remotedesktopdienste, itssbclientconnection-Schnittstelle
- Itssbclientconnection-Schnittstelle Remotedesktopdienste, Domänen Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Domain
- ITsSbClientConnection.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 678d6fc6838b615faeec9fa36b736b3105b64453
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344097"
---
# <a name="itssbclientconnectiondomain-property"></a>Itssbclientconnection::D omain-Eigenschaft

Ruft einen Wert ab, der den Domänen Namen des-Remotedesktopverbindung (RDC)-Clients angibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine **BSTR** -Variable, die den Domänen Namen des RDC-Clients enthält. Wenn Sie die Zeichenfolge nicht mehr verwenden, können Sie Sie durch Aufrufen der [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) -Funktion freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itssbclientconnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

