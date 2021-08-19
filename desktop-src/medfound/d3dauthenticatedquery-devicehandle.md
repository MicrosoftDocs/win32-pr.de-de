---
description: Gibt ein Handle für das Gerät zurück, das diesem authentifizierten Kanal zugeordnet ist.
ms.assetid: 948eac1a-640a-47fd-b538-1de3ea5d8f0b
title: D3DAUTHENTICATEDQUERY_DEVICEHANDLE (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_DEVICEHANDLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fd2af1a889cb4a51ebd278ce7aba0154a96b1f5537ea971ab6ce11828baaa1b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974659"
---
# <a name="d3dauthenticatedquery_devicehandle"></a>D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE

Gibt ein Handle für das Gerät zurück, das diesem authentifizierten Kanal zugeordnet ist. Mit diesem Handle können Sie überprüfen, ob zwei authentifizierte Kanäle mit demselben Gerät kommunizieren.



| Anforderung | Wert |
|-------------|----------------------------------------------------------------------------------------------------------------|
| Abfrage-GUID  | **D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**                                                                        |
| Eingabedaten  | [**D3DAUTHENTICATEDCHANNEL-ABFRAGEEINGABE \_ \_**](d3dauthenticatedchannel-query-input.md)                           |
| Daten zurückgeben | [**D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE-AUSGABE \_**](d3dauthenticatedchannel-querydevicehandle-output.md) |



 

## <a name="remarks"></a>Hinweise

Diese Abfrage ist für alle Kanaltypen gültig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Content Protection Abfragen](content-protection-queries.md)
</dt> <dt>

[GPU-basierte Content Protection](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




