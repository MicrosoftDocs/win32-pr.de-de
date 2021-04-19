---
description: Tritt auf, wenn ein in-Air-Paket angezeigt wird.
ms.assetid: e8eacdec-0381-435f-b453-24dca1c507c9
title: InkCollector. nwinairpaketen-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d942aa474b5cb53d01f5ce83d2bd3ec28d521c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360679"
---
# <a name="inkcollectornewinairpackets-event"></a>InkCollector. nwinairpakete-Ereignis

Tritt auf, wenn ein in-Air-Paket angezeigt wird.

## <a name="syntax"></a>Syntax


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ in\]
</dt> <dd>

Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das Ereignis " **nwinairpakete** " generiert hat.

</dd> <dt>

*PacketCount* \[ in\]
</dt> <dd>

Die Anzahl der empfangenen in-Air-Pakete.

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält Sie ein Array, das die ausgewählten Daten für das Paket enthält.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Ein in-Air-Paket wird erstellt, wenn ein Benutzer einen Stift in der Nähe des Tablets bewegt und sich der Cursor im Fenster des Ink Collector-Objekts befindet oder wenn der Benutzer eine Maus innerhalb des zugehörigen Fensters des Ink Collector-Objekts bewegt. Das generieren **von Ereignissen wird** schnell und der Ereignishandler muss schnell oder leistungsstark beeinträchtigt sein.

Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icenewinairpakete definiert.

Das Ereignis " **netwinairpackt** " wird auch dann ausgelöst, wenn es sich im Modus "auswählen" oder "Löschen" befindet Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie für die Festlegung verantwortlich sind) und den Modus beachten, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist, dass die Innovationen auf der Plattform durch ein höheres Bewusstsein für Platt Form Ereignisse verstärkt werden.

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

[**InkCollector-Klasse**](inkcollector-class.md)
</dt> <dt>

[**DesiredPacketDescription (Eigenschaft)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[**Newpakete-Ereignis**](inkcollector-newpackets.md)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




