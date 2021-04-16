---
title: Imsrdpclientshell publicmode (Eigenschaft)
description: Gibt an oder Ruft ab, ob der öffentliche Modus aktiviert ist.
ms.assetid: 983d3e46-f09e-4425-88a1-9d4ae0d9c70a
ms.tgt_platform: multiple
keywords:
- Publicmode-Eigenschaft Remotedesktopdienste
- Publicmode-Eigenschaft Remotedesktopdienste, imsrdpclientshell-Schnittstelle
- Imsrdpclientshell-Schnittstelle Remotedesktopdienste, publicmode-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientShell.PublicMode
- IMsRdpClientShell.get_PublicMode
- IMsRdpClientShell.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4129b3a9eeb62af0fa6e970c812ea6adf9670c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477760"
---
# <a name="imsrdpclientshellpublicmode-property"></a>Imsrdpclientshell::P ublicmode-Eigenschaft

Gibt an oder Ruft ab, ob der öffentliche Modus aktiviert ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt an, ob der öffentliche Modus aktiviert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imsrdpclientshell ist als d012ae6d-C19A-4bfe-b367-201f8911f134 definiert.<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclientshell**](imsrdpclientshell.md)
</dt> </dl>

 

 





