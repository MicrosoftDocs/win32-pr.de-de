---
title: EM_FILELINEFROMCHAR Meldung (kommstrg. h)
description: Ruft den Index der Zeile ab, die den angegebenen Zeichen Index in einem mehrzeiligen Bearbeitungs Steuerelement enthält, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- Windows-Steuerelemente für EM_FILELINEFROMCHAR Meldung
topic_type:
- apiref
api_name:
- EM_FILELINEFROMCHAR
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a083d7e12822eacfb1e29a7d4bfd2ea705f2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477331"
---
# <a name="em_filelinefromchar-message"></a>EM \_ filelinefromchar-Meldung

Ruft den Index der Zeile ab, die den angegebenen Zeichen Index in einem mehrzeiligen Bearbeitungs Steuerelement enthält, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden. Ein Zeichen Index ist der null basierte Index des Zeichens vom Anfang des Bearbeitungs Steuer Elements.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Zeichen Index des Zeichens, das in der Zeile enthalten ist, deren Zahl abgerufen werden soll. Wenn dieser Parameter-1 ist, ruft **EM \_ filelinefromchar** entweder die Zeilennummer der aktuellen Zeile (die Zeile mit der Einfügemarke) oder, wenn eine Auswahl vorliegt, die Zeilennummer der Zeile ab, die den Anfang der Auswahl enthält.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die null basierte Zeilennummer der Zeile, die den von *wParam* angegebenen Zeichen Index enthält, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10, 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2019 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ filelineingedex**](em-filelineindex.md)
</dt> </dl>

 

 





