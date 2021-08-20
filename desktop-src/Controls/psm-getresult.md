---
title: PSM_GETRESULT-Nachricht (Prsht.h)
description: Wird von moduslosen Eigenschaftenblättern verwendet, um die informationen abzurufen, die von PropertySheet an modale Eigenschaftenblätter zurückgegeben werden. Sie können diese Nachricht explizit senden oder das PropSheet \_ GetResult-Makro verwenden.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- PSM_GETRESULT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- PSM_GETRESULT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acc8fed8cdaa1f4282c3ed066ad44f68221330fa9e79b0719db8bba1bca37f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169806"
---
# <a name="psm_getresult-message"></a>PSM \_ GETRESULT-Nachricht

Wird von moduslosen Eigenschaftenblättern verwendet, um die Informationen abzurufen, die von [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)an modale Eigenschaftenblätter zurückgegeben werden. Sie können diese Nachricht explizit senden oder das [**PropSheet \_ GetResult-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen positiven Wert zurück, andernfalls -1. Die folgenden Rückgabewerte haben eine besondere Bedeutung.



| Rückgabecode                                                                                         | Beschreibung                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ID \_ PSREBOOTSYSTEM**</dt> </dl>   | Eine Seite hat eine [**PSM \_ REBOOTSYSTEM-Nachricht**](psm-rebootsystem.md) an das Eigenschaftenblatt gesendet. Der Computer muss neu gestartet werden, damit die Änderungen des Benutzers wirksam werden.<br/> |
| <dl> <dt>**ID \_ PSRESTARTWINDOWS**</dt> </dl> | Eine Seite hat eine [**PSM \_ RESTARTWINDOWS-Nachricht**](psm-restartwindows.md) an das Eigenschaftenblatt gesendet. Windows müssen neu gestartet werden, damit die Änderungen des Benutzers wirksam werden.<br/>  |



 

## <a name="remarks"></a>Hinweise

Rufen [**Sie GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)auf, um erweiterte Fehlerinformationen abzurufen.

Der Rückgabewert für diese Nachricht ist identisch mit dem, was [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) für ein modales Eigenschaftenblatt zurückgibt.

[Version 5.80.](common-control-versions.md) Der [**PropertySheet-Rückgabewert**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) enthält unterschiedliche Informationen für modale und moduslose Eigenschaftenblätter. In einigen Fällen benötigen moduslose Eigenschaftenblätter möglicherweise die Informationen, die sie von **PropertySheet** erhalten hätten, wenn sie modal waren. Insbesondere müssen sie möglicherweise wissen, ob id \_ PSREBOOTSYSTEM oder ID \_ PSRESTARTWINDOWS zurückgegeben worden wäre.

Bei einem moduslosen Eigenschaftenblatt sollte Ihre Nachrichtenschleife [**PSM \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md) verwenden, um Nachrichten an das Eigenschaftenblattdialogfeld zu übergeben, und [**PSM \_ GETCURRENTPAGEHWND,**](psm-getcurrentpagehwnd.md) um zu bestimmen, wann das Dialogfeld zerstört werden soll. Wenn der Benutzer auf die Schaltfläche **OK** oder **Abbrechen** klickt, gibt **PSM \_ GETCURRENTPAGEHWND** **NULL** zurück. Sie können dann den Wert abrufen, den ein modales Eigenschaftenblatt von [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) erhalten hätte, indem Sie eine **PSM \_ GETRESULT-Nachricht** senden.

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn Sie den Stil des Assistenten Für Dies verwenden [**\_ (PSH-DIALOGFELDWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

