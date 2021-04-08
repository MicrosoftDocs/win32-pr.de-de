---
title: Imsrdppreferredredirectioninfo useredirectionservername-Eigenschaft
description: Ruft ab und legt fest, ob der Umleitungs Servername verwendet werden soll.
ms.assetid: D2239600-D75D-40FB-A6D0-4C7C4C5163E3
ms.tgt_platform: multiple
keywords:
- Useredirectionservername-Eigenschaft Remotedesktopdienste
- Useredirectionservername-Eigenschaft Remotedesktopdienste, imsrdppreferredredirectioninfo-Schnittstelle
- Imsrdppreferredredirectioninfo-Schnittstelle Remotedesktopdienste, useredirectionservername-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo.UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.get_UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.put_UseRedirectionServerName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1635273078a2d09ca01c219ebf7eaa482eeb7a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740760"
---
# <a name="imsrdppreferredredirectioninfouseredirectionservername-property"></a>Imsrdppreferredredirectioninfo:: useredirectionservername-Eigenschaft

Ruft ab und legt fest, ob der Umleitungs Servername verwendet werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_UseRedirectionServerName(
  [in]  VARIANT_BOOL UseRedirectionServerName
);

HRESULT get_UseRedirectionServerName(
  [out] VARIANT_BOOL *UseRedirectionServerName
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt an, ob der Umleitungs Servername verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                    |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ imsrdppreferredredirectioninfo ist als FDD029F9-9574-4DEF-8529-64B521CCCAA4 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdppreferredredirectioninfo**](imsrdppreferredredirectioninfo.md)
</dt> </dl>

 

 





