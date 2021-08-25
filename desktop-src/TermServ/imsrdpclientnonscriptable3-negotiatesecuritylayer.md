---
title: IMsRdpClientNonScriptable3 NegotiateSecurityLayer-Eigenschaft
description: Gibt an oder ruft ab, ob die Aushandlungssicherheitsebene für die Verbindung aktiviert ist.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- NegotiateSecurityLayer-Eigenschaft Remotedesktopdienste
- NegotiateSecurityLayer-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste , NegotiateSecurityLayer-Eigenschaft
- NegotiateSecurityLayer-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste , NegotiateSecurityLayer-Eigenschaft
- NegotiateSecurityLayer-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , NegotiateSecurityLayer-Eigenschaft
- NegotiateSecurityLayer-Eigenschaft Remotedesktopdienste , MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste , NegotiateSecurityLayer-Eigenschaft
- NegotiateSecurityLayer-Eigenschaft Remotedesktopdienste , MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste , NegotiateSecurityLayer-Eigenschaft
- NegotiateSecurityLayer-Eigenschaft Remotedesktopdienste , MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste , NegotiateSecurityLayer-Eigenschaft
- NegotiateSecurityLayer-Eigenschaft Remotedesktopdienste , MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste , NegotiateSecurityLayer-Eigenschaft
- NegotiateSecurityLayer-Eigenschaft Remotedesktopdienste , MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste , NegotiateSecurityLayer-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.put_NegotiateSecurityLayer
- MsRdpClient5.NegotiateSecurityLayer
- MsRdpClient6.NegotiateSecurityLayer
- MsRdpClient7.NegotiateSecurityLayer
- MsRdpClient8.NegotiateSecurityLayer
- MsRdpClient9.NegotiateSecurityLayer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13f87abb5323289e60e3d29fa93d5e858a9a755224e7161ba28970ef5ccb186f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771550"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a>IMsRdpClientNonScriptable3::NegotiateSecurityLayer-Eigenschaft

Gibt an oder ruft ab, ob die Aushandlungssicherheitsebene für die Verbindung aktiviert ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt an, ob die Aushandlung der Sicherheitsschicht aktiviert werden soll.

## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft auf **VARIANT \_ FALSE** festgelegt ist und Authentifizierung auf Netzwerkebene (NLA) auf dem Clientbetriebssystem aktiviert ist, handelt der Client die Sicherheitsschicht nicht aus und verwendet stattdessen NLA, um die RDP-Verbindung zu schützen. Wenn diese Eigenschaft auf **VARIANT \_ TRUE** festgelegt ist, handelt der Client zwischen NLA und grundlegender RDP-Sicherheit aus.

> [!Note]  
> Das Deaktivieren der Sicherheitsschichtaushandlung ist nur möglich, wenn eine Verbindung mit einem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) hergestellt wird, auf dem Windows Vista oder höher ausgeführt wird. Wenn diese Eigenschaft aktiviert ist und der Client versucht, eine Verbindung mit einem RD-Sitzungshost Server herzustellen, auf dem ein früheres Betriebssystem ausgeführt wird, tritt bei der Verbindung ein Fehler auf.

 

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

 

 





