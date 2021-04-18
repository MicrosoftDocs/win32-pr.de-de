---
title: Is_Protected
description: Das is \_ protected-Attribut ist ein Attribut auf Dateiebene, das angibt, ob der Inhalt in der Datei durch Digital Rights Management (DRM) geschützt wurde.
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected Windows Media-Format
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ec24eb3e805f93bfd46e40954ce64da73ed774
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338436"
---
# <a name="is_protected"></a>Ist \_ geschützt

Das **is \_ Protected** -Attribut ist ein Attribut auf Dateiebene, das angibt, ob der Inhalt in der Datei durch Digital Rights Management (DRM) geschützt wurde.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmprotected

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ bool**

## <a name="remarks"></a>Bemerkungen

Dies ist ein codiertes Attribut. Wenn Sie diese Eigenschaft abrufen, werden dieselben Informationen wie beim Aufrufen von [**wmiscontentprotected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)bereitstellt.

Dieses Attribut kann nicht auf Dateiebene dupliziert werden. Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und gibt seine normale Bedeutung nicht an die Objekte des Windows Media Format SDK aus.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




