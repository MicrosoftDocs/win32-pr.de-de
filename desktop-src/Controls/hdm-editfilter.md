---
title: HDM_EDITFILTER Meldung (kommstrg. h)
description: Verschiebt den Eingabefokus in das Bearbeitungsfeld, wenn eine Filter Schaltfläche den Fokus besitzt.
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- Windows-Steuerelemente für HDM_EDITFILTER Meldung
topic_type:
- apiref
api_name:
- HDM_EDITFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733c79bf747d3b55aa8dd38eb8fad8fdc83601e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742281"
---
# <a name="hdm_editfilter-message"></a>HDM- \_ EditFilter-Meldung

Verschiebt den Eingabefokus in das Bearbeitungsfeld, wenn eine Filter Schaltfläche den Fokus besitzt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein-Wert, der die zu bearbeitende Spalte angibt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Flag, das angibt, wie die Bearbeitungs Änderungen des Benutzers behandelt werden. Verwenden Sie dieses Flag, um anzugeben, was geschehen soll, wenn der Benutzer den Filter bearbeitet, wenn die Nachricht gesendet wird.



| Wert                                                                                                                                      | Bedeutung                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt></dt><dt> **True**</dt> </dl>  | Verwerfen Sie die vom Benutzer vorgenommenen Änderungen. <br/> |
| <dl> <dt></dt><dt> **False**</dt> </dl> | Akzeptieren Sie die vom Benutzer vorgenommenen Änderungen. <br/>  |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zurück. Das **LRESULT** wird in eine ganze Zahl umgewandelt, die **true**(1) oder **false**(0) angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**HDM- \_ ClearFilter**](hdm-clearfilter.md)
</dt> </dl>

 

 





