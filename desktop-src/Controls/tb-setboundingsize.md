---
title: TB_SETBOUNDINGSIZE Meldung (kommstrg. h)
description: Legt die Begrenzungs Größe für ein mehrspaltige Symbolleisten-Steuerelement fest.
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- Windows-Steuerelemente für TB_SETBOUNDINGSIZE Meldung
topic_type:
- apiref
api_name:
- TB_SETBOUNDINGSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 419595da16148f7382da5053d3187e9cce9e00a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858636"
---
# <a name="tb_setboundingsize-message"></a>TB \_ setboundingsize-Meldung

\[Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen. Diese Meldung wird möglicherweise in zukünftigen Versionen von Windows nicht mehr unterstützt.\]

Legt die Begrenzungs Größe für ein mehrspaltige Symbolleisten-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur, deren **CY** -Member die umgebende Höhe enthält. Der **CX** -Member (die Breite) wird ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen.

## <a name="remarks"></a>Bemerkungen

Die Begrenzungs Größe steuert, wie Schaltflächen in Spalten angeordnet sind. Wenn das Symbolleisten-Steuerelement nicht über das Format [**tbstyle \_ Ex \_ MultiColumn**](toolbar-extended-styles.md) verfügt, hat diese Nachricht keine Auswirkung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

