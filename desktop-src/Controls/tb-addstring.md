---
title: TB_ADDSTRING Meldung (kommstrg. h)
description: Fügt eine neue Zeichenfolge zum Zeichen folgen Pool der Symbolleiste hinzu.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- Windows-Steuerelemente für TB_ADDSTRING Meldung
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
ms.openlocfilehash: 6fba57c298a2b903a65c429ae6b4f9d55fc9ed2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345344"
---
# <a name="tb_addstring-message"></a>TB \_ AddString-Nachricht

Fügt eine neue Zeichenfolge zum Zeichen folgen Pool der Symbolleiste hinzu.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für die Modul Instanz mit einer ausführbaren Datei, die die Zeichen folgen Ressource enthält. Wenn *LPARAM* stattdessen auf ein Zeichen Array mit einer oder mehreren Zeichen folgen verweist, legen Sie diesen Parameter auf **null** fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Der Ressourcen Bezeichner für die Zeichen folgen Ressource oder ein Zeiger auf ein TCHAR-Array. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index der ersten neuen Zeichenfolge zurück, wenn erfolgreich, andernfalls-1.

## <a name="remarks"></a>Bemerkungen

Wenn *wParam* den Wert **null** hat, verweist *LPARAM* auf ein Zeichen Array mit einer oder mehreren null-terminierten Zeichen folgen. Die letzte Zeichenfolge im Array muss mit zwei NULL-Zeichen beendet werden.

Wenn *wParam* die HINSTANCE der Anwendung oder eines anderen Moduls mit einer Zeichen folgen Ressource ist, ist *LPARAM* der Ressourcen Bezeichner der Zeichenfolge. Jedes Element in der Zeichenfolge muss mit einem beliebigen Trennzeichen beginnen, und die Zeichenfolge muss mit zwei Zeichen enden Zeichen enden. Beispielsweise kann der Text für drei Schaltflächen in der Zeichen folgen Tabelle als "/New/Open/Save//" angezeigt werden. Die Meldung gibt den Index "New" im Zeichen folgen Pool der Symbolleiste zurück, und die anderen Elemente befinden sich in aufeinander folgenden Positionen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ Addstringw** (Unicode) und **TB \_ addstraninga** (ANSI)<br/>                 |



 

 





