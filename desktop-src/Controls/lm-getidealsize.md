---
title: LM_GETIDEALSIZE (Commctrl.h)
description: 'LM_GETIDEALSIZE Meldung: Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuerelements ab.'
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE meldungssteuerelemente Windows
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
ms.openlocfilehash: 035a919aabeb5d07587c7d9e4fc97e5edc728de4ec8fc476448dca62658f1ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958373"
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

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese API verwenden zu können, müssen Sie ein Manifest bereitstellen, das Comclt32.dll 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

