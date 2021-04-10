---
title: CB_GETLBTEXT Meldung (Winuser. h)
description: Ruft eine Zeichenfolge aus der Liste eines Kombinations Felds ab.
ms.assetid: f84e302a-65bb-45c8-958b-1cb438fb5a7a
keywords:
- Windows-Steuerelemente für CB_GETLBTEXT Meldung
topic_type:
- apiref
api_name:
- CB_GETLBTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d26a964b463daedab1ad5d9f50888b3e0c1e0db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040601"
---
# <a name="cb_getlbtext-message"></a>CB \_ getlbtext-Nachricht

Ruft eine Zeichenfolge aus der Liste eines Kombinations Felds ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der abzurufenden Zeichenfolge.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf den Puffer, der die Zeichenfolge empfängt. Der Puffer muss über ausreichend Speicherplatz für die Zeichenfolge und ein abschließendes NULL-Zeichen verfügen. Sie können eine [**CB \_ getlbtextlen**](cb-getlbtextlen.md) -Nachricht vor der **CB \_ getlbtext** -Nachricht senden, um die Länge der Zeichenfolge in **TCHAR** s abzurufen. Wenn es sich um eine ANSI-Zeichenfolge handelt, ist dies die Anzahl von Bytes, aber wenn es sich um eine Unicode-Zeichenfolge handelt, ist dies die Anzahl der Zeichen

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Länge der Zeichenfolge in **TCHAR** s, wobei das abschließende Null-Zeichen ausgeschlossen wird. Wenn von *wParam* kein gültiger Index angegeben wird, ist der Rückgabewert CB \_ Err.

## <a name="remarks"></a>Bemerkungen

**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies die Sicherheit des Programms beeinträchtigen. Diese Meldung bietet keine Möglichkeit, die Größe des Puffers zu kennen. Wenn Sie diese Meldung verwenden, rufen Sie zunächst [**CB \_ getlbtextlen**](cb-getlbtextlen.md) auf, um die erforderliche Anzahl von Zeichen abzurufen, und rufen Sie dann die Nachricht zum Abrufen der Zeichenfolge auf. Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.

Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, empfängt der Puffer, auf den *LPARAM* verweist, die Daten, die dem Element zugeordnet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CB \_ getlbtextlen**](cb-getlbtextlen.md)
</dt> </dl>

 

 





