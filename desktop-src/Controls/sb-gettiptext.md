---
title: SB_GETTIPTEXT-Nachricht (Commctrl.h)
description: Ruft den QuickInfo-Text für ein Teil in einer Statusleiste ab. Die Statusleiste muss mit dem SBT \_ TOOLTIPS-Format erstellt werden, um QuickInfos zu aktivieren.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- SB_GETTIPTEXT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89a78fa6650d850cad2b6de8cc77f1d44b49b8325bf6856b989953fc6511f56f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637130"
---
# <a name="sb_gettiptext-message"></a>SB \_ GETTIPTEXT-Nachricht

Ruft den QuickInfo-Text für ein Teil in einer Statusleiste ab. Die Statusleiste muss mit dem [**SBT \_ TOOLTIPS-Format**](status-bar-styles.md) erstellt werden, um QuickInfos zu aktivieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den nullbasierten Index des Teils an, der den QuickInfo-Text empfängt. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die Größe des Puffers bei *lParam* in Zeichen an.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Zeichenpuffer, der den QuickInfo-Text empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Hinweise

**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies zu Problemen für Ihre Anwendung führen. Wenn der Text beispielsweise zu groß für den *lParam-Puffer* ist, kann dies zu einem Pufferüberlauf führen. Lesen Sie die [Sicherheitsüberlegungen: Microsoft Windows Controls,](sec-comctls.md) bevor Sie fortfahren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **SB \_ GETTIPTEXTW** (Unicode) und **SB \_ GETTIPTEXTA** (ANSI)<br/>               |



 

