---
title: Methode "undvtaskplugin Initialize"
description: Wird aufgerufen, um den Task-Agent zu initialisieren.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Initialize-Methode Remotedesktopdienste
- Initialize-Methode Remotedesktopdienste, undvtaskplugin-Schnittstelle
- Undvtaskplugin-Schnittstelle Remotedesktopdienste, Initialize-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9530be7334e1f3fefa7f73007334e448362a95ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391661"
---
# <a name="irdvtaskplugininitialize-method"></a>Undvtaskplugin:: Initialize-Methode

Wird aufgerufen, um den Task-Agent zu initialisieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnotifysink* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[**undvtaskpluginnotifysink**](irdvtaskpluginnotifysink.md) \** _

Ein Zeiger auf eine [_ *undvtaskpluginnotifysink* *](irdvtaskpluginnotifysink.md) -Schnittstelle, die der Task-Agent für die Kommunikation mit dem Auslöse-Agent verwendet. Sie müssen diese Schnittstelle freigeben, wenn Sie nicht mehr benötigt wird.

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

[**"Undvtaskplugin"**](irdvtaskplugin.md)
</dt> </dl>

 

 





