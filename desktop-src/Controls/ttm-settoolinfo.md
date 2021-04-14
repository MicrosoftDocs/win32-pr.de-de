---
title: TTM_SETTOOLINFO Meldung (kommstrg. h)
description: Legt die Informationen fest, die ein QuickInfo-Steuerelement für ein Tool verwaltet.
ms.assetid: ba18f651-2e52-46e2-871b-c1760e94ab59
keywords:
- Windows-Steuerelemente für TTM_SETTOOLINFO Meldung
topic_type:
- apiref
api_name:
- TTM_SETTOOLINFO
- TTM_SETTOOLINFOA
- TTM_SETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327dd853e3304f8233b95c947a890c4f49298cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478951"
---
# <a name="ttm_settoolinfo-message"></a>TTM- \_ SetToolInfo-Meldung

Legt die Informationen fest, die ein QuickInfo-Steuerelement für ein Tool verwaltet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur, die die festzulegenden Informationen angibt. Der **CBSIZE** -Member dieser Struktur muss vor dem Senden dieser Nachricht festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Einige interne Eigenschaften eines Tools werden erstellt, wenn das Tool erstellt wird, und werden nicht neu berechnet, wenn eine **TTM- \_ SetToolInfo** -Nachricht gesendet wird. Wenn Sie einer [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur einfach Werte zuweisen und Sie mit einer **TTM- \_ SetToolInfo** -Meldung an das QuickInfo-Steuerelement übergeben, gehen diese Eigenschaften möglicherweise verloren. Stattdessen sollte die Anwendung zuerst die aktuelle **toolinfo** -Struktur des Tools anfordern, indem das QuickInfo-Steuerelement eine [**TTM \_ gettoolinfo**](ttm-gettoolinfo.md) -Nachricht sendet. Ändern Sie dann die Elemente dieser Struktur nach Bedarf, und übergeben Sie Sie mit **TTM \_ SetToolInfo** zurück an das QuickInfo-Steuerelement.

Beim Aufrufen von **TTM \_ SetToolInfo** darf die Zeichenfolge, auf die der **lpszText** -Member der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur verweist, nicht länger als 80 **tchars** sein, einschließlich des abschließenden **null**-Werts.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ Settoolinfow** (Unicode) und **TTM \_ settoolinfoa** (ANSI)<br/>           |



 

 





