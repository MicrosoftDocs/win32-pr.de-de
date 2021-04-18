---
description: Legt ein Fenster für den Microsoft Media Foundation http-Byte-Stream fest.
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: MFPKEY_HTTP_ByteStream_Urlmon_Window-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372466"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a>Mfpkey \_ http \_ Bytestream- \_ URLMON- \_ Fenster (Eigenschaft)

Legt ein Fenster für den Microsoft Media Foundation http-Byte-Stream fest. Das Fenster wird verwendet, um während eines Bindungs Vorgangs Informationen in der Benutzeroberfläche darzustellen.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**IUnknown\***

VT \_ unbekannt

**punkVal**



## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Eigenschaft, um den Media Foundation http-Bytestream zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

Der Wert dieser Eigenschaft ist ein Zeiger auf die **iwindowforbindingui** -Schnittstelle. Diese Eigenschaft wird nur angewendet, wenn die Eigenschaft [mfpkey \_ http \_ Bytestream \_ enable \_ URLMON](mfpkey-http-bytestream-enable-urlmon.md) auf **Variant \_ true** festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
