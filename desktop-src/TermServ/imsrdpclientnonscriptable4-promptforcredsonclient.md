---
title: IMsRdpClientNonScriptable4 PromptForCredsOnClient (Eigenschaft)
description: Gibt an, ob das Clientsteuerfeld ein Dialogfeld anzeigt, das zur Eingabe von Anmeldeinformationen aufgefordert wird.
ms.assetid: 426676be-0150-4a33-acd0-26423966f32a
ms.tgt_platform: multiple
keywords:
- PromptForCredsOnClient-Remotedesktopdienste
- PromptForCredsOnClient-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste , PromptForCredsOnClient-Eigenschaft
- PromptForCredsOnClient-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , PromptForCredsOnClient-Eigenschaft
- PromptForCredsOnClient-Eigenschaft Remotedesktopdienste , MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste , PromptForCredsOnClient-Eigenschaft
- PromptForCredsOnClient-Eigenschaft Remotedesktopdienste , MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste , PromptForCredsOnClient-Eigenschaft
- PromptForCredsOnClient-Eigenschaft Remotedesktopdienste , MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste , PromptForCredsOnClient-Eigenschaft
- PromptForCredsOnClient-Eigenschaft Remotedesktopdienste , MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste , PromptForCredsOnClient-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PromptForCredsOnClient
- IMsRdpClientNonScriptable4.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable4.put_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.PromptForCredsOnClient
- IMsRdpClientNonScriptable5.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.put_PromptForCredsOnClient
- MsRdpClient6.PromptForCredsOnClient
- MsRdpClient7.PromptForCredsOnClient
- MsRdpClient8.PromptForCredsOnClient
- MsRdpClient9.PromptForCredsOnClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd914e831f43ffd6dba88bd6b1879ab578902dfb0442d26397344a0df71f8c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941502"
---
# <a name="imsrdpclientnonscriptable4promptforcredsonclient-property"></a>IMsRdpClientNonScriptable4::P romptForCredsOnClient (Eigenschaft)

Gibt an, ob das Clientsteuerfeld ein Dialogfeld anzeigt, das zur Eingabe von Anmeldeinformationen aufgefordert wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PromptForCredsOnClient(
  [in]  VARIANT_BOOL fPromptForCredsOnClient
);

HRESULT get_PromptForCredsOnClient(
  [out] VARIANT_BOOL *pfPromptForCredsOnClient
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt fest, ob das Clientsteuerfeld ein Dialogfeld anzeigt, das zur Eingabe von Anmeldeinformationen aufgefordert wird.

## <a name="error-codes"></a>Fehlercodes

Gibt **S \_ OK zurück,** wenn erfolgreich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 ist als f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





