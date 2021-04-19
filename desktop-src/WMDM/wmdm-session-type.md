---
title: WMDM_SESSION_TYPE-Enumeration
description: Der Enumerationstyp für den WMDM- \_ Sitzungstyp \_ definiert den Sitzungstyp.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- Device Manager der WMDM_SESSION_TYPE-Enumeration Windows Media
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
ms.openlocfilehash: 84322986266143e5ff4ecc469c56504f29de9e3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370978"
---
# <a name="wmdm_session_type-enumeration"></a>WMDM \_ - \_ Sitzungstyp-Enumeration

Der Enumerationstyp für den **WMDM- \_ \_ Sitzungstyp** definiert den Sitzungstyp.

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

<span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM- \_ Sitzung " \_ None"**
</dt> <dd>

Die Sitzung ist nicht definiert.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**WMDM- \_ Sitzungs \_ Übertragung \_ an \_ Gerät**
</dt> <dd>

Die Sitzung ist so definiert, dass Daten an das Gerät übertragen werden.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**WMDM- \_ Sitzungs \_ Übertragung \_ von \_ Gerät**
</dt> <dd>

Die Sitzung ist so definiert, dass Daten vom Gerät übertragen werden.

</dd> <dt>

<span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**Löschen der WMDM- \_ Sitzung \_**
</dt> <dd>

Die Sitzung wird als Löschen von Daten definiert.

</dd> <dt>

<span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**benutzerdefinierte WMDM- \_ Sitzung \_**
</dt> <dd>

Die Sitzung wird als benutzerdefinierte Sitzung definiert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





