---
title: WM/StreamTypeInfo
description: Das WM/StreamTypeInfo-Attribut enthält die Konfigurationsinformationen für den angegebenen Stream in der ASF-Datei.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- WM/StreamTypeInfo windows Media Format
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb40926d5ecba3aea2c7f2db64850152c66a25861d4422fddf04670c76d8148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698272"
---
# <a name="wmstreamtypeinfo"></a>WM/StreamTypeInfo

Das **WM/StreamTypeInfo-Attribut** enthält die Konfigurationsinformationen für den angegebenen Stream in der ASF-Datei.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMStreamTypeInfo

## <a name="data-type"></a>Datentyp

[**WM \_ \_ \_ STREAMTYPINFORMATIONEN**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**\_ WMT-TYP \_ BINARY**)

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für bestimmte Datenströme. Sie können dieses Attribut für Stream 0 nicht abrufen.

Dieses Attribut ist schreibgeschützt.

**Auf WM/StreamTypeInfo** kann über das Metadaten-Editor-Objekt zugegriffen werden. Dies ist die einzige Möglichkeit, auf Datenstromkonfigurationsinformationen zuzugreifen, ohne die Datei mit dem Readerobjekt (oder dem synchronen Readerobjekt) zu öffnen.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




