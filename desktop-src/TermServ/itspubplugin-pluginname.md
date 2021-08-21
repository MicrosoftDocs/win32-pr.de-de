---
title: ItsPubPlugin pluginName-Eigenschaft
description: Ruft den Namen des Plug-Ins ab.
ms.assetid: c1ea46b6-fac6-4140-a278-cb04ee9af739
ms.tgt_platform: multiple
keywords:
- pluginName-Eigenschaft Remotedesktopdienste
- pluginName-Eigenschaft Remotedesktopdienste , ItsPubPlugin-Schnittstelle
- ItsPubPlugin-Schnittstelle Remotedesktopdienste , pluginName-Eigenschaft
topic_type:
- apiref
api_name:
- ItsPubPlugin.pluginName
- ItsPubPlugin.get_pluginName
api_location:
- Cpubplugin.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa1cd3103e901255a6226db3e128e81bb17c02e6b586a48ca434ed44932861c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128639"
---
# <a name="itspubpluginpluginname-property"></a>ItsPubPlugin::p luginName-Eigenschaft

Ruft den Namen des Plug-Ins ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_pluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine **BSTR-Variable,** um den Namen des Plug-Ins zu empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                         |
| Idl<br/>                      | <dl> <dt>Cpubplugin.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ItsPubPlugin**](/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin)
</dt> </dl>

 

 





