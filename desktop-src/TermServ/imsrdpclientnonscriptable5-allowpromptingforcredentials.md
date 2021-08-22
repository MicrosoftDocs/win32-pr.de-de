---
title: IMsRdpClientNonScriptable5 AllowPromptingForCredentials-Eigenschaft
description: Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Benutzer zur Eingabe von Anmeldeinformationen auffordern kann.
ms.assetid: 9a780886-39ee-4d3b-9a54-fa209708d9f8
ms.tgt_platform: multiple
keywords:
- AllowPromptingForCredentials-Eigenschaft Remotedesktopdienste
- AllowPromptingForCredentials-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , AllowPromptingForCredentials-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.get_AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.put_AllowPromptingForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea0fb854b5bb12533032cd6608228d81584cd8d9f4e99bccd8a5ba76b624f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138753"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a>IMsRdpClientNonScriptable5::AllowPromptingForCredentials-Eigenschaft

Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Benutzer zur Eingabe von Anmeldeinformationen auffordern kann. Wenn diese Eigenschaft **VARIANT \_ TRUE** enthält, kann der Benutzer zur Eingabe von Anmeldeinformationen aufgefordert werden. Wenn diese Eigenschaft **VARIANT \_ FALSE** enthält, kann der Benutzer nicht zur Eingabe von Anmeldeinformationen aufgefordert werden.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AllowPromptingForCredentials(
  [in]          VARIANT_BOOL fAllow
);

HRESULT get_AllowPromptingForCredentials(
  [out, retval] VARIANT_BOOL *pfAllow
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt den neuen Eigenschaftswert an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | \_IID-IMsRdpClientNonScriptable5 ist als 4f6996d5-d7b1-412c-b0ff-063718566907 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





