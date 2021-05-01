---
title: TTM_ENUMTOOLS Nachricht (Commctrl.h)
description: Ruft die Informationen ab, die ein QuickInfo-Steuerelement über das aktuelle Tool \ 8212 verwaltet, d. h. das Tool, für das die QuickInfo derzeit Text anzeigt.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- TTM_ENUMTOOLS Meldung Windows-Steuerelemente
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
ms.openlocfilehash: a67f23a145838aa3562c81e78fb82c3ea66320df
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327135"
---
# <a name="ttm_enumtools-message"></a>\_TTM-ENUMTOOLS-Nachricht

Ruft die Informationen ab, die ein QuickInfo-Steuerelement über das aktuelle Tool verwaltet, d. h. das Tool, für das die QuickInfo derzeit Text anzeigt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index des Tools, für das Informationen abgerufen werden sollen.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TOOLINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) die Informationen über das Tool empfängt. Legen Sie den **cbSize-Member** dieser Struktur vor dem Senden dieser Nachricht auf sizeof(TOOLINFO) fest. Zuordnen eines Puffers. Legen Sie den **lpszText-Member** so fest, dass er auf den Puffer verweist, um den Tooltext zu empfangen. Es gibt keine Möglichkeit, die erforderliche Puffergröße zu bestimmen. Tooltext, wie er am **lpszText-Member** der **TOOLINFO-Struktur** zurückgegeben wird, hat jedoch eine maximale Länge von 80 **TCHARs,** einschließlich des abschließenden **NULL-Werts.** Wenn der Text diese Länge überschreitet, wird er abgeschnitten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **FALSE** zurück, unabhängig davon, ob ein Tool aufzählt wurde.

## <a name="remarks"></a>Hinweise

**Sicherheitswarnung:** Die Verwendung dieser Meldung kann die Sicherheit Ihres Programms gefährden. Diese Nachricht bietet keine Möglichkeit für den Nachrichtenempfänger, die Größe des Puffers zu kennen oder die Größe des Puffers anzugeben. Lesen Sie die [Sicherheitsüberlegungen: Microsoft Windows-Steuerelemente,](sec-comctls.md) bevor Sie fortfahren.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ ENUMTOOLSW** (Unicode) und **TTM \_ ENUMTOOLSA** (ANSI)<br/>               |



 

 





