---
description: Stellt eine Instanz von imsmuxstreamattributesmanager bereit, die die imfattributes verwaltet, die die unter Ströme einer multiplext-Medienquelle beschreiben.
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: MF_DEVICESTREAM_MULTIPLEXED_MANAGER-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495b4054337aaa709bee430ae78ff4bed658911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359971"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a>MF- \_ Attribut "devicestream \_ multiplexed \_ Manager"

Stellt eine Instanz von [**imsmuxstreamattributesmanager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) bereit, die die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) verwaltet, die die unter Ströme einer multiplext-Medienquelle beschreiben.

## <a name="data-type"></a>Datentyp

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Bemerkungen

Übergeben Sie diesen Wert an [**imfattributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) , um zu bestimmen, ob die Medienquelle Multiplex Streams bereitstellt, und wenn dies der Fall ist, eine Instanz von [**imfmuxstreamattributesmanager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager)zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



 

 
