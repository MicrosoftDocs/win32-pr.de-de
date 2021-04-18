---
description: Tragbare Windows-Geräte unterstützen die folgenden Audioeigenschaften.
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: Audioeigenschaften (portabledevice. h)
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
ms.openlocfilehash: 1bdab201fc987d5bc1aff3638fbb57358115fdce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357995"
---
# <a name="audio-properties"></a>Audioeigenschaften

Tragbare Windows-Geräte unterstützen die folgenden Audioeigenschaften.



| Eigenschaft                         | VarType     | BESCHREIBUNG                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ - \_ \_ audiobittiefe**       | **VT \_ UI4** | Die Bittiefe der Audiodatei.                                                                                                                                                                                        |
| **WPD \_ - \_ Audiobitrate**          | **VT \_ UI4** | Die Bitrate der Audiodaten (in Bits pro Sekunde).                                                                                                                                                                     |
| **WPD \_ - \_ Audioblock \_ Ausrichtung** | **VT \_ UI4** | Die Block Ausrichtung der Audiodatei in Bytes.                                                                                                                                                                   |
| **Anzahl von WPD \_ - \_ Audiokanälen \_**   | **VT \_ R4**  | Die Anzahl der Kanäle in dieser Audiodatei, z. b. 1, 2 oder 5,1.                                                                                                                                              |
| **WPD \_ - \_ \_ audioformatcode**     | **VT \_ UI4** | Die registrierte Wave-Format-Codenummer. Eine Auflistung registrierter Wellen Formate finden Sie im Artikel [registrierte FOURCC Codes und Wave Formats](https://msdn2.microsoft.com/library/ms867195.aspx) auf der MSDN-Website. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




