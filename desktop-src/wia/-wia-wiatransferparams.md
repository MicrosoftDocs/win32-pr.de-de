---
description: WiaTransferParams wird während einer Datenübertragung vom WIA-Laufzeitsystem (Windows Image Acquisition) an die IWiaTransferCallback::TransferCallback-Methode an eine Anwendung übertragen.
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: WiaTransferParams-Struktur (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaTransferParams
api_type:
- HeaderDef
api_location:
- Wia.h
ms.openlocfilehash: 7d128a39ff5d9d29bf0766273adaace7eae86b10c9556284c1f5b6f1c9285d30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449905"
---
# <a name="wiatransferparams-structure"></a>WiaTransferParams-Struktur

**WiaTransferParams** wird während einer Datenübertragung vom WIA-Laufzeitsystem (Windows Image Acquisition) an die [**IWiaTransferCallback::TransferCallback-Methode**](-wia-iwiatransfercallback-transfercallback.md) an eine Anwendung übertragen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WiaTransferParams {
  LONG    lMessage;
  LONG    lPercentComplete;
  ULONG64 ulTransferredBytes;
  HRESULT hrErrorStatus;
} WiaTransferParams;
```



## <a name="members"></a>Member

<dl> <dt>

**lMessage**
</dt> <dd>

Typ: **LONG**

</dd> <dd>

Gibt den Status der Datenübertragung an.

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**WIA \_ TRANSFER \_ MSG \_ STATUS**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**WIA \_ TRANSFER \_ MSG \_ END \_ OF \_ STREAM**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**WIA \_ TRANSFER \_ MSG \_ END \_ OF \_ TRANSFER**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**WIA \_ TRANSFER \_ MSG \_ DEVICE \_ STATUS**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**\_WIA TRANSFER \_ MSG \_ – NEUE \_ SEITE**


</dt> <dd></dd> </dl> </dd> <dt>

**lPercentComplete**
</dt> <dd>

Typ: **LONG**

</dd> <dd>

Gibt den Fortschritt der Datenübertragung als Prozentsatz an.

</dd> <dt>

**ulTransferredBytes**
</dt> <dd>

Typ: **ULONG64**

</dd> <dd>

Gibt die Menge der übertragenen Daten an.

</dd> <dt>

**hrErrorStatus**
</dt> <dd>

Typ: **HRESULT**

</dd> <dd>

Der Status oder Fehlerzustand des geräts, das vom Treiber festgelegt wurde. z. B. "aufwärmen".

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 




