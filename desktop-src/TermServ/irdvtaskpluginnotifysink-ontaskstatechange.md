---
title: Undvtaskpluginnotifysink ontaskstatechange-Methode
description: Wird verwendet, um den Agent zu benachrichtigen, dass sich der Zustand einer Aufgabe geändert hat.
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- Ontaskstatechange-Methode Remotedesktopdienste
- Ontaskstatechange-Methode Remotedesktopdienste, undvtaskpluginnotifysink-Schnittstelle
- Undvtaskpluginnotifysink-Schnittstelle Remotedesktopdienste, ontaskstatechange-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3e3acf1a2d47b1721ef90554f7a11714c02e6df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342667"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a>Undvtaskpluginnotifysink:: ontaskstatechange-Methode

Wird verwendet, um den Agent zu benachrichtigen, dass sich der Zustand einer Aufgabe geändert hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnTaskStateChange(
  [in] BSTR            bstrIdentifier,
  [in] RDV_TASK_STATUS status
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstridentifier* \[ in\]
</dt> <dd>

Typ: **BSTR**

Der Bezeichner des Tasks. Dies ist der Bezeichner, der an die [**Starttask**](irdvtaskplugin-starttask.md) -Methode übermittelt wird.

</dd> <dt>

*Status* \[ in\]
</dt> <dd>

Typ: **[ **RDV- \_ Task \_ Status**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**

Ein Wert der [**RDV- \_ aufgabenstatusenumeration \_**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) , die den neuen Zustand der Aufgabe angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RDV- \_ Task \_ Status**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[**"Undvtaskpluginnotifysink"**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





