---
title: CB_RESOURCE_TYPE-Enumeration (Cbclient.h)
description: Gibt den Typ der Ressource an, mit der die eingehende Verbindung eine Verbindung herstellt.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- CB_RESOURCE_TYPE Enumerations-Remotedesktopdienste
topic_type:
- apiref
api_name:
- CB_RESOURCE_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63dfce0f575147233735dd943645eb51c26141cacaaa61c044698b29b8d118e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139113"
---
# <a name="cb_resource_type-enumeration"></a>CB \_ RESOURCE \_ TYPE-Enumeration

Gibt den Typ der Ressource an, mit der die eingehende Verbindung eine Verbindung herstellt. Diese Enumeration wird mit der [**CB \_ CONNECTION \_ INFO-Struktur**](cb-connection-info.md) verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**\_CB-RESSOURCE \_ UNDEFINED**
</dt> <dd>

Der Ressourcentyp ist nicht definiert.

</dd> <dt>

<span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**\_ \_ CB-RESSOURCENSITZUNG**
</dt> <dd>

Die Ressource ist eine Remotesitzung.

</dd> <dt>

<span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**\_CB-RESSOURCEN-VM \_**
</dt> <dd>

Die Ressource ist ein virtueller Computer.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_ \_ CB-VERBINDUNGSINFORMATIONEN**](cb-connection-info.md)
</dt> </dl>

 

 





