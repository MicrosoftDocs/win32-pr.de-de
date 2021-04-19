---
title: WMDM_STORAGE_ENUM_MODE-Enumeration
description: Der Enumerationstyp der WMDM- \_ Speicher \_ \_ Enumeration definiert, wie der Inhalt des Speichers aufgelistet werden soll. Diese Enumeration wird von IWMDMStorage3 tenumpreference verwendet.
ms.assetid: 38293e54-92e4-4f0a-bdea-5dc684a9548b
keywords:
- Device Manager der WMDM_STORAGE_ENUM_MODE-Enumeration Windows Media
topic_type:
- apiref
api_name:
- WMDM_STORAGE_ENUM_MODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d886ade00289e655ae3323a70d01be96a09852b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369946"
---
# <a name="wmdm_storage_enum_mode-enumeration"></a>\_ \_ \_ Enumeration des enumerationsmodus für WMDM-Speicher

Der Enumerationstyp der **WMDM- \_ Speicher \_ \_** Enumeration definiert, wie der Inhalt des Speichers aufgelistet werden soll. Diese Enumeration wird von [**IWMDMStorage3:: abtenumpreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference)verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_STORAGE_ENUM_MODE { 
  ENUM_MODE_RAW,
  ENUM_MODE_USE_DEVICE_PREF,
  ENUM_MODE_METADATA_VIEWS
} WMDM_STORAGE_ENUM_MODE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**Enum- \_ Modus \_ RAW**
</dt> <dd>

Listet den Inhalt des Speichers auf, so wie er im Dateisystem des Speichers angeordnet ist.

**der Enum- \_ Modus \_ verwendet die Geräte- \_ \_ Pref.**

Listet den Inhalt des Speichers auf der Grundlage der Geräteeinstellung auf, wie vom *UseMetadataViews* -Geräteparameter angegeben.

**metadatenansichten im Enum- \_ Modus \_ \_**

Listet den Inhalt des Speichers auf, indem der Inhalt basierend auf einer Metadatenansicht organisiert wird.

</dd> <dt>

<span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**der Enum- \_ Modus \_ verwendet die Geräte- \_ \_ Pref.**
</dt> <dd>

Listet den Inhalt des Speichers auf der Grundlage der Geräteeinstellung auf, wie vom *UseMetadataViews* -Geräteparameter angegeben.

**metadatenansichten im Enum- \_ Modus \_ \_**

Listet den Inhalt des Speichers auf, indem der Inhalt basierend auf einer Metadatenansicht organisiert wird.

</dd> <dt>

<span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**metadatenansichten im Enum- \_ Modus \_ \_**
</dt> <dd>

Listet den Inhalt des Speichers auf, indem der Inhalt basierend auf einer Metadatenansicht organisiert wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





