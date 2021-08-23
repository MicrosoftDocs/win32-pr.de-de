---
title: IMsRdpClientAdvancedSettings6 –Eigenschaft
description: Gibt die Einstellung preconnection BLOB (BOARD) an, die vor dem Herstellen einer Verbindung für die Übertragung an den Server verwendet werden soll. | IMsRdpClientAdvancedSettings6 –Eigenschaft
ms.assetid: 3f3e6f09-2c26-44ab-9bcc-2636b71b57e2
ms.tgt_platform: multiple
keywords:
- EIGENSCHAFTEN-Remotedesktopdienste
- EIGENSCHAFTEN-Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , EIGENSCHAFT
- DIE-Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , EIGENSCHAFT
- DIE-Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , EIGENSCHAFT
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.PCB
- IMsRdpClientAdvancedSettings6.get_PCB
- IMsRdpClientAdvancedSettings6.put_PCB
- IMsRdpClientAdvancedSettings7.PCB
- IMsRdpClientAdvancedSettings7.get_PCB
- IMsRdpClientAdvancedSettings7.put_PCB
- IMsRdpClientAdvancedSettings8.PCB
- IMsRdpClientAdvancedSettings8.get_PCB
- IMsRdpClientAdvancedSettings8.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a68b34a04f99d830b525cadf6e35bc4816d7a52948916dc9a3d54664752dac38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001358"
---
# <a name="imsrdpclientadvancedsettings6pcb-property"></a>IMsRdpClientAdvancedSettings6::P CB-Eigenschaft

Gibt die Einstellung preconnection BLOB (BOARD) an, die vor dem Herstellen einer Verbindung für die Übertragung an den Server verwendet werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *pbstrPCB
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt die BLOB-Einstellung an, die vor dem Herstellen der Verbindung verwendet werden soll.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird nur von Remotedesktopverbindung 6.1- und 7.0-Clients unterstützt.

Der Server verwendet die BLOB-Einstellung, um den Zielprozess für die Verbindung zu identifizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





