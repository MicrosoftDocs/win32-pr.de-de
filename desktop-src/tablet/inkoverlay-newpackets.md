---
description: Tritt ein, wenn der Ink Collecto ein Paket rreceive.
ms.assetid: 26d5a3eb-430a-4e21-8a3f-fdec5005cd6e
title: InkOverlay.NewPackets-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2571e7c8f97881da5bbbef6cdab093ce2d3107b5482def5b62d2dfa141c7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219197"
---
# <a name="inkoverlaynewpackets-event"></a>InkOverlay.NewPackets-Ereignis

Tritt ein, wenn der Ink Collecto ein Paket rreceive

## <a name="syntax"></a>Syntax


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**NewInAirPackets-Ereignis generiert**](inkcollector-newinairpackets.md) hat.

</dd> <dt>

*Strich* \[ In\]
</dt> <dd>

Gibt das [**IInkStrokeDisp-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) an.

</dd> <dt>

*PacketCount* \[ In\]
</dt> <dd>

Die Anzahl der empfangenen Pakete für ein [**IInkStrokeDisp-Objekt.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Ein Array, das die ausgewählten Daten für das Paket enthält.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Pakete werden empfangen, während ein Strich erfasst wird. Paketereignisse treten schnell auf, und ein [**NewPackets-Ereignishandler**](inkcollector-newpackets.md) muss schnell sein oder die Leistung beeinträchtigen.

Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICENewPackets definiert.

Dieses Ereignis sollte sorgfältig verwendet werden, da es sich negativ auf die Ink-Leistung auswirken kann, wenn in den Ereignishandlern zu viel Code ausgeführt wird.

Verwenden Sie zum Festlegen der in diesem Array enthaltenen Eigenschaften die [**DesiredPacketDescription-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) des Ink-Collectorobjekts. Das Array, das der *PacketData-Parameter* zurückgibt, enthält die Daten für diese Eigenschaften.

> [!Note]  
> Obwohl Sie die Paketdaten ändern können, werden diese Änderungen nicht beibehalten oder verwendet.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**NewInAirPackets-Ereignis**](inkcollector-newinairpackets.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




