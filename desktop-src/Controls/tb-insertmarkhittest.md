---
title: TB_INSERTMARKHITTEST Meldung (kommstrg. h)
description: Ruft die einfügemarkierungsinformationen für einen Punkt in einer Symbolleiste ab.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- Windows-Steuerelemente für TB_INSERTMARKHITTEST Meldung
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5237d5a13250c3eb95bfe741415a9da245585c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040432"
---
# <a name="tb_insertmarkhittest-message"></a>TB \_ insertmarkhittest-Meldung

Ruft die einfügemarkierungsinformationen für einen Punkt in einer Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die die Treffer Test Koordinaten relativ zum Client Bereich der Symbolleiste enthält.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**tbinsertmark**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) -Struktur, die die einfügemarkierungsinformationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn der Punkt eine Einfügemarke ist, andernfalls NULL

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

