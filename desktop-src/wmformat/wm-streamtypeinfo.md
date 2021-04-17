---
title: WM/streamtypeingangs Info
description: Das WM/streamtypeinfo-Attribut enthält die Konfigurationsinformationen für den angegebenen Datenstrom in der ASF-Datei.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- WM/streamtypeingangs Info Windows Media-Format
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c410b470e9ddb4ec874325d9c1cca2839c00b1d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389061"
---
# <a name="wmstreamtypeinfo"></a>WM/streamtypeingangs Info

Das **WM/streamtypeinfo-** Attribut enthält die Konfigurationsinformationen für den angegebenen Datenstrom in der ASF-Datei.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmstreamtypeingangs Info

## <a name="data-type"></a>Datentyp

[**WM \_ \_Streamtyp \_ Info**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**WMT \_ - \_ typbinär Datei**)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für bestimmte Datenströme. Dieses Attribut kann für Stream 0 nicht abgerufen werden.

Dieses Attribut ist schreibgeschützt.

Das Metadateneditor-Objekt kann auf **WM/streamtypeinfo** zugreifen. Dies ist die einzige Möglichkeit, auf Informationen zur Datenstrom Konfiguration zuzugreifen, ohne die Datei mit dem Reader-Objekt (oder dem synchronen Reader-Objekt) zu öffnen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




