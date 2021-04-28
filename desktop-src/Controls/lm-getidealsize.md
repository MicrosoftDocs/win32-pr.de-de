---
title: LM_GETIDEALSIZE (Commctrl.h)
description: 'LM_GETIDEALSIZE Meldung: Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuerelements ab.'
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE Meldung Windows-Steuerelemente
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
ms.openlocfilehash: 761fb5f6e5f7a2e2e9b1b9cc862b9a8f2c0fcd1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112388"
---
# <a name="lm_getidealsize-message"></a>LM \_ GETIDEALSIZE-Nachricht

Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuerelements ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Maximale Breite des Links in Pixel.</dd> <dt>

*lParam* \[ out\]
</dt> <dd>Enthält nach der Rückgabe dieser Meldung einen Zeiger auf eine <a href="/previous-versions//dd145106(v=vs.85)">**SIZE-Struktur.**</a> Der **Cy-Member** dieser -Struktur gibt die ideale Höhe des Steuerelements für die gegebene Breite an. Sie passt das **Cx-Member** an den tatsächlich benötigten Speicherplatz an.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine ganze Zahl, die die bevorzugte Höhe des Linktexts in Pixel darstellt.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Um diese API verwenden zu können, müssen Sie ein Manifest bereitstellen, das Comclt32.dll 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

