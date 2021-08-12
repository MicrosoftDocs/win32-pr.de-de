---
title: IMsRdpClientNonScriptable3 WarnAboutSendingCredentials (Eigenschaft)
description: Gibt an oder ruft ab, ob das Dialogfeld "Sicherheitswarnung" eine Warnung zum Senden von Anmeldeinformationen an den Remoteserver enthalten soll, bevor eine Sitzung gestartet wird.
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- WarnAboutSendingCredentials-Remotedesktopdienste
- WarnAboutSendingCredentials-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste , WarnAboutSendingCredentials -Eigenschaft
- WarnAboutSendingCredentials-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste , WarnAboutSendingCredentials -Eigenschaft
- WarnAboutSendingCredentials-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , WarnAboutSendingCredentials -Eigenschaft
- WarnAboutSendingCredentials-Eigenschaft Remotedesktopdienste , MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste , WarnAboutSendingCredentials -Eigenschaft
- WarnAboutSendingCredentials-Eigenschaft Remotedesktopdienste , MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste , WarnAboutSendingCredentials -Eigenschaft
- WarnAboutSendingCredentials-Eigenschaft Remotedesktopdienste , MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste , WarnAboutSendingCredentials -Eigenschaft
- WarnAboutSendingCredentials-Eigenschaft Remotedesktopdienste , MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste , WarnAboutSendingCredentials -Eigenschaft
- WarnAboutSendingCredentials-Eigenschaft Remotedesktopdienste , MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste , WarnAboutSendingCredentials -Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.put_WarnAboutSendingCredentials
- MsRdpClient5.WarnAboutSendingCredentials
- MsRdpClient6.WarnAboutSendingCredentials
- MsRdpClient7.WarnAboutSendingCredentials
- MsRdpClient8.WarnAboutSendingCredentials
- MsRdpClient9.WarnAboutSendingCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48924b435e09b002992e6380ef130a1e11ca4961dbb0d3514b8c551f21f1b648
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607679"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a>IMsRdpClientNonScriptable3::WarnAboutSendingCredentials (Eigenschaft)

Gibt an oder ruft ab, ob das Dialogfeld "Sicherheitswarnung" eine Warnung zum Senden von Anmeldeinformationen an den Remoteserver enthalten soll, bevor eine Sitzung gestartet wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_WarnAboutSendingCredentials(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutSendingCredentials(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt an, ob das Dialogfeld "Sicherheitswarnung" eine Warnung zum Senden von Anmeldeinformationen an den Remoteserver enthalten soll, bevor eine Sitzung gestartet wird.

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

 

 





