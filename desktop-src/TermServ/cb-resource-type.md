---
title: CB_RESOURCE_TYPE-Enumeration (cbclient. h)
description: Gibt den Typ der Ressource an, mit der die eingehende Verbindung eine Verbindung herstellt.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- CB_RESOURCE_TYPE Enumeration Remotedesktopdienste
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
ms.openlocfilehash: 60561e4af54c6d27288d8df311693d51c0b9fc77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740584"
---
# <a name="cb_resource_type-enumeration"></a>CB \_ - \_ Ressourcentyp Enumeration

Gibt den Typ der Ressource an, mit der die eingehende Verbindung eine Verbindung herstellt. Diese Enumeration wird mit der [**CB- \_ Verbindungs \_ Informations**](cb-connection-info.md) Struktur verwendet.

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

<span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**CB- \_ Ressource nicht \_ definiert**
</dt> <dd>

Der Ressourcentyp ist nicht definiert.

</dd> <dt>

<span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**CB- \_ Ressourcen \_ Sitzung**
</dt> <dd>

Die Ressource ist eine Remote Sitzung.

</dd> <dt>

<span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**CB- \_ Ressourcen- \_ VM**
</dt> <dd>

Die Ressource ist ein virtueller Computer.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CB- \_ Verbindungs \_ Informationen**](cb-connection-info.md)
</dt> </dl>

 

 





