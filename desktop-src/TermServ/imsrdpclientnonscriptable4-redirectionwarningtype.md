---
title: IMsRdpClientNonScriptable4 redirectionwarningtype (Eigenschaft)
description: Steuert das vorhanden sein und die Darstellung des Dialog Felds, in dem der Benutzer über die Umleitung benachrichtigt wird.
ms.assetid: 1aa79fc3-9620-466d-a93f-77a55ad76ede
ms.tgt_platform: multiple
keywords:
- Redirectionwarningtype-Eigenschaft Remotedesktopdienste
- Redirectionwarningtype-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, Eigenschaft redirectionwarningtype
- Redirectionwarningtype-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, Eigenschaft redirectionwarningtype
- Redirectionwarningtype-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6 Object Remotedesktopdienste, Eigenschaft redirectionwarningtype
- Redirectionwarningtype-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7 Object Remotedesktopdienste, Eigenschaft redirectionwarningtype
- Redirectionwarningtype-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8 Object Remotedesktopdienste, Eigenschaft redirectionwarningtype
- Redirectionwarningtype-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9 Object Remotedesktopdienste, Eigenschaft redirectionwarningtype
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.RedirectionWarningType
- IMsRdpClientNonScriptable4.get_RedirectionWarningType
- IMsRdpClientNonScriptable4.put_RedirectionWarningType
- IMsRdpClientNonScriptable5.RedirectionWarningType
- IMsRdpClientNonScriptable5.get_RedirectionWarningType
- IMsRdpClientNonScriptable5.put_RedirectionWarningType
- MsRdpClient6.RedirectionWarningType
- MsRdpClient7.RedirectionWarningType
- MsRdpClient8.RedirectionWarningType
- MsRdpClient9.RedirectionWarningType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077c8f78c61cc9b7dd090db26f58ca7e28c14abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341396"
---
# <a name="imsrdpclientnonscriptable4redirectionwarningtype-property"></a>IMsRdpClientNonScriptable4:: redirectionwarningtype (Eigenschaft)

Steuert das vorhanden sein und die Darstellung des Dialog Felds, in dem der Benutzer über die Umleitung benachrichtigt wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RedirectionWarningType(
  [in]  RedirectionWarningType wrnType
);

HRESULT get_RedirectionWarningType(
  [out] RedirectionWarningType *pWrnType
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt den Typ des Dialog Felds fest, in dem der Benutzer über eine Umleitung benachrichtigt wird.

<dt>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**Redirectionwarningtypedefault** (0x0000)


</dt> <dd>

Das Dialogfeld ist nicht Herausgeber spezifisch.

</dd> <dt>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**Redirectionwarningtypeunsigned** (0x0001)


</dt> <dd>

Das Dialogfeld ist für nicht signierte Dateien.

</dd> <dt>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**Redirectionwarningtypeunknown** (0x0002)


</dt> <dd>

Das Dialogfeld ist für einen unbekannten Verleger vorgesehen.

</dd> <dt>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**Redirectionwarningtypeuser** (0x0003)


</dt> <dd>

Das Dialogfeld ist für die Dateien des Benutzers.

</dd> <dt>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**Redirectionwarningtypethirdpartysigned** (0x0004)


</dt> <dd>

Das Dialogfeld wird für Drittanbieter-zertifizierte signierte Dateien angezeigt.

</dd> <dt>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**Redirectionwarningtypetrusted** (0x0005)


</dt> <dd>

Das Dialogfeld wird nicht angezeigt, da die Anwendung von einem vertrauenswürdigen Herausgeber veröffentlicht wird.

</dd> <dt>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**Redirectionwarningtypemax** (0x0005)


</dt> <dd>

Das Dialogfeld wird nicht angezeigt, da die Anwendung von einem vertrauenswürdigen Herausgeber veröffentlicht wird.

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Der Wert **redirectionwarningtypedefault**, bei dem es sich um den Standardwert dieser Eigenschaft handelt, wirkt sich nicht auf das Dialogfeld aus. Die steuernde Eigenschaft ist in diesem Fall " [**showredirectionwarningdialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) " in [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).

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

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





