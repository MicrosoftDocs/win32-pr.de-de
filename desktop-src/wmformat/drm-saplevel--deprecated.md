---
title: DRM_SAPLEVEL (veraltet)
description: Gibt die sap-Ebene (Secure Audio Path) an, die von Ihrer Anwendung unterstützt wird.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (veraltet) Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80b43cfcf0c89283237f8ff2d3e4f8612050296d7462f54890c3efa908fa9be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930890"
---
# <a name="drm_saplevel-deprecated"></a>DRM \_ SAPLEVEL (veraltet)

\[**DRM \_ SAPLEVEL** ist ab Windows Vista nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen Protected User Mode Audio (CSV) in der bibliothek Media Foundation. \]

Die **\_ DRM-Eigenschaft SAPLEVEL** gibt den sicheren Audiopfad (SECURE Audio Path, SAP) an, der von Ihrer Anwendung unterstützt wird.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM \_ SAPLEVEL

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYPZEICHENFOLGE**

## <a name="remarks"></a>Hinweise

Dies ist eine Schreibeigenschaft, die durch Aufrufen von [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty)festgelegt wird. Der Wert ist eine Breitzeichen-Zeichenfolgendarstellung der SAP-Ebene, z.B. L"200". Die aktuellen unterstützten Werte sind 200 und 300.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|--------------------------------|
| Ende des Supports (Client)<br/> | Windows XP<br/>          |
| Ende des Supports (Server)<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 





