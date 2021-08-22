---
description: Gibt den Aktionstyp eines Endpunktvorgangs zur Verhinderung von Datenverlust (Data Loss Prevention, DLP) an.
title: DlpActionType-Enumeration (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpActionType
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 5b7066eec7832ba0b76dee38e6483e0bfcfcfb05fdb8448ee7b3a91e701069fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976650"
---
# <a name="dlpactiontype-enumeration"></a>DlpActionType-Enumeration

Gibt den Aktionstyp eines Endpunktvorgangs zur Verhinderung von Datenverlust (Data Loss Prevention, DLP) an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
```


## <a name="constants"></a>Konstanten

<dl> <dt>

*DlpActionTypeCopyToRemovableMedia*
</dt> <dd>

Ein Kopiervorgang auf Wechselmedien.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCopyToNetworkShare*
</dt> <dd>

Ein Kopiervorgang in einen freigegebenen Netzwerkordner.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCopyToClipboard*
</dt> <dd>

Ein Kopiervorgang in die Zwischenablage.

</dd> </dl>

<dl> <dt>

*DlpActionTypePrint*
</dt> <dd>

Ein Druckvorgang.

</dd> </dl>


<dl> <dt>

*DlpActionTypeScreenClip*
</dt> <dd>

Ein Bildschirmaufnahmevorgang.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByUnallowedApp*
</dt> <dd>

Ein Vorgang, der von einer nicht zulässigen App ausgeführt wird.

</dd> </dl>


<dl> <dt>

*DlpActionTypeCloudAppEgress*
</dt> <dd>

Ein Vorgang, der auf einen Cloudstandort ausgerichtet ist.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByBluetoothApp*
</dt> <dd>

Ein Vorgang, der den Zugriff über eine Bluetooth-App einschließt.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByRDPApp*
</dt> <dd>

Ein Vorgang, der den Zugriff über einen Remotedesktop einschließt.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCount*
</dt> <dd>

Der Höchstwert der Enumeration.

</dd> </dl>
 

## <a name="remarks"></a>Hinweise

Werte aus dieser Enumeration werden von der [DLP_APP_OP_ENLIGHTENED_LEVEL-Struktur](endpointdlp-dlp_app_op_enlightened_level.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |

