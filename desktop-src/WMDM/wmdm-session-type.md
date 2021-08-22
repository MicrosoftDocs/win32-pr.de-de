---
title: WMDM_SESSION_TYPE-Enumeration
description: Der WMDM \_ SESSION \_ TYPE-Enumerationstyp definiert den Sitzungstyp.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- WMDM_SESSION_TYPE-Enumerationsfenster Media Geräte-Manager
topic_type:
- apiref
api_name:
- WMDM_SESSION_TYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4e3d3d774667ca0c7026caa05609efd69443e00c0c2e273a1e6ad0ac086aa9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055528"
---
# <a name="wmdm_session_type-enumeration"></a>WMDM \_ SESSION \_ TYPE-Enumeration

Der **WMDM \_ SESSION TYPE-Enumerationstyp \_** definiert den Sitzungstyp.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_SESSION_TYPE { 
  WMDM_SESSION_NONE,
  WMDM_SESSION_TRANSFER_TO_DEVICE,
  WMDM_SESSION_TRANSFER_FROM_DEVICE,
  WMDM_SESSION_DELETE,
  WMDM_SESSION_CUSTOM
} WMDM_SESSION_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM \_ SESSION \_ NONE**
</dt> <dd>

Die Sitzung ist nicht definiert.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**\_WMDM-SITZUNGSÜBERTRAGUNG \_ \_ AUF \_ GERÄT**
</dt> <dd>

Die Sitzung wird als Übertragung von Daten an das Gerät definiert.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**\_WMDM-SITZUNGSÜBERTRAGUNG \_ \_ VOM \_ GERÄT**
</dt> <dd>

Die Sitzung wird als Übertragung von Daten vom Gerät definiert.

</dd> <dt>

<span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**WMDM \_ SESSION \_ DELETE**
</dt> <dd>

Die Sitzung wird als Löschen von Daten definiert.

</dd> <dt>

<span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**WMDM \_ SESSION \_ CUSTOM**
</dt> <dd>

Die Sitzung wird als benutzerdefinierte Sitzung definiert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





