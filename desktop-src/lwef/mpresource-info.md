---
title: MPRESOURCE_INFO -Struktur (MpClient.h)
description: Ressourceninformationsstruktur.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- MPRESOURCE_INFO struktur Legacy-Windows-Umgebungsfeatures
- PMPRESOURCE_INFO strukturzeiger Legacy-Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPRESOURCE_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c399beceba4551ba3269e86f5f3c30c6967f31b4dbc5f303225e8cbfc1667df4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747423"
---
# <a name="mpresource_info-structure"></a>MPRESOURCE \_ INFO-Struktur

Ressourceninformationsstruktur.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Schema**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Ressourcenschemabezeichner, z. B. "file" oder "dir".

</dd> <dt>

**Path**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Absoluter Pfad der Ressource, basierend auf **Schema**.

</dd> <dt>

**Klasse**
</dt> <dd>

Typ: **MPRESOURCE-KLASSE \_**

</dd> <dd>

Dieses Feld wird festgelegt, wenn die Ressource als Teil der Bedrohung identifiziert wird. Sie gibt die Ressourcenklasse an, hauptsächlich konkrete und latente. Dabei kann es sich um eine Kombination dieser möglichen Werte handelt:



| Wert                                                                                                                                                                                                                                                                        | Bedeutung                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <dt>**MP \_ RESOURCE \_ CLASS \_ UNKNOWN**</dt> <dt>0x0000</dt> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <dt>**MP \_ KONKRETE \_ \_ RESSOURCENKLASSE**</dt> <dt>0X0001</dt> </dl>           | Schließen sich gegenseitig mit **MP RESOURCE CLASS LATENT \_ \_ \_ aus.**<br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <dt>**MP \_ RESOURCE \_ CLASS \_ LATENT**</dt> <dt>0x0002</dt> </dl>                 | Schließen sich mit **MP RESOURCE CLASS CONCRETE gegenseitig \_ \_ \_ aus.**<br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <dt>**MP \_ RESOURCE \_ CLASS SAMPLE FILE \_ \_ 0X0004**</dt> <dt></dt> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <dt>**MP \_ FREIGEGEBENE \_ \_ RESSOURCENKLASSE**</dt> <dt>0x0100</dt> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





