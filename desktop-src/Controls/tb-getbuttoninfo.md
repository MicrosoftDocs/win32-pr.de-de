---
title: TB_GETBUTTONINFO Meldung (kommstrg. h)
description: Ruft erweiterte Informationen für eine Schaltfläche in einer Symbolleiste ab.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- Windows-Steuerelemente für TB_GETBUTTONINFO Meldung
topic_type:
- apiref
api_name:
- TB_GETBUTTONINFO
- TB_GETBUTTONINFOA
- TB_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c7f6a8d1d36737d09cfb4d307129200a51180c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106599"
---
# <a name="tb_getbuttoninfo-message"></a>TB \_ getbuttoninfo-Meldung

Ruft erweiterte Informationen für eine Schaltfläche in einer Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Befehls Bezeichner der Schaltfläche.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**tbbuttoninfo**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) -Struktur, die die Schaltflächen Informationen empfängt. Die Member **CBSIZE** und **dwMask** dieser Struktur müssen ausgefüllt werden, bevor diese Nachricht gesendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den NULL basierten Index der Schaltfläche oder-1 zurück, wenn ein Fehler auftritt.

## <a name="remarks"></a>Bemerkungen

Wenn Sie mit [**TB \_ AddButtons**](tb-addbuttons.md) oder [**TB \_ InsertButton**](tb-insertbutton.md) Schaltflächen auf der Symbolleiste platzieren, wird der Schaltflächen Text häufig durch den zugehörigen Zeichen folgen Pool Index angegeben. **TB \_ Getbuttoninfo** ruft diese Zeichenfolge nicht ab. Wenn Sie " **TB \_ getbuttoninfo** " zum Abrufen von Schaltflächen Text verwenden möchten, müssen Sie zunächst die Text Zeichenfolge mit " [**TB \_ SetButtonInfo**](tb-setbuttoninfo.md)" festlegen Nachdem Sie den Schaltflächen Text mit **TB \_ SetButtonInfo** festgelegt haben, können Sie den Zeichen folgen-Pool Index nicht mehr verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ Getbuttoninfow** (Unicode) und **TB \_ getbuttoninfoa** (ANSI)<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**TB \_ SetButtonInfo**](tb-setbuttoninfo.md)
</dt> <dt>

[**TB \_ getbuttontext**](tb-getbuttontext.md)
</dt> </dl>

 

 





