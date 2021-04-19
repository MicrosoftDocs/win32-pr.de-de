---
description: 'Der wiatransferparameams wird während einer Datenübertragung durch das Windows-Abbild Erfassungs Laufzeitsystem (WIA) an die iwiatransfercallback:: transfercallback-Methode an eine Anwendung übertragen.'
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: Wiatransferparameams-Struktur (WIA. h)
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
ms.openlocfilehash: 4c432cab14e08d89a49234dd7c6de059cc9d72c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348786"
---
# <a name="wiatransferparams-structure"></a>Wiatransferparameams-Struktur

Der **wiatransferparameams** wird während einer Datenübertragung durch das Windows-Abbild Erfassungs Laufzeitsystem (WIA) an die [**iwiatransfercallback:: transfercallback**](-wia-iwiatransfercallback-transfercallback.md) -Methode an eine Anwendung übertragen.

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

Type: **Long**

</dd> <dd>

Gibt den Status der Datenübertragung an.

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**Status der WIA- \_ Übertragungs Meldung \_ \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**\_ \_ \_ Ende \_ des Daten \_ Stroms der WIA-Übertragungs Nachricht**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**\_ \_ \_ Ende \_ der \_ Übertragung der WIA-Übertragungs Nachricht**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**\_ \_ \_ Geräte \_ Status der WIA-Übertragungs Meldung**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**Seite "WIA \_ Transfer \_ msg \_ New \_ "**


</dt> <dd></dd> </dl> </dd> <dt>

**lprozentuabgeschlossen**
</dt> <dd>

Type: **Long**

</dd> <dd>

Gibt den Fortschritt der Datenübertragung als Prozentsatz an.

</dd> <dt>

**ultransferredbytes**
</dt> <dd>

Typ: **ULONG64**

</dd> <dd>

Gibt die Menge der übertragenen Daten an.

</dd> <dt>

**hrerrorstatus**
</dt> <dd>

Typ: **HRESULT**

</dd> <dd>

Der Status oder Fehlerzustand des Geräts, das vom Treiber festgelegt wird. beispielsweise "Aufwärmphase".

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 




