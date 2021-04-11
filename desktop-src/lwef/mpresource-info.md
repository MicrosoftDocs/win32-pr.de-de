---
title: MPRESOURCE_INFO Struktur (mpclient. h)
description: Struktur der Ressourcen Informationen.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- MPRESOURCE_INFO Struktur Funktionen der Legacy-Windows-Umgebung
- PMPRESOURCE_INFO Struktur Zeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: dcac6552e0a0060df1bd6a0464fbb8f610395131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956736"
---
# <a name="mpresource_info-structure"></a>Mpresource- \_ Informationsstruktur

Struktur der Ressourcen Informationen.

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

**Schrift**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Ressourcen Schema Bezeichner, z. b. "file" oder "dir".

</dd> <dt>

**Pfad**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Absoluter Pfad der Ressource, basierend auf dem **Schema**.

</dd> <dt>

**Klasse**
</dt> <dd>

Type: **mpresource- \_ Klasse**

</dd> <dd>

Dieses Feld wird festgelegt, wenn die Ressource als Teil der Bedrohung identifiziert wird. Es gibt die Ressourcen Klasse an, hauptsächlich konkrete und latente. Dies kann eine Kombination der folgenden möglichen Werte sein:



| Wert                                                                                                                                                                                                                                                                        | Bedeutung                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <dt>**MP \_ Ressourcen \_ Klasse \_ unbekannt**</dt> <dt>0x0000</dt> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <dt>**MP \_ Ressourcen \_ Klasse \_ konkret**</dt> <dt>0x0001</dt> </dl>           | Schließen Sie sich gegenseitig mit der **MP- \_ Ressourcen \_ Klasse \_** aus<br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <dt>**MP \_ Ressourcen \_ Klasse, \_ LATENT**</dt> <dt>0x0002</dt> </dl>                 | Schließen Sie sich gegenseitig mit **MP- \_ Ressourcen \_ Klasse \_** aus.<br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <dt>**MP \_ Ressourcen \_ Klassen- \_ Beispiel \_ Datei**</dt> <dt>0x0004</dt> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <dt>**MP \_ Ressourcen \_ Klasse \_ Shared**</dt> <dt>0x0100</dt> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





