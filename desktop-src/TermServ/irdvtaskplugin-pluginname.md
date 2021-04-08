---
title: "\"Undvtaskplugin PluginName\"-Eigenschaft (tspubplugincom. h)"
description: Enthält den anzeigen amen des Task-Agents.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- PluginName-Eigenschaft Remotedesktopdienste
- PluginName-Eigenschaft Remotedesktopdienste, undvtaskplugin-Schnittstelle
- Undvtaskplugin-Schnittstelle Remotedesktopdienste, PluginName-Eigenschaft
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
ms.openlocfilehash: 0262472e37a8ff3e5b9bb153d2e94f4e52029b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742073"
---
# <a name="irdvtaskpluginpluginname-property"></a>Undvtaskplugin::P luginname-Eigenschaft

Enthält den anzeigen amen des Task-Agents. Dieser Name wird nur zu Protokollierungs Zwecken verwendet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Anzeige Name des Task-Agents.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                           |
| Header<br/>                   | <dl> <dt>Tspubplugincom. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Undvtaskplugin"**](irdvtaskplugin.md)
</dt> </dl>

 

 





