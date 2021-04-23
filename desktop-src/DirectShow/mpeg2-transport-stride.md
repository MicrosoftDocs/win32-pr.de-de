---
description: Die MPEG2 \_ TRANSPORT \_ STRIDE-Struktur beschreibt das Format von MPEG-2-Transportstreampaketen (TS).
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: MPEG2_TRANSPORT_STRIDE -Struktur (Bdatypes.h)
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
ms.openlocfilehash: 5153f6f79c2807634149222a126a7256a65ffe8a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908488"
---
# <a name="mpeg2_transport_stride-structure"></a>\_ \_ MPEG2-TRANSPORT-STRIDE-Struktur

Die `MPEG2_TRANSPORT_STRIDE` -Struktur beschreibt das Format von MPEG-2-Transportstreampaketen (TS). Diese Struktur ermöglicht Transportstreams, bei denen die 188-Byte-Transportpakete nicht zusammenhängend sind. Im Sinne dieser Dokumentation werden solche Pakete als *Stride-Pakete bezeichnet.*

Stride-Pakete werden durch den folgenden Medientyp identifiziert:



| Bezeichnung | Wert |
|-------------|----------------------------------------|
| Haupttyp  | \_MEDIATYPE-Stream                      |
| Subtype     | MEDIASUBTYPE \_ \_ MPEG2-TRANSPORT-STRIDE \_ |
| Formattyp | FORMAT \_ None                           |



 

Der Formatblock (**pbFormat**) ist optional. Wenn der Formatblock enthalten ist, muss er mit einer **MPEG2 \_ \_ TRANSPORT-STRIDE-Struktur** beginnen. Diese Struktur definiert das Layout des Transportpakets innerhalb des Stride-Pakets. Wenn der Formatblock NULL **ist,** wird davon ausgegangen, dass die Pakete einen Satz von Standardwerten verwenden. Weitere Informationen finden Sie im Abschnitt "Hinweise".

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

Gibt den Offset vom Anfang des Pakets bis zum ersten Byte des eingebetteten Transportpakets in Bytes an. Der Wert muss von 0 (null) bis `(dwStride - dwPacketLength)` einschließlich liegen.

</dd> <dt>

**dwPacketLength**
</dt> <dd>

Gibt die Länge des eingebetteten Transportpakets in Bytes an. Für MPEG-2-Standardtransportpakete muss der Wert 188 Bytes betragen.

</dd> <dt>

**dwStride**
</dt> <dd>

Gibt die Länge des gesamten Schrittpakets in Bytes an. Der Wert muss mindestens `(dwOffset + dwPacketLength)` sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das folgende Diagramm veranschaulicht die Beziehungen zwischen den Strukturmembern.

![mpeg-2 stride packet](images/mpeg2-stride-packet.png)

Für Eingabepuffer, die Multiplexpakete enthalten, gelten einige Einschränkungen:

-   Schrittpakete müssen zusammenhängend innerhalb des Puffers gepackt werden.
-   Dem ersten Schrittpaket dürfen keine Bytes vorangestellt oder dem letzten Schrittpaket folgen.
-   Eine ganzzahligen Anzahl von Schrittpaketen muss in den Puffer passen. Das bedeutet, dass die Pufferlänge % dwStride gleich 0 (null) ist.

Es gibt keine Einschränkung hinsichtlich der Anzahl von Schrittpaketen pro Puffer.

Wenn der Medientyp keinen Formatblock enthält (**pbFormat** ist **NULL),** werden die folgenden Standardwerte verwendet:

-   **dwOffset:** 0
-   **dwPacketLength**: 188
-   **dwStride**: 188

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Bdatypes.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Strukturen](directshow-structures.md)
</dt> <dt>

[MPEG-2-Medientypen](mpeg-2-media-types.md)
</dt> </dl>

 

 




