---
description: 'Enthält einen Zeiger auf das Token, das für die imfmediastream:: requestsample-Methode bereitgestellt wurde.'
ms.assetid: 9403bb15-e912-4aa3-9af1-fef4a4f9b242
title: MFSampleExtension_Token-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17331ad098f80c2676e9d057e1688a776cee305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350530"
---
# <a name="mfsampleextension_token-attribute"></a>MF Sample Extension- \_ tokenattribut

Enthält einen Zeiger auf das Token, das für die [**imfmediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode bereitgestellt wurde.

## <a name="data-type"></a>Datentyp

**IUnknown \** _

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>Gilt für:

[**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Medien Beispiele. Der Wert des-Attributs ist der **IUnknown** -Zeiger, der an den *pToken* -Parameter der [**requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode übergeben wird. Der Aufrufer verwendet dieses Attribut, um den Status der Anforderung zu überprüfen.

Wenn Sie eine benutzerdefinierte Medienquelle schreiben, legen Sie dieses Attribut für das Beispiel fest, wenn der Mediendaten Strom ein Beispiel als Antwort auf die [**requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode liefert, es sei denn, der Wert von *pToken* ist **null**.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Beispiel Attribute](sample-attributes.md)
</dt> <dt>

[Medien Beispiele](media-samples.md)
</dt> </dl>

 

 




