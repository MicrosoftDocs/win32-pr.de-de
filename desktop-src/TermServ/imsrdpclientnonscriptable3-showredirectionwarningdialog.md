---
title: IMsRdpClientNonScriptable3 showredirectionwarningdialog (Eigenschaft)
description: Gibt an oder Ruft ab, ob das Dialogfeld für die Weiterleitungs Warnung angezeigt werden soll.
ms.assetid: 7ed37288-77c3-4551-a553-1ca679e1047a
ms.tgt_platform: multiple
keywords:
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.put_ShowRedirectionWarningDialog
- MsRdpClient5.ShowRedirectionWarningDialog
- MsRdpClient6.ShowRedirectionWarningDialog
- MsRdpClient7.ShowRedirectionWarningDialog
- MsRdpClient8.ShowRedirectionWarningDialog
- MsRdpClient9.ShowRedirectionWarningDialog
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468e1721de3395067ca570c2051f3906df626071
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040330"
---
# <a name="imsrdpclientnonscriptable3showredirectionwarningdialog-property"></a>IMsRdpClientNonScriptable3:: showredirectionwarningdialog-Eigenschaft

Gibt an oder Ruft ab, ob das Dialogfeld für die Weiterleitungs Warnung angezeigt werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ShowRedirectionWarningDialog(
  [in]  VARIANT_BOOL fShowRdrDlg
);

HRESULT get_ShowRedirectionWarningDialog(
  [out] VARIANT_BOOL *pfShowRdrDlg
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt an, ob das Dialogfeld für die Weiterleitungs Warnung angezeigt werden soll.

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

 

 





