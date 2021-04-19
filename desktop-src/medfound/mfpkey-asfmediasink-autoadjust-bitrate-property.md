---
description: Gibt an, ob die ASF-Medien Senke die Bitrate automatisch anpasst.
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d22463f477eb5abc1bb84254ad312427ecef52
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106373423"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a>Mfpkey \_ asfmediasink \_ autoanpassung- \_ Bitrate (Eigenschaft)

Gibt an, ob die ASF-Medien Senke die Bitrate automatisch anpasst.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**Variant \_ bool**

VT \_ bool

**Boolesche Werte**



## <a name="remarks"></a>Bemerkungen

Wenn der Wert dieser Eigenschaft Variant true ist \_ , passt die ASF-Medien Senke die Bitrate des ASF-Inhalts automatisch als Reaktion auf die Merkmale der zu multipleckenden Streams an.

Diese Eigenschaft wirkt sich darauf aus, wie sich die ASF-Medien Senke verhält, wenn ein Stream den "Leaky Bucket"-Parameter der Senke überschreitet



| Wert              | Verhalten                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **Variant \_ true**  | Die ASF-Medien Senke passt die Bitrate des ASF-Inhalts automatisch als Reaktion auf die Merkmale der zu multipleckenden Streams an. |
| **Variant \_ false** | Die ASF-Medien Senke verwendet den von der Anwendung bereitgestellten Stream-Bitrate-Wert.                                                                |



 

Der Standardwert ist **Variant \_ false**.

Legen Sie diese Eigenschaft fest, wenn Sie die ASF-Medien Senke konfigurieren. Die Verwendung hängt von der Funktion ab, die Sie zum Erstellen der ASF-Medien Senke aufzurufen:

-   [**Mfkreateasfmediasink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): fragt den abgerufenen [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) -Zeiger für die **IPropertyStore** -Schnittstelle ab.

-   [**Mfkreateasfmediasinkaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Aufrufen von [**imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) für den [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Zeiger, der im *pcontentinfo* -Parameter angegeben ist.

Wenn diese Eigenschaft auf Variant true festgelegt wird, \_ legt die ASF-Medien Senke das Flag für die **Automatische Anpassung der mfasf \_ Multiplexer- \_ \_ Bitrate** für den ASF Multiplexer fest. Weitere Informationen finden Sie unter [**imfasf Multiplexer:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).

Weitere Informationen zum "Leaky Bucket"-Konzept finden Sie im Thema "The Leaky Bucket Buffer Model" in der Dokumentation zum Windows Media-Format-SDK.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**MF \_ asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[**MF \_ asfstreamconfig \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




