---
title: IMsRdpClientNonScriptable3 warnaboutsending-Anmelde Informationen (Eigenschaft)
description: Gibt an oder Ruft ab, ob das Dialogfeld Sicherheitswarnung eine Warnung zum Senden von Anmelde Informationen an den Remote Server enthalten soll, bevor eine Sitzung gestartet wird.
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- Eigenschaften Remotedesktopdienste warnaboutsending-Anmelde Informationen
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
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
ms.openlocfilehash: 29d9d2fcfe158f5a0bb6812002bfcc160f1c9009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339549"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a>IMsRdpClientNonScriptable3:: warnaboutsendinganmeldeinformationen (Eigenschaft)

Gibt an oder Ruft ab, ob das Dialogfeld Sicherheitswarnung eine Warnung zum Senden von Anmelde Informationen an den Remote Server enthalten soll, bevor eine Sitzung gestartet wird.

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

Gibt an, ob das Dialogfeld Sicherheitswarnung eine Warnung zum Senden von Anmelde Informationen an den Remote Server enthalten soll, bevor eine Sitzung gestartet wird.

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

 

 





