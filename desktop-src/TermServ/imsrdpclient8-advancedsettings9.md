---
title: IMsRdpClient8 AdvancedSettings9-Eigenschaft
description: Enthält ein Objekt, das die IMsRdpClientAdvancedSettings8-Schnittstelle unterstützt.
ms.assetid: eb7bf118-15e7-4a11-91b1-e48f18afb436
ms.tgt_platform: multiple
keywords:
- AdvancedSettings9-Eigenschaft Remotedesktopdienste
- AdvancedSettings9-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, AdvancedSettings9-Eigenschaft
- AdvancedSettings9-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, AdvancedSettings9-Eigenschaft
- AdvancedSettings9-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, AdvancedSettings9-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient8.AdvancedSettings9
- IMsRdpClient8.get_AdvancedSettings9
- IMsRdpClient9.AdvancedSettings9
- IMsRdpClient9.get_AdvancedSettings9
- IMsRdpClient10.AdvancedSettings9
- IMsRdpClient10.get_AdvancedSettings9
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fce4c6f07b0c6c798d613e5312b3ae2b258c9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339604"
---
# <a name="imsrdpclient8advancedsettings9-property"></a>IMsRdpClient8:: AdvancedSettings9-Eigenschaft

Enthält ein Objekt, das die [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) -Schnittstelle unterstützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AdvancedSettings9(
  [out, retval] IMsRdpClientAdvancedSettings8 **ppAdvSettings
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) -Schnittstelle, die das Einstellungs Objekt darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient8 ist als 4247e044-9271-43a9-bc49-e2ad9e855d62 definiert.<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





