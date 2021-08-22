---
description: Stellt eine Instanz von FLEETMuxStreamMediaTypeManager bereit, die verwendet werden kann, um die Medientypen der Unterstreams einer Multiplexmedienquelle abzurufen und die Kombination von Substreams zu steuern, die von der Quelle multiplexiert werden.
ms.assetid: 5C36956D-336A-4956-8793-D86DC792E906
title: MF_MEDIATYPE_MULTIPLEXED_MANAGER-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe00e8824997a0af89099c7fbaad4a2378b44c3360bad0d4b8808023355da2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973689"
---
# <a name="mf_mediatype_multiplexed_manager-attribute"></a>MF \_ MEDIATYPE \_ MULTIPLEXED \_ MANAGER-Attribut

Stellt eine Instanz von [**FLEETMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) bereit, die verwendet werden kann, um die Medientypen der Unterstreams einer Multiplexmedienquelle abzurufen und die Kombination von Substreams zu steuern, die von der Quelle multiplexiert werden.

## <a name="data-type"></a>Datentyp

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Hinweise

Übergeben Sie diesen Wert an [**DIE ATTRIBUTEAttributes::GetUnknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) um eine Instanz von [**COGMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager)abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1703 \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 
