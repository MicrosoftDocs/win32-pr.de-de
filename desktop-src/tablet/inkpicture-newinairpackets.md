---
description: 'InkPicture.NewInAirPackets-Ereignis: Tritt auf, wenn ein In-Air-Paket gesehen wird.'
ms.assetid: 30bc423d-0642-4515-9e51-a8b8b36aecad
title: InkPicture.NewInAirPackets-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f81f6f485329eaa5cd96c2aece39646e700a21bc762c5d66344e5daf0a628f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967049"
---
# <a name="inkpicturenewinairpackets-event"></a>InkPicture.NewInAirPackets-Ereignis

Tritt ein, wenn ein Paket in der Luft gesehen wird.

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

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **NewInAirPackets-Ereignis generiert** hat.

</dd> <dt>

*PacketCount* \[ In\]
</dt> <dd>

Die Anzahl der empfangenen In-Air-Pakete.

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Ein Array, das die ausgewählten Daten für das Paket enthält.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Ein In-Air-Paket wird erstellt, wenn ein Benutzer einen Stift in die Nähe des Tablets verschiebt und sich der Cursor im Fenster des Freiformsammlerobjekts befindet oder der Benutzer eine Maus im zugeordneten Fenster des Freiformsammlerobjekts bewegt. **NewInAirPackets-Ereignisse** werden schnell generiert, und der Ereignishandler muss schnell sein oder die Leistung beeinträchtigen.

Diese Ereignismethode wird in den Dispatch-Schnittstellen **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ ICENewInAirPackets definiert.

Das **NewInAirPackets-Ereignis** wird auch dann ausgelöst, wenn es sich im Auswahl- oder Löschmodus befindet, nicht nur beim Einfügen von Ink. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein größeres Bewusstsein für Plattformereignisse.

Verwenden Sie zum Festlegen der in diesem Array enthaltenen Eigenschaften die [**DesiredPacketDescription-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) des Ink-Collectorobjekts. Das Array, das der *PacketData-Parameter* zurückgibt, enthält die Daten für diese Eigenschaften.

> [!Note]  
> Obwohl Sie die Paketdaten ändern können, werden diese Änderungen nicht beibehalten oder verwendet.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**DesiredPacketDescription-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription)
</dt> <dt>

[**NewPackets-Ereignis**](inkpicture-newpackets.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




