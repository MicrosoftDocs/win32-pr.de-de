---
title: Itssbtaskinfo-Bezeichnung (Eigenschaft)
description: Ruft die Bezeichnung ab, die den Zweck der Aufgabe beschreibt.
ms.assetid: 075de6a4-53b0-43b0-9bca-03bf312fff6e
ms.tgt_platform: multiple
keywords:
- Eigenschaft "Bezeichnung" Remotedesktopdienste
- Label-Eigenschaft Remotedesktopdienste, itssbtaskinfo-Schnittstelle
- Itssbtaskinfo-Schnittstelle Remotedesktopdienste, Label-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Label
- ITsSbTaskInfo.get_Label
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f85aaea366cf002d4ec1bacce8f29a6aa67fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743505"
---
# <a name="itssbtaskinfolabel-property"></a>Itssbtaskinfo:: Label-Eigenschaft

Ruft die Bezeichnung ab, die den Zweck der Aufgabe beschreibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Label(
  [out, retval] BSTR *pLabel
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen **BSTR** -Wert, der die Bezeichnung enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itssbtaskinfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





