---
title: Itssbsession-Status Eigenschaft
description: Ruft den Sitzungszustand ab oder legt ihn fest.
ms.assetid: 4e769ff7-2bd5-4fcb-b2d7-4dedc853482b
ms.tgt_platform: multiple
keywords:
- State-Eigenschaft Remotedesktopdienste
- State-Eigenschaft Remotedesktopdienste, itssbsession-Schnittstelle
- Itssbsession-Schnittstelle Remotedesktopdienste, State-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbSession.State
- ITsSbSession.get_State
- ITsSbSession.put_State
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb939a518ab1050d932349cd70c85bcd22edf3d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479101"
---
# <a name="itssbsessionstate-property"></a>Itssbsession:: State (Eigenschaft)

Ruft den Sitzungszustand ab oder legt ihn fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_State(
  [in]          TSSESSION_STATE State
);

HRESULT get_State(
  [out, retval] TSSESSION_STATE *pState
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**tssession- \_ Zustands**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) Enumeration, die den Status einer Sitzung angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itssbsession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dt>

[**tssession- \_ Status**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state)
</dt> </dl>

 

 





