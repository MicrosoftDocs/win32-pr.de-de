---
title: TB_ADDSTRING (Commctrl.h)
description: Fügt dem Zeichenfolgenpool der Symbolleiste eine neue Zeichenfolge hinzu.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- TB_ADDSTRING von Windows Steuerelementen
topic_type:
- apiref
api_name:
- TB_ADDSTRING
- TB_ADDSTRINGA
- TB_ADDSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0556add41addb4a58d5734ab900af4a43c2018b533723145ed4f9c8272e3890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078374"
---
# <a name="tb_addstring-message"></a>TB \_ ADDSTRING-Meldung

Fügt dem Zeichenfolgenpool der Symbolleiste eine neue Zeichenfolge hinzu.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für die Modulinstanz mit einer ausführbaren Datei, die die Zeichenfolgenressource enthält. Wenn *lParam* stattdessen auf ein Zeichenarray mit mindestens einer Zeichenfolge zeigt, legen Sie diesen Parameter auf **NULL fest.**

</dd> <dt>

*lParam* 
</dt> <dd>

Ressourcenbezeichner für die Zeichenfolgenressource oder ein Zeiger auf ein TCHAR-Array. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Index der ersten neuen Zeichenfolge zurück, andernfalls -1.

## <a name="remarks"></a>Hinweise

Wenn *wParam* **NULL ist,** *zeigt lParam* auf ein Zeichenarray mit einer oder mehr Zeichenfolgen mit NULL-Terminierung. Die letzte Zeichenfolge im Array muss mit zwei NULL-Zeichen beendet werden.

Wenn *wParam* die HINSTANCE der Anwendung oder eines anderen Moduls ist, das eine Zeichenfolgenressource enthält, ist *lParam* der Ressourcenbezeichner der Zeichenfolge. Jedes Element in der Zeichenfolge muss mit einem beliebigen Trennzeichen beginnen, und die Zeichenfolge muss mit zwei solchen Zeichen enden. Beispielsweise kann der Text für drei Schaltflächen in der Zeichenfolgentabelle als "/New/Open/Save/" angezeigt werden. Die Meldung gibt den Index von "New" im Zeichenfolgenpool der Symbolleiste zurück, und die anderen Elemente befinden sich an aufeinanderfolgenden Positionen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ ADDSTRINGW** (Unicode) und **TB \_ ADDSTRINGA** (ANSI)<br/>                 |



 

 





