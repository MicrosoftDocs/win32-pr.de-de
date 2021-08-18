---
description: Tritt ein, wenn sich der Stift auf dem Digitizer bewegt.
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: ITabletEventSink::P ackets-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.Packets
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 29b118771fb5217ed13c01ef9376ad9b426e1ecd74a4bf931d8412a0b47e913b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712120"
---
# <a name="itableteventsinkpackets-method"></a>ITabletEventSink::P ackets-Methode

Tritt ein, wenn sich der Stift auf dem Digitizer bewegt.

## <a name="syntax"></a>Syntax


```C++
HRESULT Packets(
  [in] TABLET_CONTEXT_ID tcid,
  [in] ULONG             cPkts,
  [in] ULONG             cbPkts,
  [in] BYTE              *pbPkts,
  [in] ULONG             *pnSerialNumbers,
       t                 cid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tcid* \[ In\]
</dt> <dd>

Der Bezeichner des Tablets.

</dd> <dt>

*cPkts* \[ In\]
</dt> <dd>

Die Anzahl der Pakete.

</dd> <dt>

*cbPkts* \[ In\]
</dt> <dd>

Die Größe des Paketpuffers

</dd> <dt>

*pbPkts* \[ In\]
</dt> <dd>

Der Paketpuffer.

</dd> <dt>

*pnSerialNumbers* \[ In\]
</dt> <dd>

Das Seriennummernarray.

</dd> <dt>

*Cid* 
</dt> <dd>

Der Bezeichner des Stifts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITabletEventSink-Schnittstelle**](itableteventsink.md)
</dt> </dl>

 

 




