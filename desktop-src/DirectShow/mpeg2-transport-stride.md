---
description: Die MPEG2 \_ \_ -Transport Stride-Struktur beschreibt das Format von MPEG-2-Transportstream-Paketen (TS).
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: MPEG2_TRANSPORT_STRIDE-Struktur (bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MPEG2_TRANSPORT_STRIDE
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 4a0cdc21bdd8c320728da0c0af8c0af023de68eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359250"
---
# <a name="mpeg2_transport_stride-structure"></a>MPEG2- \_ Transport- \_ Stride-Struktur

Die `MPEG2_TRANSPORT_STRIDE` -Struktur beschreibt das Format von MPEG-2-Transportdaten Strom-Paketen (TS). Diese Struktur ermöglicht Transport Datenströme, bei denen die 188-Byte-Transport Pakete nicht zusammenhängend sind. Im Rahmen dieser Dokumentation werden solche Pakete als *Stride-Pakete* bezeichnet.

Stride-Pakete werden durch den folgenden Medientyp identifiziert:



|             |                                        |
|-------------|----------------------------------------|
| Haupttyp  | MediaType- \_ Stream                      |
| Subtype     | Mediasubtype \_ MPEG2- \_ Transport \_ Stride |
| Formattyp | Nicht \_ formatieren                           |



 

Der Format Block (**pbformat**) ist optional. Wenn der Format Block eingeschlossen ist, muss er mit einer " **MPEG2- \_ Transport \_ Stride** "-Struktur beginnen. Diese Struktur definiert das Layout des Transport Pakets innerhalb des STRIDE-Pakets. Wenn der Format Block **null** ist, wird davon ausgegangen, dass die Pakete einen Satz von Standardwerten verwenden. Weitere Informationen finden Sie im Abschnitt "Hinweise".

## <a name="syntax"></a>Syntax


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a>Member

<dl> <dt>

**dwOffset**
</dt> <dd>

Gibt den Offset (in Bytes) vom Anfang des Pakets bis zum ersten Byte des eingebetteten Transport Pakets an. Der Wert muss zwischen 0 (null) und `(dwStride - dwPacketLength)` einschließlich liegen.

</dd> <dt>

**dwpacketlength**
</dt> <dd>

Gibt die Länge des eingebetteten Transport Pakets in Bytes an. Bei Standard-MPEG-2-Transport Paketen muss der Wert 188 Bytes betragen.

</dd> <dt>

**dwstride**
</dt> <dd>

Gibt die Länge des gesamten Stride-Pakets in Bytes an. Der Wert muss mindestens lauten `(dwOffset + dwPacketLength)` .

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das folgende Diagramm veranschaulicht die Beziehungen zwischen den Strukturmembern.

![MPEG-2-Stride-Paket](images/mpeg2-stride-packet.png)

Eingabepuffer, die Multiplex Stride-Pakete enthalten, weisen einige Einschränkungen auf:

-   Stride-Pakete müssen zusammenhängend innerhalb des Puffers verpackt werden.
-   Es können keine Bytes dem ersten Stride-Paket vorangestellt sein, oder Sie können dem letzten Stride-Paket folgen.
-   Eine ganzzahlige Anzahl von Stride-Paketen muss in den Puffer passen. Das heißt, die Pufferlänge% dwstride ist gleich 0 (null).

Es gibt keine Einschränkung für die Anzahl von Stride-Paketen pro Puffer.

Wenn der Medientyp keinen Format Block enthält (**pbformat** ist **null**), werden die folgenden Standardwerte verwendet:

-   **dwOffset**: 0
-   **dwpacketlength**: 188
-   **dwstride**: 188

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Bdatypes. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Strukturen](directshow-structures.md)
</dt> <dt>

[MPEG-2-Medientypen](mpeg-2-media-types.md)
</dt> </dl>

 

 




