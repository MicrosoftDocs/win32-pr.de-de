---
title: CB_SETEDITSEL Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ seteditsel-Meldung, um Zeichen im Bearbeitungs Steuerelement eines Kombinations Felds auszuwählen.
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- Windows-Steuerelemente für CB_SETEDITSEL Meldung
topic_type:
- apiref
api_name:
- CB_SETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54e09697e266b4e0c4260104e90f454a5e3edfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476632"
---
# <a name="cb_seteditsel-message"></a>CB-nach \_ richten-Nachricht

Eine Anwendung sendet eine **CB \_ seteditsel** -Meldung, um Zeichen im Bearbeitungs Steuerelement eines Kombinations Felds auszuwählen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) von *LPARAM* gibt die Anfangsposition an. Wenn das **LoWord** -1 ist, wird die Auswahl ggf. entfernt.

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) von *LPARAM* gibt die Endposition an. Wenn das **HIWORD** -1 ist, wird der gesamte Text von der Anfangsposition bis zum letzten Zeichen im Bearbeitungs Steuerelement ausgewählt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert " **true**". Wenn die Nachricht an ein Kombinations Feld mit dem Format " [**CBS \_ DropDownList**](combo-box-styles.md) " gesendet wird, ist es CB \_ Err.

## <a name="remarks"></a>Bemerkungen

Die Positionen sind NULL basiert. Das erste Zeichen des Bearbeitungs Steuer Elements befindet sich an der Nullposition. Das erste Zeichen nach dem letzten ausgewählten Zeichen befindet sich an der Endposition. Wenn Sie z. b. die ersten vier Zeichen des Bearbeitungs Steuer Elements auswählen möchten, verwenden Sie die Startposition 0 und die Endposition 4.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**CB \_ geteditsel**](cb-geteditsel.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Makelparam**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

