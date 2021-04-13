---
title: PSM_GETRESULT Meldung (prsht. h)
description: Wird von nicht modalen Eigenschaften Blättern zum Abrufen der Informationen verwendet, die von PropertySheet an modale Eigenschaften Blätter zurückgegeben werden. Sie können diese Nachricht explizit senden oder das propsheet \_ GetResult-Makro verwenden.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- Windows-Steuerelemente für PSM_GETRESULT Meldung
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
ms.openlocfilehash: d41609f625cbd3938fa78e9a2f91ab70168ecc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518530"
---
# <a name="psm_getresult-message"></a>PSM \_ GetResult-Nachricht

Wird von nicht modalen Eigenschaften Blättern zum Abrufen der Informationen verwendet, die von [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)an modale Eigenschaften Blätter zurückgegeben werden. Sie können diese Nachricht explizit senden oder das [**propsheet \_ GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) -Makro verwenden.

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

Gibt einen positiven Wert zurück, wenn erfolgreich, andernfalls-1. Die folgenden Rückgabewerte haben eine besondere Bedeutung.



| Rückgabecode                                                                                         | Beschreibung                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ID \_ psrebootsystem**</dt> </dl>   | Eine Seite hat eine [**PSM- \_ rebootsystemmeldung**](psm-rebootsystem.md) an das Eigenschaften Blatt gesendet. Der Computer muss neu gestartet werden, damit die Änderungen des Benutzers wirksam werden.<br/> |
| <dl> <dt>**ID \_ psrestartwindows**</dt> </dl> | Eine Seite hat eine [**PSM- \_ restartwindows**](psm-restartwindows.md) -Meldung an das Eigenschaften Blatt gesendet. Windows muss neu gestartet werden, damit die Änderungen des Benutzers wirksam werden.<br/>  |



 

## <a name="remarks"></a>Bemerkungen

Um erweiterte Fehlerinformationen abzurufen, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)auf.

Der Rückgabewert für diese Nachricht ist identisch mit dem, was [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) für ein modales Eigenschaften Blatt zurückgibt.

[Version 5,80.](common-control-versions.md) Der Rückgabewert [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) enthält unterschiedliche Informationen für modale und nicht modale Eigenschaften Blätter. In einigen Fällen benötigen nicht modale Eigenschaften Blätter möglicherweise die Informationen, die Sie von **PropertySheet** erhalten haben, wenn Sie Modal waren. Insbesondere müssen Sie möglicherweise wissen, ob ID \_ psrebootsystem oder ID \_ psrestartwindows zurückgegeben worden wäre.

Für ein nicht modalem Eigenschaften Blatt sollte die Nachrichten Schleife [**PSM \_ IsDialogMessage**](psm-isdialogmessage.md) verwenden, um Nachrichten an das Eigenschaften Blatt zu übergeben, und [**PSM \_ getcurrentpagehwnd**](psm-getcurrentpagehwnd.md) , um zu bestimmen, wann das Dialogfeld zerstört werden soll. Wenn der Benutzer auf die Schaltfläche **OK** oder **Abbrechen** klickt, gibt **PSM \_ getcurrentpagehwnd** den Wert **null** zurück. Sie können dann den Wert abrufen, den ein modales Eigenschaften Blatt von [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) erhalten hätte, indem Sie eine **PSM \_ GetResult** -Nachricht senden.

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

