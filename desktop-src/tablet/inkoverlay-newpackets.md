---
description: Tritt auf, wenn der frei Hand Collecto ein Paket empfängt.
ms.assetid: 26d5a3eb-430a-4e21-8a3f-fdec5005cd6e
title: InkOverlay. newpakets-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43743b47d007b44d4f2460266e7198266c36afd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218049"
---
# <a name="inkoverlaynewpackets-event"></a>InkOverlay. newpackt-Ereignis

Tritt auf, wenn das frei Hand Collecto-Paket ein Paket empfängt.

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

*Cursor* \[ in\]
</dt> <dd>

Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das Ereignis " [**nwinairpakete**](inkcollector-newinairpackets.md) " generiert hat.

</dd> <dt>

*Strich* \[ in\]
</dt> <dd>

Gibt das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt an.

</dd> <dt>

*PacketCount* \[ in\]
</dt> <dd>

Die Anzahl der für ein [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt empfangenen Pakete.

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Ein Array, das die ausgewählten Daten für das Paket enthält.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Pakete werden empfangen, während ein Strich erfasst wird. Paket Ereignisse treten schnell auf, und ein [**newpacket**](inkcollector-newpackets.md) -Ereignishandler muss schnell sein, oder die Leistung ist beeinträchtigt.

Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icenewpakete definiert.

Dieses Ereignis sollte sorgfältig verwendet werden, da es eine negative Auswirkung auf die Handschrift Leistung haben kann, wenn zu viel Code in den Ereignis Handlern ausgeführt wird.

Verwenden Sie die [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) -Eigenschaft des Ink Collector-Objekts, um festzulegen, welche Eigenschaften in diesem Array enthalten sind. Das Array, das der *packetData* -Parameter zurückgibt, enthält die Daten für diese Eigenschaften.

> [!Note]  
> Obwohl Sie die Paketdaten ändern können, werden diese Änderungen nicht beibehalten oder verwendet.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**"Nwinairpakete"-Ereignis**](inkcollector-newinairpackets.md)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




