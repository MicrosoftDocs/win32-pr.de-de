---
description: Windows Portable Geräte unterstützen die folgenden Audioeigenschaften.
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: Audioeigenschaften (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Audio
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 93ddbee0eb078c1b9d5a1e7c64288e95b47e2bdb0363bf8b7b19cb773129d0ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590410"
---
# <a name="audio-properties"></a>Audioeigenschaften

Windows Portable Geräte unterstützen die folgenden Audioeigenschaften.



| Eigenschaft                         | VarType     | Beschreibung                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ WPD-AUDIOBITTIEFE \_**       | **VT \_ UI4** | Die Bittiefe des Audios.                                                                                                                                                                                        |
| **WPD \_ AUDIO \_ BITRATE**          | **VT \_ UI4** | Die Bitrate des Audios in Bits pro Sekunde.                                                                                                                                                                     |
| **\_ \_ WPD-AUDIOBLOCKAUSRICHTUNG \_** | **VT \_ UI4** | Die Blockausrichtung der Audiodatei in Bytes.                                                                                                                                                                   |
| **\_ \_ \_ WPD-AUDIOKANALANZAHL**   | **VT \_ R4**  | Die Anzahl der Kanäle in dieser Audiodatei, z. B. 1, 2 oder 5.1.                                                                                                                                              |
| **\_ \_ WPD-AUDIOFORMATCODE \_**     | **VT \_ UI4** | Die registrierte WAVE-Formatcodenummer. Eine Liste der registrierten WAVE-Formate finden Sie im Artikel [Registrierte FOURCC-Codes und WAVE-Formate](https://msdn2.microsoft.com/library/ms867195.aspx) auf der MSDN-Website. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




