---
title: LM_GETIDEALSIZE Meldung (kommstrg. h)
description: Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuer Elements ab.
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- Windows-Steuerelemente für LM_GETIDEALSIZE Meldung
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c138e22982116a3b7173f586d96c70cfc91194c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475207"
---
# <a name="lm_getidealsize-message"></a>LM- \_ getidealsize-Nachricht

Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuer Elements ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Maximale Breite des Links in Pixel.</dd> <dt>

*LPARAM* \[ vorgenommen\]
</dt> <dd>Wenn diese Nachricht zurückgegeben wird, enthält Sie einen Zeiger auf eine <a href="/previous-versions//dd145106(v=vs.85)">**Größen**</a> Struktur. Der **CY** -Member dieser Struktur gibt die ideale Höhe des Steuer Elements für die angegebene Breite an. Der **CX** -Member wird an den tatsächlich benötigten Speicherplatz angepasst.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine ganze Zahl, die die bevorzugte Höhe des linktexts in Pixel darstellt.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Um diese API zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

