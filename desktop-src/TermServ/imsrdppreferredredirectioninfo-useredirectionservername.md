---
title: IMsRdpPreferredRedirectionInfo UseRedirectionServerName-Eigenschaft
description: Ruft ab und legt fest, ob der Umleitungsservername verwendet werden soll.
ms.assetid: D2239600-D75D-40FB-A6D0-4C7C4C5163E3
ms.tgt_platform: multiple
keywords:
- UseRedirectionServerName-Eigenschaft Remotedesktopdienste
- UseRedirectionServerName-Eigenschaft Remotedesktopdienste , IMsRdpPreferredRedirectionInfo-Schnittstelle
- IMsRdpPreferredRedirectionInfo-Schnittstelle Remotedesktopdienste , UseRedirectionServerName-Eigenschaft
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
ms.openlocfilehash: d1bb57bacafbc3061cee6cb49b09a8fdbf8187026a378deff605b90472ed6394
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513250"
---
# <a name="imsrdppreferredredirectioninfouseredirectionservername-property"></a>IMsRdpPreferredRedirectionInfo::UseRedirectionServerName -Eigenschaft

Ruft ab und legt fest, ob der Umleitungsservername verwendet werden soll.

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

Gibt an, ob der Umleitungsservername verwendet werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                    |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpPreferredRedirectionInfo ist als FDD029F9-9574-4DEF-8529-64B521CCCAA4 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpPreferredRedirectionInfo**](imsrdppreferredredirectioninfo.md)
</dt> </dl>

 

 





