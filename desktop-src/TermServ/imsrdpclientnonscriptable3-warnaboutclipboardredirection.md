---
title: IMsRdpClientNonScriptable3 warnaboutclipboardredirection (Eigenschaft)
description: Gibt an oder Ruft ab, ob das Dialogfeld Sicherheitswarnung angezeigt werden soll, um Benutzer vor der Zwischenablage Umleitung zu warnen.
ms.assetid: 2f3ca58b-3c89-4251-ae15-2c0aaf308893
ms.tgt_platform: multiple
keywords:
- Die warnaboutclipboardredirection-Eigenschaft Remotedesktopdienste
- Warnaboutclipboardredirection-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, warnaboutclipboardredirection-Eigenschaft
- Warnaboutclipboardredirection-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, warnaboutclipboardredirection-Eigenschaft
- Warnaboutclipboardredirection-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, warnaboutclipboardredirection-Eigenschaft
- Warnaboutclipboardredirection-Eigenschaft Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste, warnaboutclipboardredirection-Eigenschaft
- Warnaboutclipboardredirection-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, warnaboutclipboardredirection-Eigenschaft
- Warnaboutclipboardredirection-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, warnaboutclipboardredirection-Eigenschaft
- Warnaboutclipboardredirection-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, warnaboutclipboardredirection-Eigenschaft
- Warnaboutclipboardredirection-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, warnaboutclipboardredirection-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutClipboardRedirection
- MsRdpClient5.WarnAboutClipboardRedirection
- MsRdpClient6.WarnAboutClipboardRedirection
- MsRdpClient7.WarnAboutClipboardRedirection
- MsRdpClient8.WarnAboutClipboardRedirection
- MsRdpClient9.WarnAboutClipboardRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8da6fa2f7fb36a110666c8b14a818264813d816
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517546"
---
# <a name="imsrdpclientnonscriptable3warnaboutclipboardredirection-property"></a>IMsRdpClientNonScriptable3:: warnaboutclipboardredirection-Eigenschaft

Gibt an oder Ruft ab, ob das Dialogfeld Sicherheitswarnung angezeigt werden soll, um Benutzer vor der Zwischenablage Umleitung zu warnen.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_WarnAboutClipboardRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutClipboardRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt an, ob das Dialogfeld Sicherheitswarnung angezeigt werden soll, um Benutzer vor der Zwischenablage Umleitung zu warnen.

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

 

 





