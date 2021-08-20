---
title: TB_SETBOUNDINGSIZE Nachricht (Commctrl.h)
description: Legt die Begrenzungsgröße für ein symbolleistenbasiertes Steuerelement mit mehreren Spalten fest.
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- TB_SETBOUNDINGSIZE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 7d409769e08e489d922dbdc2361779953555000dca784a6f7b977bbbcd3a5e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167743"
---
# <a name="tb_setboundingsize-message"></a>TB \_ SETBOUNDINGSIZE-Nachricht

\[Für die interne Verwendung vorgesehen; nicht für die Verwendung in Anwendungen empfohlen. Diese Meldung wird in zukünftigen Versionen von Windows möglicherweise nicht mehr unterstützt.\]

Legt die Begrenzungsgröße für ein symbolleistenbasiertes Steuerelement mit mehreren Spalten fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**SIZE-Struktur,**](/previous-versions//dd145106(v=vs.85)) deren **Cy-Member** die umgebende Höhe enthält. Der **cx-Member** (die Breite) wird ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Die Verwendung dieser Meldung kann die Sicherheit Ihres Programms gefährden.

## <a name="remarks"></a>Hinweise

Die Begrenzungsgröße steuert, wie Schaltflächen in Spalten organisiert werden. Wenn das Symbolleistensteuerelement nicht über den [**TBSTYLE \_ EX \_ MULTICOLUMN-Stil**](toolbar-extended-styles.md) verfügt, hat diese Meldung keine Auswirkungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

