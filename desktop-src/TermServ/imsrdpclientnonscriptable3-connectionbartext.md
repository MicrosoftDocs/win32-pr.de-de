---
title: IMsRdpClientNonScriptable3 ConnectionBarText-Eigenschaft
description: Legt den Text zum Aktualisieren der Verbindungsleiste fest oder ruft diesen ab.
ms.assetid: 9671118d-ee7c-4077-be81-57655aff5e35
ms.tgt_platform: multiple
keywords:
- ConnectionBarText-Eigenschaft Remotedesktopdienste
- ConnectionBarText-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste , ConnectionBarText-Eigenschaft
- ConnectionBarText-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste , ConnectionBarText-Eigenschaft
- ConnectionBarText-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , ConnectionBarText-Eigenschaft
- ConnectionBarText-Eigenschaft Remotedesktopdienste , MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste , ConnectionBarText-Eigenschaft
- ConnectionBarText-Eigenschaft Remotedesktopdienste , MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste , ConnectionBarText-Eigenschaft
- ConnectionBarText-Eigenschaft Remotedesktopdienste , MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste , ConnectionBarText-Eigenschaft
- ConnectionBarText-Eigenschaft Remotedesktopdienste , MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste , ConnectionBarText-Eigenschaft
- ConnectionBarText-Eigenschaft Remotedesktopdienste , MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste , ConnectionBarText-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ConnectionBarText
- IMsRdpClientNonScriptable3.get_ConnectionBarText
- IMsRdpClientNonScriptable3.put_ConnectionBarText
- IMsRdpClientNonScriptable4.ConnectionBarText
- IMsRdpClientNonScriptable4.get_ConnectionBarText
- IMsRdpClientNonScriptable4.put_ConnectionBarText
- IMsRdpClientNonScriptable5.ConnectionBarText
- IMsRdpClientNonScriptable5.get_ConnectionBarText
- IMsRdpClientNonScriptable5.put_ConnectionBarText
- MsRdpClient5.ConnectionBarText
- MsRdpClient6.ConnectionBarText
- MsRdpClient7.ConnectionBarText
- MsRdpClient8.ConnectionBarText
- MsRdpClient9.ConnectionBarText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dac8f704f5ecaa7bd521af10f05fd1c56d2adebff70827862478847a782faf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941593"
---
# <a name="imsrdpclientnonscriptable3connectionbartext-property"></a>IMsRdpClientNonScriptable3::ConnectionBarText-Eigenschaft

Legt den Text zum Aktualisieren der Verbindungsleiste fest oder ruft diesen ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ConnectionBarText(
  [in]  BSTR newVal
);

HRESULT get_ConnectionBarText(
  [out] BSTR *pConnectionBarText
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt die Textzeichenfolge fest, die auf der Verbindungsleiste angezeigt werden soll.

## <a name="remarks"></a>Hinweise

Sie müssen die **Methode IMsRdpClientNonScriptable3::p ut \_ ConnectionBarText** aufrufen, bevor Sie die [**IMsTscSecuredSettings::p ut \_ Fullscreen-Methode**](imstscsecuredsettings-fullscreen.md) oder die [**IMsRdpClient::p ut \_ Fullscreen-Methode**](imsrdpclient-fullscreen.md) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 ist als b3378d90-0728-45c7-8ed7-b6159fb92219 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





