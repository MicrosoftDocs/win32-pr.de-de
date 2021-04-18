---
description: Die TSPI-Zeilen- \_ sendmspdata-Nachricht wird gesendet, wenn der Telefoniedienstanbieter (TSP) Informationen an den Media Service Provider (MSP) übergeben möchte.
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: LINE_SENDMSPDATA Meldung (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce46664be0bc7f312af8b45cc5e06e13a7d91488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357617"
---
# <a name="line_sendmspdata-message"></a>Zeile \_ sendmspdata-Nachricht

Die TSPI- **Zeilen- \_ sendmspdata** -Nachricht wird gesendet, wenn der Telefoniedienstanbieter (TSP) Informationen an den Media Service Provider (MSP) übergeben möchte.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*htline* 
</dt> <dd>

Der TAPI-Handle für die Zeile.

</dd> <dt>

*"htcall"* 
</dt> <dd>

Der TAPI-Handle für den-Befehl.

</dd> <dt>

*dwmsg* 
</dt> <dd>

Die Wert Zeile \_ sendmspdata.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identifiziert den MSP, der die Nachricht empfangen soll. Wenn der Wert 0 ist, wird die Nachricht an alle MSPs gesendet. Dabei handelt es sich um das Handle, das an die Funktion [**TSPI \_ linecreatemspinstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) weitergeleitet wird.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Der Puffer, der an das MSP übergeben werden soll. Der Puffer wird nicht von TAPI interpretiert.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Die Größe (in Bytes) des Puffers in *dwParam2*.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Dienstanbieter muss eine TAPI-Version 3,0 oder höher aushandeln, damit diese Nachricht funktioniert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Informationen zum Media Service Provider (MSP)](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[**TSPI \_ linemspidentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[**TSPI \_ linecreatemspinstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[**TSPI \_ lineclosemspinstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[**TSPI \_ linerecievemspdata**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[**Linedevcaps**](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

