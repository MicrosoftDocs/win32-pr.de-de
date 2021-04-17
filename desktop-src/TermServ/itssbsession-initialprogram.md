---
title: Itssbsession InitialProgram (Eigenschaft)
description: Ruft das Anfangs Programm für diese Sitzung ab oder legt es fest.
ms.assetid: c299c4f7-3c5f-468f-9fc7-81eac322dfa2
ms.tgt_platform: multiple
keywords:
- InitialProgram-Eigenschaft Remotedesktopdienste
- InitialProgram-Eigenschaft Remotedesktopdienste, itssbsession-Schnittstelle
- Itssbsession-Schnittstelle Remotedesktopdienste, InitialProgram-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbSession.InitialProgram
- ITsSbSession.get_InitialProgram
- ITsSbSession.put_InitialProgram
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 307f8bb4330caf4b84b8650c9ccc2551c94da76d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476728"
---
# <a name="itssbsessioninitialprogram-property"></a>Itssbsession:: InitialProgram-Eigenschaft

Ruft das Anfangs Programm für diese Sitzung ab oder legt es fest. Das erste Programm ist das Programm, das beim Starten der Benutzersitzung gestartet wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_InitialProgram(
  [in]          BSTR Application
);

HRESULT get_InitialProgram(
  [out, retval] BSTR *app
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine **BSTR** -Variable, die das ursprüngliche Programm enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itssbsession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





