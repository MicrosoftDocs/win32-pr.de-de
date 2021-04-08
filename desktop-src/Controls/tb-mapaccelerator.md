---
title: TB_MAPACCELERATOR Meldung (kommstrg. h)
description: Bestimmt die ID der Schaltfläche, die dem angegebenen Zugriffstasten Zeichen entspricht.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- Windows-Steuerelemente für TB_MAPACCELERATOR Meldung
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029584d9e1614a3a135da5ebd3f4f446795fd9ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742657"
---
# <a name="tb_mapaccelerator-message"></a>TB \_ mapaccelerator-Meldung

Bestimmt die ID der Schaltfläche, die dem angegebenen Zugriffstasten Zeichen entspricht.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Das Zugriffstasten Zeichen.

</dd> <dt>

*LPARAM* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen **uint**. Bei erfolgreicher Rückgabe enthält dieser Parameter die ID der Schaltfläche, die über *wParam* als Zugriffstasten verfügt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn eine der Schaltflächen über *wParam* als Zugriffstaste verfügt, andernfalls 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ Mapacceleratorw** (Unicode) und **TB \_ mapacceleratora** (ANSI)<br/>       |



 

 





