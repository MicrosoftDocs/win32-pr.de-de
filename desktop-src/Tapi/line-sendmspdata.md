---
description: Die TSPI LINE \_ SENDMSPDATA-Nachricht wird gesendet, wenn der Telefoniedienstanbieter (Telefoniedienstanbieter, TSP) Informationen an den Mediendienstanbieter (Media Service Provider, MSP) übergeben möchte.
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: LINE_SENDMSPDATA-Nachricht (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90a4f9086bb734f73a9a28817009c11d261442cf4253791b51e48e89d511b2ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126210"
---
# <a name="line_sendmspdata-message"></a>LINE \_ SENDMSPDATA-Nachricht

Die TSPI **LINE \_ SENDMSPDATA-Nachricht** wird gesendet, wenn der Telefoniedienstanbieter (Telefoniedienstanbieter, TSP) Informationen an den Mediendienstanbieter (Media Service Provider, MSP) übergeben möchte.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*htLine* 
</dt> <dd>

Das TAPI-Handle für die Zeile.

</dd> <dt>

*htCall* 
</dt> <dd>

Das TAPI-Handle für den Aufruf.

</dd> <dt>

*dwMsg* 
</dt> <dd>

Der Wert LINE \_ SENDMSPDATA.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identifiziert den MSP, der die Nachricht empfangen soll. Bei 0 wird die Nachricht an alle MSPs gesendet. Dies ist das Handle, das an die [**\_ TSPI-Funktion LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) übergeben wird.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Der Puffer, der an den MSP übergeben werden soll. Der Puffer wird von TAPI nicht interpretiert.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Die Größe des Puffers in *dwParam2* in Bytes.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Dienstanbieter muss eine TAPI-Version 3.0 oder höher aushandeln, damit diese Nachricht funktioniert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Informationen zum Media Service Provider (MSP)](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[**TSPI \_ lineMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[**TSPI \_ LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[**\_TSPI-ZeileCloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[**TSPI \_ lineRecieveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

