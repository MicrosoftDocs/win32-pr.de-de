---
title: Is_Protected
description: Das Is Protected-Attribut ist ein Attribut auf Dateiebene, das an gibt, ob der Inhalt in der Datei mithilfe von \_ Digital Rights Management (DRM) geschützt wurde.
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected windows Media Format
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0759dfc781409a1331403c3b02c2645f6ad843925584eab2a55f31a0c8d31af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847417"
---
# <a name="is_protected"></a>Ist \_ geschützt

Das **Is \_ Protected-Attribut** ist ein Attribut auf Dateiebene, das an gibt, ob der Inhalt in der Datei mithilfe von Digital Rights Management (DRM) geschützt wurde.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMProtected

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ BOOL**

## <a name="remarks"></a>Hinweise

Dies ist ein codiertes Attribut. Das Abrufen dieser Eigenschaft stellt die gleichen Informationen wie das Aufrufen von [**WMIsContentProtected zur Verfügung.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)

Dieses Attribut kann nicht auf Dateiebene dupliziert werden. Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und vermittelt den Objekten des Windows Media Format SDK nicht seine normale Bedeutung.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




