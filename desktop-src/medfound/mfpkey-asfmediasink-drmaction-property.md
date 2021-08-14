---
description: Gibt an, wie die ASF-Mediensenke Windows Medien-DRM angewendet werden soll.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: MFPKEY_ASFMEDIASINK_DRMACTION-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed62f62a5d03d7fe938101d9837bd8ed9bccefe69b2bf30e0566ea0b471e37f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874344"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a>MFPKEY \_ ASFMEDIASINK \_ DRMACTION-Eigenschaft

Gibt an, wie die ASF-Mediensenke Windows Medien-DRM angewendet werden soll.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Hinweise

Der Wert dieser Eigenschaft ist ein Member der [**MFSINK \_ WMDRMACTION-Enumeration.**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction)

Sie können dieses Attribut verwenden, um die ASF-Mediensenke zu konfigurieren. Die Verwendung hängt davon ab, welche Funktion Sie aufrufen, um die ASF-Mediensenke zu erstellen:

-   [**MFCreateASFMediaSink:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)Fragen Sie den abgerufenen [**POINTERMediaSink-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) für die **IPropertyStore-Schnittstelle** ab.

-   [**MFCreateASFMediaSinkActivate:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)Rufen Sie [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) für den im *pContentInfo-Parameter* angegebenen [**IMFASFContentInfo-Zeiger**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
