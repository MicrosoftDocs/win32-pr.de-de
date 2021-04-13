---
title: IMsRdpClientNonScriptable4 warnaboutprinterredirect (Eigenschaft)
description: Steuert, ob im Dialogfeld Umleitung eine Meldung zur Drucker Umleitung angezeigt wird, bevor eine Sitzung gestartet wird.
ms.assetid: 12c5bc8d-7bc1-4a94-a9b8-6b852772c936
ms.tgt_platform: multiple
keywords:
- Warnaboutprinterredirect-Eigenschaft Remotedesktopdienste
- Warnaboutprinterredirect-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, warnaboutprinterredirect (Eigenschaft)
- Warnaboutprinterredirect-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, warnaboutprinterredirect (Eigenschaft)
- Warnaboutprinterredirect-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, warnaboutprinterredirect-Eigenschaft
- Warnaboutprinterredirect-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, warnaboutprinterredirect-Eigenschaft
- Warnaboutprinterredirect-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, warnaboutprinterredirect-Eigenschaft
- Warnaboutprinterredirect-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, warnaboutprinterredirect-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutPrinterRedirection
- MsRdpClient6.WarnAboutPrinterRedirection
- MsRdpClient7.WarnAboutPrinterRedirection
- MsRdpClient8.WarnAboutPrinterRedirection
- MsRdpClient9.WarnAboutPrinterRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e2fa93995946e741caa76f1ee5b84be79d9c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340807"
---
# <a name="imsrdpclientnonscriptable4warnaboutprinterredirection-property"></a>IMsRdpClientNonScriptable4:: warnaboutprinterredirect-Eigenschaft

Steuert, ob im Dialogfeld Umleitung eine Meldung zur Drucker Umleitung angezeigt wird, bevor eine Sitzung gestartet wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_WarnAboutPrinterRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutPrinterRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt fest, ob im Dialogfeld Umleitung eine Meldung zur Drucker Umleitung angezeigt wird.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

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

 

 





