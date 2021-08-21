---
title: IRDVTaskPlugin-Plug-InName-Eigenschaft (Tspubplugincom.h)
description: Enthält den Anzeigenamen des Task-Agents.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- PluginName-Eigenschaft Remotedesktopdienste
- PluginName-Eigenschaft Remotedesktopdienste , IRDVTaskPlugin-Schnittstelle
- IRDVTaskPlugin-Schnittstelle Remotedesktopdienste , PluginName-Eigenschaft
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.PluginName
- IRDVTaskPlugin.get_PluginName
api_location:
- tspubplugincom.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078934c8f19085bf233df78501798a8416ceadf7ba6a0b663cb14b8a8c46b223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129331"
---
# <a name="irdvtaskpluginpluginname-property"></a>IRDVTaskPlugin::P luginName-Eigenschaft

Enthält den Anzeigenamen des Task-Agents. Dieser Name wird nur zu Protokollierungszwecken verwendet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Anzeigename des Task-Agents.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                           |
| Header<br/>                   | <dl> <dt>Tspubplugincom.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





