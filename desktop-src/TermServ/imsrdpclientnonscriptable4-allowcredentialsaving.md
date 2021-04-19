---
title: IMsRdpClientNonScriptable4 allowkredentialsave (Eigenschaft)
description: Gibt an, ob im Dialogfeld Anmelde Informationen ein Kontrollkästchen angezeigt wird, das das Speichern von Anmelde Informationen ermöglicht.
ms.assetid: c5148ff0-0d7f-413d-b2a8-ff942668bee6
ms.tgt_platform: multiple
keywords:
- Allowkredentialsave-Eigenschaft Remotedesktopdienste
- Allowkredentialsave-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, allowkredentialsave (Eigenschaft)
- Allowkredentialsave-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, allowkredentialsave (Eigenschaft)
- Allowkredentialsave-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, allowkredentialsave (Eigenschaft)
- Allowkredentialsave-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, allowkredentialsave (Eigenschaft)
- Allowkredentialsave-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, allowkredentialsave (Eigenschaft)
- Allowkredentialsave-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, allowkredentialsave (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.AllowCredentialSaving
- IMsRdpClientNonScriptable4.get_AllowCredentialSaving
- IMsRdpClientNonScriptable4.put_AllowCredentialSaving
- IMsRdpClientNonScriptable5.AllowCredentialSaving
- IMsRdpClientNonScriptable5.get_AllowCredentialSaving
- IMsRdpClientNonScriptable5.put_AllowCredentialSaving
- MsRdpClient6.AllowCredentialSaving
- MsRdpClient7.AllowCredentialSaving
- MsRdpClient8.AllowCredentialSaving
- MsRdpClient9.AllowCredentialSaving
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240e2eb8e80209ee5c90d63f2996231cf84bb2dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339340"
---
# <a name="imsrdpclientnonscriptable4allowcredentialsaving-property"></a>IMsRdpClientNonScriptable4:: allowkredentialsave (Eigenschaft)

Gibt an, ob im Dialogfeld Anmelde Informationen ein Kontrollkästchen angezeigt wird, das das Speichern von Anmelde Informationen ermöglicht.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AllowCredentialSaving(
  [in]  VARIANT_BOOL fAllowSave
);

HRESULT get_AllowCredentialSaving(
  [out] VARIANT_BOOL *pfAllowSave
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt fest, ob im Dialogfeld Anmelde Informationen ein Kontrollkästchen angezeigt wird, das das Speichern von Anmelde Informationen ermöglicht.

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

 

 





