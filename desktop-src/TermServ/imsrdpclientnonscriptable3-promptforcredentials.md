---
title: IMsRdpClientNonScriptable3 PromptForCredentials-Eigenschaft (Wuapi.h)
description: Gibt an oder ruft ab, ob das Dialogfeld zur Eingabe von Anmeldeinformationen für die Verbindung aktiviert ist.
ms.assetid: 252ec5bd-bd52-40d4-ae48-b2c00c0720c0
ms.tgt_platform: multiple
keywords:
- PromptForCredentials-Remotedesktopdienste
- PromptForCredentials-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste , PromptForCredentials-Eigenschaft
- PromptForCredentials-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste , PromptForCredentials-Eigenschaft
- PromptForCredentials-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , PromptForCredentials-Eigenschaft
- PromptForCredentials-Eigenschaft Remotedesktopdienste , MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste , PromptForCredentials-Eigenschaft
- PromptForCredentials-Eigenschaft Remotedesktopdienste , MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste , PromptForCredentials-Eigenschaft
- PromptForCredentials-Eigenschaft Remotedesktopdienste , MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste , PromptForCredentials-Eigenschaft
- PromptForCredentials-Eigenschaft Remotedesktopdienste , MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste , PromptForCredentials-Eigenschaft
- PromptForCredentials-Eigenschaft Remotedesktopdienste , MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste , PromptForCredentials-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.PromptForCredentials
- IMsRdpClientNonScriptable3.get_PromptForCredentials
- IMsRdpClientNonScriptable3.put_PromptForCredentials
- IMsRdpClientNonScriptable4.PromptForCredentials
- IMsRdpClientNonScriptable4.get_PromptForCredentials
- IMsRdpClientNonScriptable4.put_PromptForCredentials
- IMsRdpClientNonScriptable5.PromptForCredentials
- IMsRdpClientNonScriptable5.get_PromptForCredentials
- IMsRdpClientNonScriptable5.put_PromptForCredentials
- MsRdpClient5.PromptForCredentials
- MsRdpClient6.PromptForCredentials
- MsRdpClient7.PromptForCredentials
- MsRdpClient8.PromptForCredentials
- MsRdpClient9.PromptForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcfb206e8479892b5c8e2e544d3c660c2dcfbd76c6dfe3c66f382c78c734e9bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001120"
---
# <a name="imsrdpclientnonscriptable3promptforcredentials-property"></a>IMsRdpClientNonScriptable3::P romptForCredentials-Eigenschaft

Gibt an oder ruft ab, ob das Dialogfeld zur Eingabe von Anmeldeinformationen für die Verbindung aktiviert ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PromptForCredentials(
  [in]  VARIANT_BOOL fPrompt
);

HRESULT get_PromptForCredentials(
  [out] VARIANT_BOOL *pfPrompt
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt an, ob das Dialogfeld "Eingabeaufforderung für Anmeldeinformationen" für die Verbindung aktiviert ist.

## <a name="error-codes"></a>Fehlercodes

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Header<br/>                   | <dl> <dt>Wuapi.h</dt> </dl>            |
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

 

 





