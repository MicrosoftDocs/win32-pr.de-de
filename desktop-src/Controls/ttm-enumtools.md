---
title: TTM_ENUMTOOLS Meldung (kommstrg. h)
description: Ruft die Informationen ab, die ein QuickInfo-Steuerelement über das aktuelle Tool \ 8212 verwaltet, d. h. das Tool, für das die QuickInfo momentan Text anzeigt.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- Windows-Steuerelemente für TTM_ENUMTOOLS Meldung
topic_type:
- apiref
api_name:
- TTM_ENUMTOOLS
- TTM_ENUMTOOLSA
- TTM_ENUMTOOLSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad1679f9740539507a57c4cba93319569add0af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476791"
---
# <a name="ttm_enumtools-message"></a>TTM- \_ enumtoolsnachricht

Ruft die Informationen ab, die ein QuickInfo-Steuerelement über das aktuelle Tool, das Tool, für das die QuickInfo aktuell Text anzeigt, verwaltet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des Tools, für das Informationen abgerufen werden sollen.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur, die Informationen über das Tool empfängt. Legen Sie den **CBSIZE** -Member dieser Struktur auf sizeof (toolinfo) fest, bevor Sie diese Nachricht senden. Zuordnen eines Puffers. Legen Sie fest, dass der **lpszText** -Member auf den Puffer verweist, um den tooltext zu empfangen. Es gibt keine Möglichkeit, die erforderliche Puffergröße zu bestimmen. Allerdings hat der Tool Text, wie er im **lpszText** -Member der **toolinfo** -Struktur zurückgegeben wird, eine maximale Länge von 80 **tchars**, einschließlich des abschließenden **null**-Werts. Wenn der Text diese Länge überschreitet, wird er abgeschnitten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn Tools aufgelistet werden, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

**Sicherheitswarnung:** Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen. Diese Meldung bietet keine Möglichkeit, dass der Nachrichtenempfänger die Größe des Puffers kennt oder die Größe des Puffers angibt. Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ Enumtoolsw** (Unicode) und **TTM \_ enumtoolsa** (ANSI)<br/>               |



 

 





