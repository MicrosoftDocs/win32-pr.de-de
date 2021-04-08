---
title: IMsRdpClientNonScriptable3 redirectdynamicdevices (Eigenschaft)
description: Gibt an, ob dynamisch angefügte Plug & Play (PNP)-Geräte, die in einer Sitzung aufgelistet sind, für die Umleitung verfügbar sind, oder ruft Sie ab.
ms.assetid: 8cc5d6a4-108b-4505-8937-f6e790a5c2ba
ms.tgt_platform: multiple
keywords:
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, Eigenschaft redirectdynamicdevices
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, Eigenschaft redirectdynamicdevices
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, Eigenschaft redirectdynamicdevices
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste, redirectdynamicdevices-Eigenschaft
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, redirectdynamicdevices-Eigenschaft
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, redirectdynamicdevices-Eigenschaft
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, redirectdynamicdevices-Eigenschaft
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, redirectdynamicdevices-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDevices
- IMsRdpClientNonScriptable3.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable3.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.RedirectDynamicDevices
- IMsRdpClientNonScriptable4.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.RedirectDynamicDevices
- IMsRdpClientNonScriptable5.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.put_RedirectDynamicDevices
- MsRdpClient5.RedirectDynamicDevices
- MsRdpClient6.RedirectDynamicDevices
- MsRdpClient7.RedirectDynamicDevices
- MsRdpClient8.RedirectDynamicDevices
- MsRdpClient9.RedirectDynamicDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75224d26034e606a7a46943a02845280a092c3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740400"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdevices-property"></a>IMsRdpClientNonScriptable3:: redirectdynamicdevices (Eigenschaft)

Gibt an, ob dynamisch angefügte Plug & Play (PNP)-Geräte, die in einer Sitzung aufgelistet sind, für die Umleitung verfügbar sind, oder ruft Sie ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RedirectDynamicDevices(
  [in]  VARIANT_BOOL fRedirectDynamicDevices
);

HRESULT get_RedirectDynamicDevices(
  [out] VARIANT_BOOL *pfRedirectDynamicDevices
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt an, ob dynamisch angefügte PNP-Geräte, die in einer Sitzung aufgelistet sind, für die Umleitung verfügbar sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 ist als b3378d90-0728-45c7-8ed7-b6159fb92219 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





