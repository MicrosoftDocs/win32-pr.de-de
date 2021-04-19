---
title: DRM_SAPLEVEL (veraltet)
description: Gibt die von der Anwendung unterstützte SAP-Ebene (Secure audiopath) an.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (veraltet) Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43711c6c394761f599271809419a46311265d8b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369357"
---
# <a name="drm_saplevel-deprecated"></a>DRM- \_ saplevel (veraltet)

\[**DRM \_ Saplevel** ist nicht mehr für die Verwendung ab Windows Vista verfügbar. Verwenden Sie stattdessen "Protected User Mode" (Puma) in der Media Foundation-Bibliothek. \]

Die DRM-Eigenschaft " **\_ saplevel** " gibt die von der Anwendung unterstützte SAP-Ebene (Secure audiopath) an.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm ( \_ saplevel)

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Dies ist eine schreibgeschützte Eigenschaft, die durch den Aufruf von [**iwmdrmreader:: setdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty)festgelegt wird. Der Wert ist eine breit Zeichen-Zeichen folgen Darstellung der SAP-Ebene, z. b. L "200". Die derzeit unterstützten Werte sind 200 und 300.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|--------------------------------|
| Ende des Supports (Client)<br/> | Windows XP<br/>          |
| Ende des Supports (Server)<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 





