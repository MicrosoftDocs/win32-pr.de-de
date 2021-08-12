---
title: IRDVTaskPlugin Initialize-Methode
description: Wird aufgerufen, um den Task-Agent zu initialisieren.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Initialize method Remotedesktopdienste
- Initialisieren der Methode Remotedesktopdienste , IRDVTaskPlugin-Schnittstelle
- IRDVTaskPlugin-Schnittstelle Remotedesktopdienste , Initialize-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14f4a002a0b33e403c02dba74385edd21e211fb27bcfb144c7a9ddc080a40fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606103"
---
# <a name="irdvtaskplugininitialize-method"></a>IRDVTaskPlugin::Initialize-Methode

Wird aufgerufen, um den Task-Agent zu initialisieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNotifySink* \[ In\]
</dt> <dd>

Typ: **[ **IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)\***

Ein Zeiger auf eine [**IRDVTaskPluginNotifySink-Schnittstelle,**](irdvtaskpluginnotifysink.md) die der Task-Agent für die Kommunikation mit dem Trigger-Agent verwendet. Sie müssen diese Schnittstelle freigeben, wenn sie nicht mehr benötigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





