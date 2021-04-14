---
title: IMsRdpClientNonScriptable4-Eigenschaft "Treuhänder-OneSite"
description: Gibt an, ob die Website, von der der Benutzer die Verbindung gestartet hat, in der Liste der vertrauenswürdigen Sites auf dem Client Computer des Benutzers enthalten ist.
ms.assetid: cb7efacc-b13b-494c-ab02-35c4f914744c
ms.tgt_platform: multiple
keywords:
- Eigenschaft "Treuhänder-OneSite" Remotedesktopdienste
- Eigenschaft "Treuhänder-OneSite" Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, Eigenschaft "Treuhänder-OneSite"
- Eigenschaft "Treuhänder-OneSite" Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, Eigenschaft "Treuhänder-OneSite"
- Eigenschaft "Treuhänder-OneSite" Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, Eigenschaft "Treuhänder-OneSite"
- Eigenschaft "Treuhänder-OneSite" Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, Eigenschaft "Treuhänder-OneSite"
- Eigenschaft "Treuhänder-OneSite" Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, Eigenschaft "Treuhänder-OneSite"
- Eigenschaft "Treuhänder-OneSite" Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, Eigenschaft "Treuhänder-OneSite"
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.TrustedZoneSite
- IMsRdpClientNonScriptable4.get_TrustedZoneSite
- IMsRdpClientNonScriptable4.put_TrustedZoneSite
- IMsRdpClientNonScriptable5.TrustedZoneSite
- IMsRdpClientNonScriptable5.get_TrustedZoneSite
- IMsRdpClientNonScriptable5.put_TrustedZoneSite
- MsRdpClient6.TrustedZoneSite
- MsRdpClient7.TrustedZoneSite
- MsRdpClient8.TrustedZoneSite
- MsRdpClient9.TrustedZoneSite
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791b5eff3346f61f999ea1f4f78bc41a5acea0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392029"
---
# <a name="imsrdpclientnonscriptable4trustedzonesite-property"></a>IMsRdpClientNonScriptable4:: treuhändzonesite-Eigenschaft

Gibt an, ob die Website, von der der Benutzer die Verbindung gestartet hat, in der Liste der vertrauenswürdigen Sites auf dem Client Computer des Benutzers enthalten ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_TrustedZoneSite(
  [in]  VARIANT_BOOL fIsTrustedZone
);

HRESULT get_TrustedZoneSite(
  [out] VARIANT_BOOL *pfIsTrustedZone
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt die Eigenschaft "Treuhänder-OneSite" fest. Diese Methode wirkt sich nicht darauf aus, ob die Website, von der der Benutzer die Verbindung gestartet hat, in der Liste der vertrauenswürdigen Sites des Client Computers enthalten ist.

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

 

 





